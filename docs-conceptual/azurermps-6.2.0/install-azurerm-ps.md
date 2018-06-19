---
title: Installare Azure PowerShell con PowerShellGet
description: Come installare Azure PowerShell con PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323102"
---
# <a name="install-azure-powershell-with-powershellget"></a>Installare Azure PowerShell con PowerShellGet

Questo articolo illustra l'installazione dei moduli di Azure PowerShell in ambiente Windows con PowerShellGet.  Si tratta della modalità di installazione ideale di Azure PowerShell, ma se si preferisce usare Installazione guidata piattaforma Web o il pacchetto MSI, vedere [Altri metodi di installazione ](other-install.md).

Se si intende usa Azure PowerShell in ambiente macOS o Linux, vedere l'articolo seguente: [Installare e configurare Azure PowerShell in macOS e Linux](install-azurermps-maclinux.md).

## <a name="system-requirements"></a>Requisiti di sistema

La versione 6.1.0 di Azure PowerShell richiede la versione 5.0 (o superiore) di PowerShell. Per informazioni sull'aggiornamento a PowerShell 5.0, vedere [Aggiornamento di Windows PowerShell esistente](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

PowerShellGet è automaticamente incluso come componente di PowerShell 5.0.

## <a name="install-or-update-the-azure-powershell-module"></a>Installare o aggiornare il modulo Azure PowerShell

L'installazione di Azure PowerShell da PowerShell Gallery richiede privilegi elevati. Eseguire il comando seguente da una sessione di PowerShell con privilegi elevati:

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> Questo comando aggiorna qualsiasi installazione esistente di Azure PowerShell nel sistema. Se è necessario installare più versioni, vedere la risposta alla domanda frequente [È possibile installare più versioni di Azure PowerShell?](#multiple-versions)

Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet. La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Rispondere "Sì" o "Yes to All" (Sì a tutti) per continuare l'installazione.

> [!NOTE]
> Se si dispone di una versione precedente alla versione 2.8.5.201 di NuGet, viene richiesto di scaricare e installare la versione più recente di NuGet.

Il modulo AzureRM è un modulo di rollup per i cmdlet di Azure Resource Manager. Durante l'installazione del modulo AzureRM, qualsiasi modulo di Azure PowerShell non installato precedentemente viene scaricato da PowerShell Gallery.

## <a name="load-the-azure-powershell-module"></a>Caricare il modulo Azure PowerShell

Dopo aver installato il modulo, è necessario caricarlo nella sessione di PowerShell. Eseguire questa operazione in una normale sessione di PowerShell, senza privilegi elevati. I moduli vengono caricati usando il cmdlet `Import-Module`, come indicato di seguito:

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a>Segnalazione di problemi e suggerimenti

Se si verificano bug con lo strumento, [registrare un problema in GitHub](https://github.com/Azure/azure-powershell/issues). Per inserire commenti e suggerimenti dalla riga di comando, usare il cmdlet `Send-Feedback`.

## <a name="next-steps"></a>Passaggi successivi

Per altre informazioni sull'uso di Azure PowerShell, vedere gli articoli seguenti:

* [Guida introduttiva ad Azure PowerShell](get-started-azureps.md)

## <a name="frequently-asked-questions"></a>Domande frequenti

### <a id="helpmechoose"></a>Come si verifica la versione di Azure PowerShell?

Anche se si consiglia di eseguire l'aggiornamento alla versione più recente il prima possibile, alcune versioni di Azure PowerShell sono supportate. Per determinare la versione di Azure PowerShell installata, eseguire `Get-Module AzureRM` dalla riga di comando.

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a>È possibile usare Azure PowerShell per le distribuzioni classiche di Azure?

In presenza di distribuzioni che usano il modello di distribuzione classico, è possibile installare la versione di Gestione dei servizi di Azure PowerShell. Per altre informazioni, vedere [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps) (Installare il modulo Gestione dei servizi di Azure PowerShell). I moduli Azure e AzureRM condividono dipendenze comuni. Se si usano sia moduli di Azure che quelli di AzureRM, è necessario installare la stessa versione di ogni pacchetto.

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><a name="multiple-versions"/>È possibile installare più versioni di Azure PowerShell?

PowerShellGet è l'unico metodo di installazione che supporta più versioni. Per installare più versioni, è possibile aggiungere il parametro `-RequiredVersion` al cmdlet `Install-Module`. Per installare ad esempio le versioni 6.1.0 e 1.2.9:

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

Solo una versione del modulo può essere caricata in una sessione di PowerShell. È necessario aprire una nuova finestra di PowerShell e usare `Import-Module` per importare una versione specifica del modulo Azure PowerShell.

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> La versione 2.1.0 e la versione 1.2.6 sono le prime versioni del modulo progettate per l'installazione e l'uso affiancati. Durante il caricamento di una versione precedente di Azure PowerShell, vengono caricate versioni incompatibili del modulo **AzureRM.Profile**. Di conseguenza, i cmdlet richiedono di effettuare l'accesso ogni volta che si esegue un cmdlet.
