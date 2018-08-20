---
title: Eseguire Azure PowerShell in un contenitore Docker
description: Come eseguire Azure PowerShell in un contenitore Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 27ac176d8bd0b142b7740b2ba6793edb500a8af3
ms.sourcegitcommit: 7df99dc139e93a8a4e6d5b1a27968857588d75dd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/16/2018
ms.locfileid: "40106552"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>Eseguire Azure PowerShell in un contenitore Docker

Per semplificare l'esecuzione di Azure PowerShell in ambienti portatili, Microsoft pubblica le immagini Docker con Azure PowerShell preinstallato. Queste immagini offrono un guest Linux con PowerShell Core o un guest Windows con PowerShell Core o PowerShell 5.

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
