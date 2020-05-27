---
title: Altre modalità di installazione e configurazione di Azure PowerShell | Microsoft Docs
description: Come installare Azure PowerShell usando il pacchetto MSI o l'Installazione guidata piattaforma Web.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 3f8963c98b26f971c1259dc89d5da1f35ce3015a
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386698"
---
# <a name="other-installation-methods"></a>Altri metodi di installazione

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Per Azure PowerShell sono disponibili più metodi di installazione. L'uso di PowerShellGet con PowerShell Gallery è il metodo preferito. Azure PowerShell può essere installato in Windows usando l'Installazione guidata piattaforma Web (WebPI) o il file MSI disponibile su GitHub.

## <a name="install-on-windows-using-the-web-platform-installer"></a>Eseguire l'installazione in Windows con l'Installazione guidata piattaforma Web

L'installazione della versione più recente di Azure PowerShell dall'Installazione guidata piattaforma Web è uguale a quella per le versioni precedenti.
Scaricare il [pacchetto per l'Installazione guidata piattaforma Web di Azure PowerShell](https://aka.ms/webpi-azps) e avviare l'installazione.

> [!NOTE]
> Se sono stati installati precedentemente moduli Azure da PowerShell Gallery, il programma di installazione li rimuoverà automaticamente. Ciò semplifica l'ambiente, garantendo l'installazione di una sola versione di Azure PowerShell. Tuttavia, esistono scenari in cui sono necessarie più versioni installate nello stesso momento.
>
> I moduli di PowerShell Gallery consentono di installare i moduli in `$env:ProgramFiles\WindowsPowerShell\Modules`. Al contrario, il programma di Installazione guidata piattaforma Web installerà i moduli di Azure in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.
>
> Se si verifica un errore durante l'installazione, è possibile rimuovere manualmente le cartelle di Azure\* nella cartella `$env:ProgramFiles\WindowsPowerShell\Modules` e ripetere l'installazione.

Al termine dell'installazione, l'impostazione `$env:PSModulePath` includerà le directory contenenti i cmdlet di Azure PowerShell. È possibile usare il comando seguente per verificare che Azure PowerShell sia installato correttamente.

```powershell-interactive
# To make sure the Azure PowerShell module is available after you install
Get-InstalledModule -Name AzureRM -AllVersions | Select-Object Name, Version, Path
```

> [!NOTE]
> Durante l'uso dell'Installazione guidata piattaforma Web è possibile che si verifichi un problema noto. Se il computer richiede il riavvio a causa di aggiornamenti di sistema o di altre installazioni, gli aggiornamenti di `$env:PSModulePath` potrebbero non includere il percorso in cui è installato Azure PowerShell.

Quando si tenta di caricare o eseguire i cmdlet dopo l'installazione, è possibile ricevere il messaggio di errore seguente:

```output
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

Questo errore può essere corretto riavviando il computer o importando il modulo usando il percorso completo. Ad esempio:

```powershell-interactive
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a>Eseguire l'installazione in Windows tramite il pacchetto MSI

Azure PowerShell può essere installato usando il file MSI disponibile su [GitHub](https://github.com/Azure/azure-powershell/releases/latest). Se sono state installate versioni precedenti dei moduli di Azure, il programma di installazione le rimuove automaticamente. Il pacchetto MSI consente di installare i moduli in `$env:ProgramFiles\WindowsPowerShell\Modules`, ma non crea cartelle specifiche per la versione.

