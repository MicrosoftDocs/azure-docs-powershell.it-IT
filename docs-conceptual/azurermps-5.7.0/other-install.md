---
title: Altre modalità di installazione di Azure PowerShell
description: Come installare Azure PowerShell usando il pacchetto MSI o l'Installazione guidata piattaforma Web.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 0919583d9cb05a75fae3b812eed84109be8b28aa
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323272"
---
# <a name="other-installation-methods"></a>Altri metodi di installazione

Questo articolo illustra come installare Azure PowerShell usando un pacchetto MSI o Installazione guidata piattaforma Web (WebPI). Azure PowerShell può essere eseguito anche dall'interno di un contenitore Docker. Usare questi metodi di installazione solo se sono necessari per il sistema. Il modo canonico per installare Azure PowerShell è tramite PowerShellGet. Per istruzioni sull'uso di PowerShellGet per installare Azure PowerShell, vedere [Installare Azure PowerShell con PowerShellGet ](install-azurerm-ps.md).

Per l'installazione in ambienti Linux o macOS, vedere [Installare Azure PowerShell in macOS o Linux ](install-azurermps-maclinux.md).

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>Eseguire l'installazione o l'aggiornamento in Windows con Installazione guidata piattaforma Web

L'installazione della versione più recente di Azure PowerShell dall'Installazione guidata piattaforma Web è uguale a quella per le versioni precedenti.
Scaricare il [pacchetto per l'Installazione guidata piattaforma Web di Azure PowerShell](http://aka.ms/webpi-azps) e avviare l'installazione.

> [!NOTE]
> Se sono stati installati precedentemente moduli Azure da PowerShell Gallery, il programma di installazione li rimuoverà automaticamente. Ciò semplifica l'ambiente, garantendo l'installazione di una sola versione di Azure PowerShell. Tuttavia, esistono scenari in cui sono necessarie più versioni installate nello stesso momento.
>
> I moduli di PowerShell Gallery consentono di installare i moduli in `$env:ProgramFiles\WindowsPowerShell\Modules`. Al contrario, il programma di Installazione guidata piattaforma Web installerà i moduli di Azure in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.
>
> Se si verifica un errore durante l'installazione, è possibile rimuovere manualmente le cartelle `Azure*` dalla cartella `$env:ProgramFiles\WindowsPowerShell\Modules` e riprovare l'installazione.

Al termine dell'installazione, l'impostazione `$env:PSModulePath` includerà le directory contenenti i cmdlet di Azure PowerShell. È possibile usare il comando seguente per verificare che Azure PowerShell sia installato correttamente:

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> Durante l'uso dell'Installazione guidata piattaforma Web è possibile che si verifichi un problema noto. Se il computer richiede il riavvio a causa di aggiornamenti di sistema o di altre installazioni, gli aggiornamenti di `$env:PSModulePath` potrebbero non includere il percorso in cui è installato Azure PowerShell.

Quando si tenta di caricare o eseguire i cmdlet dopo l'installazione, è possibile ricevere il messaggio di errore seguente:

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

Questo errore può essere corretto riavviando il computer o importando il modulo usando il percorso completo.

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Eseguire l'installazione o l'aggiornamento in Windows tramite il pacchetto MSI

Azure PowerShell può essere installato usando il file MSI disponibile su [GitHub](https://aka.ms/azps-release). Se sono state installate versioni precedenti dei moduli di Azure, il programma di installazione le rimuove automaticamente. Il pacchetto MSI consente di installare i moduli in `$env:ProgramFiles\WindowsPowerShell\Modules`, ma non crea cartelle specifiche per la versione.

## <a name="run-in-a-docker-container"></a>Eseguire in un contenitore Docker

È disponibile un set di immagini Docker preconfigurate con Azure PowerShell. Sono disponibili due tipi di contenitori: quelli che eseguono la versione tradizionale di PowerShell in Windows e un contenitore che esegue PowerShell Core in Windows o Linux.

| Environment | Immagine Docker |
|-------------|--------------|
| PowerShell in Windows | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| PowerShell Core in Windows | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| PowerShell Core in Linux | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Per eseguire uno di questi contenitori, usare `docker run -it $ImageName` per ottenere un terminale interattivo. Ad esempio, per eseguire PowerShell Core in un contenitore Linux usare:

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> Per eseguire un contenitore Windows in Docker, il sistema operativo host deve essere Windows e Docker deve essere impostato per l'esecuzione dei contenitori Windows. Per informazioni su come passare da un ambiente Windows a un ambiente Linux in Docker, vedere il documento Docker [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) (Passare dai contenitori Windows ai contenitori Linux).