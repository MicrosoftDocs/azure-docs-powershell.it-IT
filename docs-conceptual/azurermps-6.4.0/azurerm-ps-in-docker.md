---
title: Eseguire Azure PowerShell in un contenitore Docker
description: Come eseguire Azure PowerShell in un contenitore Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 656c58fbb7cafb539736a0083d6aed1f46b7b98d
ms.sourcegitcommit: cb1fd248920d7efca67bd6c738a3b47206df7890
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/13/2018
ms.locfileid: "39024937"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>Eseguire Azure PowerShell in un contenitore Docker

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