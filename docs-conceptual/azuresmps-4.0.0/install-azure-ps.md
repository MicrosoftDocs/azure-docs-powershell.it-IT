---
title: Installare e configurare il modulo Gestione dei servizi di Azure PowerShell | Documenti di Microsoft
description: Come installare e configurare Azure PowerShell per il primo uso.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: a4911e72f687c07b31805c07fd23263a6b7f33b4
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2020
ms.locfileid: "75718798"
---
# <a name="installing-the-azure-powershell-service-management-module"></a>Installare il modulo Gestione dei servizi di Azure PowerShell

L'installazione di Azure PowerShell da [PowerShell Gallery](https://www.powershellgallery.com/) è il metodo preferito di installazione.

## <a name="step-1-install-powershellget"></a>Passaggio 1: installare PowerShellGet

L'installazione degli elementi da PowerShell Gallery richiede il modulo PowerShellGet. Assicurarsi di avere la versione appropriata di PowerShellGet e di soddisfare gli altri requisiti di sistema. Eseguire il comando seguente per determinare se PowerShellGet è installato nel sistema.

```powershell
Get-InstalledModule PowerShellGet -AllVersions | Select-Object Name,Version,Path
```

Verrà visualizzata una schermata simile all'output seguente:

```output
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Se PowerShellGet non è installato, vedere la sezione [Come ottenere PowerShellGet](#how-to-get-powershellget).

## <a name="step-2-install-azure-powershell"></a>Passaggio 2: Installare Azure PowerShell

Eseguire il comando seguente dalla console di Windows PowerShell come amministratore:

```powershell
Install-Module Azure
```

Il modulo Azure è un modulo di rollup per i cmdlet di Azure Resource Manager. Durante l'installazione del modulo AzureRM, qualsiasi modulo di Azure non installato precedentemente viene scaricato e installato da PowerShell Gallery.

Il modulo di Gestione dei servizi di Azure condivide le dipendenze con i moduli di Gestione risorse di Azure PowerShell. Se sono stati installati i moduli di Gestione risorse di Azure PowerShell, sarà necessario aggiungere il parametro `-AllowClobber` al comando di installazione. In questo modo le dipendenze condivise esistenti verranno aggiornate. Senza questo parametro, si verifica un errore di installazione del modulo.

```powershell
Install-Module Azure -AllowClobber
```

Dopo aver installato il modulo, è possibile importarlo eseguendo il comando seguente:

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a>Usare i cmdlet

Per iniziare a lavorare con i cmdlet di Gestione dei servizi di Azure, accedere al proprio account Azure. Per accedere al proprio account, eseguire il comando seguente:

```powershell
Add-AzureAccount
```

Dopo l'accesso ad Azure, Azure PowerShell crea un contesto per la sessione specificata. Tale contesto contiene l'ambiente Azure PowerShell, l'account, il tenant e la sottoscrizione che verranno usati per tutti i cmdlet della sessione. È ora possibile usare i moduli seguenti.

## <a name="azure-service-management-cmdlets"></a>Cmdlet di Gestione dei servizi di Azure

I moduli di Azure PowerShell vengono aggiornati di frequente. Se si nota che la guida dei cmdlet online include cmdlet o parametri non presenti nel modulo, scaricare e installare la versione più recente del modulo. Per conoscere la versione del modulo, digitare: `(Get-InstalledModule Azure).Version`.

Per gli script di esempio che consentono di automatizzare alcune delle attività comuni in Azure, vedere lo [Script Center di Windows Azure](http://www.windowsazure.com/documentation/scripts/).

Per informazioni generali sull'installazione, la formazione, l'uso e la personalizzazione di Windows PowerShell, vedere [Scripting con Windows PowerShell](https://go.microsoft.com/fwlink/p/?linkid=320210).

### <a name="how-to-get-powershellget"></a>Come ottenere PowerShellGet

|Versione sistema operativo|Istruzioni di installazione|
|---|---|
|Il sistema operativo è Windows 10 o Windows Server 2016|Integrato in Windows Management Framework (WMF) 5.0 incluso nel sistema operativo|
|Si vuole eseguire l'aggiornamento a PowerShell 5|[Installare la versione più recente di WMF](https://www.microsoft.com/download/details.aspx?id=54616)|
|È in esecuzione una versione di Windows con PowerShell 3 o 4|[Ottenere i moduli PackageManagement](https://go.microsoft.com/fwlink/?LinkID=746217)|

<div id="helpmechoose"/>

### <a name="checking-the-version-of-azure-powershell"></a>Controllo della versione di Azure PowerShell

Anche se si consiglia di eseguire l'aggiornamento alla versione più recente il prima possibile, alcune versioni di Azure PowerShell sono di supporto. Per determinare la versione di Azure PowerShell installata, eseguire `Get-InstalledModule Azure` dalla riga di comando.

```powershell
Get-InstalledModule Azure -AllVersions | Select-Object Name,Version,Path
```
