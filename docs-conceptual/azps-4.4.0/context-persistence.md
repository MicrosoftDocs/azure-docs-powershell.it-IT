---
title: Contesti e credenziali di accesso di Azure
description: Informazioni su come riutilizzare le credenziali di Azure e altre informazioni in più sessioni di PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: c79d1d634d5b76b2c6ab6b6ab309c2d49f9f7678
ms.sourcegitcommit: 23e5b2b0751777ef0a5ca74e40c7772653e339a3
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/14/2020
ms.locfileid: "86382067"
---
# <a name="azure-powershell-context-objects"></a>Oggetti contesto di Azure PowerShell

Azure PowerShell usa gli _oggetti contesto di Azure PowerShell_ (contesti di Azure) per memorizzare informazioni su sottoscrizioni e autenticazione. Nel caso di più sottoscrizioni, i contesti di Azure consentono di selezionare quella in cui eseguire i cmdlet di Azure PowerShell. I contesti di Azure possono anche essere usati per archiviare informazioni di accesso tra più sessioni di PowerShell e per eseguire attività in background.

Questo articolo riguarda i contesti di Azure, non la gestione di sottoscrizioni o account. Per informazioni su gestione degli utenti, sottoscrizioni, tenant o account, vedere la documentazione di [Azure Active Directory](/azure/active-directory). Per informazioni sull'uso di contesti per l'esecuzione in background di attività parallele, vedere [Usare i cmdlet di Azure PowerShell in processi di PowerShell](using-psjobs.md) dopo aver acquisito familiarità con i contesti di Azure.

## <a name="overview-of-azure-context-objects"></a>Panoramica degli oggetti contesto di Azure

I contesti di Azure sono oggetti di PowerShell che rappresentano la sottoscrizione attiva in cui eseguire i comandi e le informazioni di autenticazione necessarie per connettere Azure al cloud. Con i contesti di Azure, non è necessario ripetere l'autenticazione dell'account in Azure PowerShell ogni volta che si cambia sottoscrizione. Un contesto di Azure è costituito da:

* L'_account_ usato per accedere ad Azure con [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount). I contesti di Azure considerano gli utenti, gli ID applicazione e le entità servizio allo stesso modo dal punto di vista di un account.
* La _sottoscrizione_ attiva, un contratto di servizi stipulato con Microsoft per la creazione e l'esecuzione delle risorse di Azure, che sono associate a un _tenant_. I tenant vengono spesso citati come _organizzazioni_ nella documentazione e durante l'uso di Active Directory.
* Un riferimento a una _cache del token_, un token di autenticazione archiviato per l'accesso al cloud di Azure. La posizione di archiviazione e la durata del periodo di conservazione di tale token vengono definite dalle [impostazioni di salvataggio automatico dei contesti](#save-azure-contexts-across-powershell-sessions).

Per altre informazioni, vedere [Terminologia di Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis#terminology). I token di autenticazione usati dai contesti di Azure sono uguali ad altri token archiviati che fanno parte di una sessione persistente. 

Quando si accede con `Connect-AzAccount`, viene creato almeno un contesto di Azure per la sottoscrizione predefinita. L'oggetto restituito da `Connect-AzAccount` è il contesto di Azure predefinito usato per il resto della sessione di PowerShell.

## <a name="get-azure-contexts"></a>Ottenere i contesti di Azure

I contesti di Azure disponibili vengono recuperati con il cmdlet [Get-AzContext](/powershell/module/az.accounts/get-azcontext). Per elencare tutti i contesti disponibili, usare `-ListAvailable`:

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

Oppure ottenere un contesto per nome:

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

I nomi dei contesti possono essere diversi dal nome della sottoscrizione associata.

> [!IMPORTANT]
> I contesti di Azure disponibili __non__ corrispondono sempre alle sottoscrizioni disponibili, ma rappresentano solo informazioni archiviate in locale. Per ottenere le sottoscrizioni, usare il cmdlet [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0).

## <a name="create-a-new-azure-context-from-subscription-information"></a>Creare un nuovo contesto di Azure dalle informazioni della sottoscrizione

Il cmdlet [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) consente sia di creare nuovi contesti di Azure sia di impostarli come contesto attivo.
Il modo più semplice per creare un nuovo contesto di Azure consiste nell'usare le informazioni della sottoscrizione esistenti. Il cmdlet è progettato per configurare un nuovo contesto di Azure con l'oggetto output di `Get-AzSubscription` come valore della pipeline:

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

In alternativa, specificare il nome o l'ID della sottoscrizione oppure l'ID tenant, se necessario:

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

Se l'argomento `-Name` viene omesso, per il nome del contesto vengono usati il nome e l'ID della sottoscrizione, nel formato `Subscription Name (subscription-id)`.

## <a name="change-the-active-azure-context"></a>Cambiare il contesto di Azure attivo

Per cambiare il contesto di Azure attivo, è possibile usare sia `Set-AzContext` sia [Select-AzContext](/powershell/module/az.accounts/set-azcontext). Come descritto nella sezione [Creare un nuovo contesto di Azure](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` crea un nuovo contesto di Azure per una sottoscrizione, se non ne esiste già uno, e quindi imposta tale contesto come quello attivo.

`Select-AzContext` deve essere usato solo con i contesti di Azure esistenti e funziona in modo simile all'uso di `Set-AzContext -Context`, ma è destinato all'uso con le pipeline:

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

Analogamente a molti altri comandi di gestione di account e contesti disponibili in Azure PowerShell, `Set-AzContext` e `Select-AzContext` supportano l'argomento `-Scope`, quindi è possibile controllare il periodo di tempo in cui il contesto è attivo. `-Scope` consente di cambiare il contesto attivo di una singola sessione senza cambiare l'impostazione predefinita:

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

Per evitare di cambiare contesto per un'intera sessione di PowerShell, tutti i comandi di Azure PowerShell possono essere eseguiti in uno specifico contesto con l'argomento `-AzContext`:

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

L'altro uso principale dei contesti con i cmdlet di Azure PowerShell consiste nell'esecuzione di comandi in background. Per altre informazioni sull'esecuzione di processi di PowerShell con Azure PowerShell, vedere [Eseguire i cmdlet di Azure PowerShell nei processi di PowerShell](using-psjobs.md).

## <a name="save-azure-contexts-across-powershell-sessions"></a>Salvare i contesti di Azure tra sessioni di PowerShell

Per impostazione predefinita, i contesti di Azure vengono salvati per l'uso tra sessioni di PowerShell. È possibile cambiare questo comportamento nei modi seguenti:

* Accedere usando `-Scope Process` con `Connect-AzAccount`.

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  Il contesto di Azure restituito come parte di questo accesso è valido _solo_ per la sessione corrente e non verrà salvato automaticamente, indipendentemente dall'impostazione di salvataggio automatico dei contesti di Azure PowerShell.
* Disabilitare il salvataggio automatico dei contesti di Azure PowerShell con il cmdlet [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave).
  La disabilitazione del salvataggio automatico __non__ comporta la cancellazione di eventuali token archiviati. Per informazioni su come cancellare le informazioni dei contesti di Azure, vedere [Rimuovere contesti e credenziali di Azure](#remove-azure-contexts-and-stored-credentials).
* L'abilitazione esplicita del salvataggio automatico dei contesti di Azure può essere impostata con il cmdlet [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave). Con il salvataggio automatico abilitato, tutti i contesti dell'utente vengono archiviati in locale per sessioni di PowerShell successive.
* Salvare manualmente i contesti con [Save-AzContext](/powershell/module/az.accounts/save-azcontext) per usarli in future sessioni di PowerShell, dove possono essere caricati con [Import-AzContext](/powershell/module/az.accounts/import-azcontext):

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> La disabilitazione del salvataggio automatico dei contesti __non__ comporta la cancellazione delle informazioni salvate dei contesti archiviati. Per rimuovere le informazioni archiviate, usare il cmdlet [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext). Per altre informazioni sulla rimozione dei contesti salvati, vedere [Rimuovere contesti e credenziali](#remove-azure-contexts-and-stored-credentials).

Ognuno di questi comandi supporta il parametro `-Scope`, che accetta un valore `Process` per applicarlo solo al processo corrente in esecuzione. Ad esempio, per assicurarsi che i contesti appena creati non vengano salvati dopo l'uscita da una sessione di PowerShell:

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

Le informazioni dei contesti e i token vengono archiviati nella directory `$env:USERPROFILE\.Azure` in Windows e in `$HOME/.Azure` in altre piattaforme. Le informazioni sensibili, come gli ID sottoscrizione e gli ID tenant, possono essere comunque esposte nelle informazioni archiviate, tramite log o contesti salvati. Per informazioni su come cancellare le informazioni archiviate, vedere la sezione [Rimuovere contesti e credenziali](#remove-azure-contexts-and-stored-credentials).

## <a name="remove-azure-contexts-and-stored-credentials"></a>Rimuovere contesti e credenziali archiviate di Azure

Per cancellare contesti e credenziali di Azure:

* Disconnettersi da un account con [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).
  È possibile disconnettersi da qualsiasi account in base ad account o contesto:

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account 
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  Con la disconnessione vengono sempre rimossi i token di autenticazione e vengono cancellati i contesti salvati associati all'utente o al contesto disconnesso.
* Usare [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext). Questo cmdlet è garantito per rimuovere sempre i contesti e i token di autenticazione archiviati e consente anche di disconnettersi.
* Rimuovere un contesto con [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):
  
  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  Se si rimuove il contesto attivo, si verrà disconnessi da Azure e sarà necessario ripetere l'autenticazione con `Connect-AzAccount`.

## <a name="see-also"></a>Vedere anche

* [Eseguire i cmdlet di Azure PowerShell nei processi di PowerShell](using-psjobs.md)
* [Terminologia di Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [Informazioni di riferimento su Az.Accounts](/powershell/module/az.accounts)
