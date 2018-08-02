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
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/02/2018
ms.locfileid: "39367906"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="e6f3d-103">Eseguire Azure PowerShell in un contenitore Docker</span><span class="sxs-lookup"><span data-stu-id="e6f3d-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="e6f3d-104">È disponibile un set di immagini Docker preconfigurate con Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e6f3d-104">There are a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="e6f3d-105">Sono disponibili due tipi di contenitori: quelli che eseguono la versione tradizionale di PowerShell in Windows e un contenitore che esegue PowerShell Core in Windows o Linux.</span><span class="sxs-lookup"><span data-stu-id="e6f3d-105">Two types of containers are available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="e6f3d-106">Environment</span><span class="sxs-lookup"><span data-stu-id="e6f3d-106">Environment</span></span> | <span data-ttu-id="e6f3d-107">Immagine Docker</span><span class="sxs-lookup"><span data-stu-id="e6f3d-107">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="e6f3d-108">PowerShell in Windows</span><span class="sxs-lookup"><span data-stu-id="e6f3d-108">PowerShell on Windows</span></span> | [<span data-ttu-id="e6f3d-109">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="e6f3d-109">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="e6f3d-110">PowerShell Core in Windows</span><span class="sxs-lookup"><span data-stu-id="e6f3d-110">PowerShell Core on Windows</span></span> | [<span data-ttu-id="e6f3d-111">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="e6f3d-111">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="e6f3d-112">PowerShell Core in Linux</span><span class="sxs-lookup"><span data-stu-id="e6f3d-112">PowerShell Core on Linux</span></span> | [<span data-ttu-id="e6f3d-113">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="e6f3d-113">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="e6f3d-114">Per eseguire uno di questi contenitori, usare `docker run -it $ImageName` per ottenere un terminale interattivo.</span><span class="sxs-lookup"><span data-stu-id="e6f3d-114">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="e6f3d-115">Ad esempio, per eseguire PowerShell Core in un contenitore Linux usare:</span><span class="sxs-lookup"><span data-stu-id="e6f3d-115">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="e6f3d-116">Per eseguire un contenitore Windows in Docker, il sistema operativo host deve essere Windows e Docker deve essere impostato per l'esecuzione dei contenitori Windows.</span><span class="sxs-lookup"><span data-stu-id="e6f3d-116">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="e6f3d-117">Per informazioni su come passare da un ambiente Windows a un ambiente Linux in Docker, vedere il documento Docker [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) (Passare dai contenitori Windows ai contenitori Linux).</span><span class="sxs-lookup"><span data-stu-id="e6f3d-117">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="e6f3d-118">Usare un contenitore PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="e6f3d-118">Use a PowerShell Core container</span></span>

<span data-ttu-id="e6f3d-119">I contenitori PowerShell Core vengono forniti con PowerShell Core v6 e il modulo `AzureRM.NetCore`.</span><span class="sxs-lookup"><span data-stu-id="e6f3d-119">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="e6f3d-120">Eseguire il cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module) e quindi accedere con l'account Azure:</span><span class="sxs-lookup"><span data-stu-id="e6f3d-120">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="e6f3d-121">Usare il contenitore di Windows con PowerShell</span><span class="sxs-lookup"><span data-stu-id="e6f3d-121">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="e6f3d-122">Il contenitore di Windows ha il modulo `AzureRM` preinstallato.</span><span class="sxs-lookup"><span data-stu-id="e6f3d-122">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="e6f3d-123">Eseguire il cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module) e quindi accedere con l'account Azure:</span><span class="sxs-lookup"><span data-stu-id="e6f3d-123">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```