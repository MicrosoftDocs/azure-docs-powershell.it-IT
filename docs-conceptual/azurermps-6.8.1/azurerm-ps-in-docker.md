---
title: Eseguire Azure PowerShell in un contenitore Docker
description: Come eseguire Azure PowerShell in un contenitore Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 0ed8f50abbcb2aa00192196f19004446dc696b5d
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/20/2018
ms.locfileid: "46304013"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>Eseguire Azure PowerShell in un contenitore Docker

Microsoft pubblica immagini Docker con Azure PowerShell preinstallato. Queste immagini consentono di provare a usare Azure PowerShell o di eseguirlo in un ambiente isolato. Sono disponibili immagini che eseguono sia PowerShell Core che PowerShell 5. 

| Environment | Immagine Docker |
|-------------|--------------|
| PowerShell in Windows | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| PowerShell Core in Windows | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| PowerShell Core in Linux | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Per eseguire uno di questi contenitori, usare `docker run -it $ImageName` per ottenere un terminale interattivo. Ad esempio, per eseguire un contenitore Linux con PowerShell Core:

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> Per eseguire un contenitore Windows in Docker, il sistema operativo host deve essere Windows e Docker deve essere impostato per l'esecuzione dei contenitori Windows. Per informazioni su come passare da un ambiente Windows a un ambiente Linux in Docker, vedere il documento Docker [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) (Passare dai contenitori Windows ai contenitori Linux).

## <a name="use-a-powershell-core-container"></a>Usare un contenitore PowerShell Core

I contenitori PowerShell Core vengono forniti con PowerShell Core v6 e il modulo `AzureRM.NetCore`. Eseguire il cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module) e quindi accedere con l'account Azure:

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a>Usare il contenitore di Windows con PowerShell

Il contenitore di Windows ha il modulo `AzureRM` preinstallato. Eseguire il cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module) e quindi accedere con l'account Azure:

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
