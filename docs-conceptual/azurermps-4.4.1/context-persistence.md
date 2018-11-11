---
title: Conservare le credenziali utente tra le sessioni di PowerShell
description: Informazioni su come riutilizzare le credenziali di Azure e altre informazioni in più sessioni di PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: 85de158cd2a4c3a38f653a530db8e6fae50cb37f
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211129"
---
# <a name="persisting-user-credentials-across-powershell-sessions"></a>Conservare le credenziali utente tra le sessioni di PowerShell

Azure PowerShell offre una funzionalità denominata **salvataggio automatico del contesto Azure**, che fornisce le funzionalità seguenti:

- Conservazione delle informazioni di accesso per il riutilizzo in nuove sessioni di PowerShell.
- Uso semplificato di attività in background per eseguire cmdlet con esecuzione prolungata.
- Passaggio da un account, una sottoscrizione o un ambiente all'altro senza un accesso separato.
- Esecuzione simultanea di attività con credenziali e sottoscrizioni diverse dalla stessa sessione di PowerShell.

## <a name="azure-contexts-defined"></a>Definizione dei contesti Azure

Un *contesto Azure* è un set di informazioni che definisce la destinazione dei cmdlet di Azure PowerShell. Il contesto è costituito da cinque parti.

- *Account*: entità servizio o nome utente usato per l'autenticazione delle comunicazioni con Azure.
- *Sottoscrizione*: sottoscrizione di Azure contenente le risorse su cui vengono eseguire le operazioni.
- *Tenant*: tenant di Azure Active Directory contenente la sottoscrizione. I tenant sono particolarmente importanti per l'autenticazione di entità servizio.
- *Ambiente*: specifico cloud di Azure di destinazione, in genere il cloud globale di Azure.
  L'impostazione dell'ambiente consente tuttavia di specificare come destinazione anche cloud nazionali, per enti pubblici e locali (Azure Stack).
- *Credenziali*: informazioni usate da Azure per verificare l'identità dell'utente e la relativa autorizzazione ad accedere alle risorse in Azure.

Nelle versioni precedenti, il contesto Azure deve essere creato ogni volta che viene aperta una nuova sessione di PowerShell. A partire da Azure PowerShell v4.4.0, è possibile abilitare il salvataggio automatico dei contesti Azure e il relativo riutilizzo all'apertura di una nuova sessione di PowerShell.

## <a name="automatically-saving-the-context-for-the-next-sign-in"></a>Salvataggio automatico del contesto per l'accesso successivo

Per impostazione predefinita, Azure PowerShell rimuove le informazioni di contesto alla chiusura della sessione di PowerShell.

Per consentire ad Azure PowerShell di mantenere il contesto memorizzato dopo la chiusura della sessione di PowerShell, usare `Enable-AzureRmContextAutosave`. Le informazioni relative al contesto e alle credenziali vengono salvate automaticamente in una speciale cartella nascosta nella directory dell'utente (`%AppData%\Roaming\Windows Azure PowerShell`).
Successivamente, ogni nuova sessione di PowerShell avrà come destinazione il contesto usato nell'ultima sessione.

Per annullare la memorizzazione del contesto e delle credenziali in PowerShell, usare `Disable-AzureRmContextAutoSave`. Sarà necessario eseguire l'accesso ad Azure ogni volta che si apre una sessione di PowerShell.

I cmdlet che consentono di gestire i contesti Azure permettono anche un controllo con granularità fine. Se si vuole, è possibile applicare le modifiche solo alla sessione di PowerShell corrente (ambito `Process`) o a ogni sessione di PowerShell (ambito `CurrentUser`). Questo opzioni sono descritte più dettagliatamente in [Uso degli ambiti dei contesti](#Using-Context-Scopes).

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a>Esecuzione dei cmdlet di Azure PowerShell come processi in background

La funzionalità di **salvataggio automatico del contesto Azure** consente anche di condividere il contesto con processi in background di PowerShell. In PowerShell è possibile avviare e monitorare attività con esecuzione prolungata come processi in background senza dover attendere il completamento delle attività. Per condividere le credenziali con i processi in background sono disponibili due diversi modi:

- Passaggio del contesto come argomento

  La maggior parte dei cmdlet di AzureRM consente di passare il contesto come parametro al cmdlet. È possibile passare un contesto a un processo in background come illustrato nell'esempio seguente:

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- Uso del contesto predefinito con il salvataggio automatico abilitato

  Se si è abilitato il **salvataggio automatico del contesto**, i processi in background usano automaticamente il contesto salvato predefinito.

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

Quando è necessario conoscere il risultato dell'attività in background, usare `Get-Job` per controllare lo stato del processo e `Wait-Job` per attenderne il completamento. Usare `Receive-Job` per acquisire o visualizzare l'output del processo in background. Per altre informazioni, vedere [About Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs) (Informazioni sui processi).

## <a name="creating-selecting-renaming-and-removing-contexts"></a>Creazione, selezione, ridenominazione e rimozione di contesti

Per creare un contesto, è necessario eseguire l'accesso ad Azure. Il cmdlet `Add-AzureRmAccount` (o il relativo alias `Login-AzureRmAccount`) imposta il contesto predefinito usato dai cmdlet di Azure PowerShell successivi e consente di accedere a qualsiasi sottoscrizione o tenant consentito dalle credenziali.

Per aggiungere un nuovo contesto dopo l'accesso, usare `Set-AzureRmContext` o il relativo alias `Select-AzureRmSubscription`.

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

L'esempio precedente aggiunge un nuovo contesto specificando come destinazione "Contoso Subscription 1" con le credenziali correnti. Il nuovo contesto è denominato "Contoso1". Se non si specifica un nome per il contesto, verrà usato un nome predefinito contenente l'ID account e l'ID sottoscrizione.

Per rinominare un contesto esistente, usare il cmdlet `Rename-AzureRmContext`, Ad esempio: 

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

Questo esempio rinomina il contesto denominato automaticamente `[user1@contoso.org; 123456-7890-1234-564321]` con il semplice nome "Contoso2". I cmdlet che gestiscono i contesti usano anche il completamento tramite tasto TAB, consentendo così di selezionare rapidamente il contesto.

Infine, per rimuovere un contesto usare il cmdlet `Remove-AzureRmContext`,  Ad esempio: 

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

Questo esempio annulla la memorizzazione del contesto denominato "Contoso2". È possibile ricreare questo contesto in seguito usando `Set-AzureRmContext`

## <a name="removing-credentials"></a>Rimozione delle credenziali

È possibile rimuovere tutte le credenziali e i contesti associati per un utente o un'entità servizio usando `Remove-AzureRmAccount` (denominato anche `Logout-AzureRmAccount`). Se eseguito senza parametri, il cmdlet `Remove-AzureRmAccount` rimuove tutte le credenziali e i contesti associati all'utente o all'entità servizio nel contesto corrente. È possibile passare un nome utente, un nome di entità servizio o un contesto per specificare come destinazione una determinata entità di sicurezza.

```azurepowershell-interactive
Remove-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a>Uso degli ambiti dei contesti

In alcuni casi può essere opportuno selezionare, modificare o rimuovere un contesto in una sessione di PowerShell senza influire su altre sessioni. Per modificare il comportamento predefinito dei cmdlet per il contesto, usare il parametro `Scope`. L'ambito `Process` esegue l'override del comportamento predefinito determinando l'applicazione solo per la sessione corrente. Al contrario, l'ambito `CurrentUser` modifica il contesto in tutte le sessioni, anziché solo nella sessione corrente.

Ad esempio, per modificare il contesto predefinito nella sessione di PowerShell corrente senza influire sulle altre finestre o sul contesto usato alla successiva apertura di una sessione, usare:

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a>Memorizzazione dell'impostazione di salvataggio automatico del contesto

L'impostazione di salvataggio automatico del contesto viene salvata nella directory di Azure PowerShell dell'utente (`%AppData%\Roaming\Windows Azure PowerShell`). Alcune tipologie di account computer potrebbero non avere accesso a tale directory. In tali scenari, è possibile usare la variabile di ambiente seguente:

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

Se è impostata su "true", il contesto viene salvato automaticamente. Se è impostata su "false", il contesto non viene salvato.

## <a name="changes-to-the-azurermprofile-module"></a>Modifiche apportate al modulo AzureRM.Profile

Nuovi cmdlet per la gestione del contesto

- [Enable-AzureRmContextAutosave][enable]: consente di salvare il contesto tra le sessioni di PowerShell.
  Qualsiasi modifica viene applicata al contesto globale.
- [Disable-AzureRmContextAutosave][disable]: disattiva il salvataggio automatico del contesto. Per ogni nuova sessione di PowerShell è necessario ripetere l'accesso.
- [Select-AzureRmContext][select]: seleziona un contesto come predefinito. Tutti i cmdlet successivi useranno le credenziali di questo contesto per l'autenticazione.
- [Remove-AzureRmAccount][remove-cred]: rimuove tutte le credenziali e i contesti associati a un account.
- [Remove-AzureRmContext][remove-context]: rimuove un contesto denominato.
- [Rename-AzureRmContext][rename]: rinomina un contesto esistente.

Modifiche apportate ai cmdlet per i profili esistenti

- [Add-AzureRmAccount][login]: consente di limitare l'ambito dell'accesso al processo o all'utente corrente,
  nonché di denominare il contesto predefinito dopo l'autenticazione.
- [Import-AzureRmContext][import]: consente di limitare l'ambito dell'accesso al processo o all'utente corrente.
- [Set-AzureRmContext][set-context]: consente di selezionare contesti denominati esistenti e limitare l'ambito delle modifiche al processo o all'utente corrente.

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Remove-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Add-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
