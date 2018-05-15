---
title: Installare e configurare Azure PowerShell | Microsoft Docs
description: Come installare e configurare Azure PowerShell per il primo uso.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: c6b8e2e8aa4afb9e58a2d357c4e51e19410a8188
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/08/2018
---
# <a name="install-and-configure-azure-powershell"></a>Installare e configurare Azure PowerShell

Questo articolo illustra i passaggi per installare i moduli di Azure PowerShell in ambiente Windows.
Se si intende usa Azure PowerShell in ambiente macOS o Linux, vedere l'articolo seguente: [Installare e configurare Azure PowerShell in macOS e Linux](install-azurermps-maclinux.md).

## <a name="system-requirements"></a>Requisiti di sistema

Con Azure PowerShell versione 6.0.0 è richiesta la versione 5.0 (o successiva) di PowerShell. Per eseguire un qualsiasi cmdlet, con le versioni precedenti di Azure PowerShell era richiesta _almeno_ la versione 3.0 di PowerShell. Per informazioni sull'aggiornamento a PowerShell 5.0, vedere [questa tabella](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

## <a name="step-1-install-powershellget"></a>Passaggio 1: installare PowerShellGet

L'installazione di Azure PowerShell da PowerShell Gallery è il metodo preferito di installazione.

L'installazione degli elementi da PowerShell Gallery richiede il modulo PowerShellGet. Assicurarsi di avere la versione appropriata di PowerShellGet e di soddisfare gli altri requisiti di sistema. Eseguire il comando seguente per determinare se PowerShellGet è installato nel sistema.

```powershell
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

Verrà visualizzata una schermata simile all'output seguente:

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

È necessario PowerShellGet versione 1.1.2.0 o successiva. Per aggiornare PowerShellGet, usare il comando seguente:

```powershell
Install-Module PowerShellGet -Force
```

Se PowerShellGet non è installato, vedere la sezione [Come ottenere PowerShellGet](#how-to-get-powershellget) di questo articolo.

> [!NOTE]
> L'uso di PowerShellGet richiede criteri di esecuzione che consentono di eseguire script. Per altre informazioni sui criteri di esecuzione di PowerShell, vedere [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies) (Informazioni sui criteri di esecuzione).

## <a name="step-2-install-azure-powershell"></a>Passaggio 2: Installare Azure PowerShell

L'installazione di Azure PowerShell da PowerShell Gallery richiede privilegi elevati. Eseguire il comando seguente da una sessione di PowerShell con privilegi elevati:

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet. La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

Rispondere "Sì" o "Yes to All" (Sì a tutti) per continuare l'installazione.

> [!NOTE]
> Se si dispone di una versione precedente alla versione 2.8.5.201 di NuGet, viene richiesto di scaricare e installare la versione più recente di NuGet.

Il modulo AzureRM è un modulo di rollup per i cmdlet di Azure Resource Manager. Durante l'installazione del modulo AzureRM, qualsiasi modulo di Azure PowerShell non installato precedentemente viene scaricato da PowerShell Gallery.

Se è installata una versione precedente di Azure PowerShell è probabile che venga visualizzato un errore. Per risolvere questo problema, vedere la sezione [Eseguire l'aggiornamento a una nuova versione di Azure PowerShell](#update-azps) di questo articolo.

## <a name="step-3-load-the-azurerm-module"></a>Passaggio 3: caricare il modulo AzureRM
Dopo aver installato il modulo, è necessario caricarlo nella sessione di PowerShell. Eseguire questa operazione in una normale sessione di PowerShell, senza privilegi elevati. I moduli vengono caricati usando il cmdlet `Import-Module`, come indicato di seguito:

```powershell
Import-Module -Name AzureRM
```

## <a name="next-steps"></a>Passaggi successivi

Per altre informazioni sull'uso di Azure PowerShell, vedere gli articoli seguenti:

* [Guida introduttiva ad Azure PowerShell](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a>Segnalazione di problemi e suggerimenti

Se si rilevano bug con lo strumento, segnalare un problema nella sezione [Issues](https://github.com/Azure/azure-powershell/issues) (Problemi) del repository GitHub. Per inserire commenti e suggerimenti dalla riga di comando, usare il cmdlet `Send-Feedback`.

## <a name="frequently-asked-questions"></a>Domande frequenti

### <a name="how-to-get-powershellget"></a>Come ottenere PowerShellGet

|Scenario|Istruzioni di installazione|
|---|---|
|Windows 10<br/>Windows Server 2016|Integrato in Windows Management Framework (WMF) 5.0 incluso nel sistema operativo|
|Si vuole eseguire l'aggiornamento a PowerShell 5|<ol><li>[Installare la versione più recente di WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li>Eseguire il comando seguente:<br/>```Install-Module PowerShellGet -Force```</li></ol>|
|È in esecuzione una versione di Windows con PowerShell 3 o 4|<ol><il>[Ottenere i moduli PackageManagement](http://go.microsoft.com/fwlink/?LinkID=746217)</il><li>Eseguire il comando seguente:<br/>```Install-Module PowerShellGet -Force```</li></ol>|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a>Controllo della versione di Azure PowerShell

Anche se si consiglia di eseguire l'aggiornamento alla versione più recente il prima possibile, alcune versioni di Azure PowerShell sono supportate. Per determinare la versione di Azure PowerShell installata, eseguire `Get-Module AzureRM` dalla riga di comando.

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a>Supporto per i metodi di distribuzione classica

In presenza di distribuzioni che usano il modello di distribuzione classico, è possibile installare la versione di Gestione dei servizi di Azure PowerShell. Per altre informazioni, vedere [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps) (Installare il modulo Gestione dei servizi di Azure PowerShell). I moduli Azure e AzureRM condividono dipendenze comuni. Se si usano sia moduli di Azure che quelli di AzureRM, è necessario installare la stessa versione di ogni pacchetto.

### <a id="update-azps"></a>Eseguire l'aggiornamento a una nuova versione di Azure PowerShell

Se è installata una versione precedente di Azure PowerShell che include il modulo Gestione dei servizi, è probabile che venga visualizzato l'errore seguente:

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

Come indicato nel messaggio di errore, è necessario usare il parametro -AllowClobber per installare il modulo. Usare il comando seguente:

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

Per altre informazioni, vedere l'argomento relativo alla guida per [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).

### <a name="installing-module-versions-side-by-side"></a>Installazione di versioni del modulo affiancate

Il metodo di installazione PowerShellGet è l'unico che supporta l'installazione di più versioni. Ad esempio, è possibile che molti script siano stati scritti con una versione precedente di Azure PowerShell che non si è in grado di aggiornare per mancanza di tempo o risorse. I comandi seguenti mostrano come installare più versioni di Azure PowerShell:

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

Solo una versione del modulo può essere caricata in una sessione di PowerShell. È necessario aprire una nuova finestra di PowerShell e usare `Import-Module` per importare una versione specifica dei cmdlet di AzureRM:

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> La versione 2.1.0 e la versione 1.2.6 sono le prime versioni del modulo progettate per l'installazione e l'uso affiancati. Durante il caricamento di una versione precedente di Azure PowerShell, vengono caricate versioni incompatibili del modulo **AzureRM.Profile**. Di conseguenza, i cmdlet richiedono di effettuare l'accesso ogni volta che si esegue un cmdlet.

### <a name="other-installation-methods"></a>Altri metodi di installazione

Per informazioni sull'installazione con l'Installazione guidata piattaforma Web o il pacchetto MSI, vedere [Other installation methods](other-install.md) (Altri metodi di installazione)
