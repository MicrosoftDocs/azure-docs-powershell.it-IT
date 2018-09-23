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
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="d41e5-103">Eseguire Azure PowerShell in un contenitore Docker</span><span class="sxs-lookup"><span data-stu-id="d41e5-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="d41e5-104">Microsoft pubblica immagini Docker con Azure PowerShell preinstallato.</span><span class="sxs-lookup"><span data-stu-id="d41e5-104">Microsoft publishes Docker images with Azure PowerShell pre-installed.</span></span> <span data-ttu-id="d41e5-105">Queste immagini consentono di provare a usare Azure PowerShell o di eseguirlo in un ambiente isolato.</span><span class="sxs-lookup"><span data-stu-id="d41e5-105">These images allow for experimenting with Azure PowerShell or running it in an isolated environment.</span></span> <span data-ttu-id="d41e5-106">Sono disponibili immagini che eseguono sia PowerShell Core che PowerShell 5.</span><span class="sxs-lookup"><span data-stu-id="d41e5-106">There are images running both PowerShell Core and PowerShell 5.</span></span> 

| <span data-ttu-id="d41e5-107">Environment</span><span class="sxs-lookup"><span data-stu-id="d41e5-107">Environment</span></span> | <span data-ttu-id="d41e5-108">Immagine Docker</span><span class="sxs-lookup"><span data-stu-id="d41e5-108">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="d41e5-109">PowerShell in Windows</span><span class="sxs-lookup"><span data-stu-id="d41e5-109">PowerShell on Windows</span></span> | [<span data-ttu-id="d41e5-110">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="d41e5-110">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="d41e5-111">PowerShell Core in Windows</span><span class="sxs-lookup"><span data-stu-id="d41e5-111">PowerShell Core on Windows</span></span> | [<span data-ttu-id="d41e5-112">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="d41e5-112">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="d41e5-113">PowerShell Core in Linux</span><span class="sxs-lookup"><span data-stu-id="d41e5-113">PowerShell Core on Linux</span></span> | [<span data-ttu-id="d41e5-114">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="d41e5-114">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="d41e5-115">Per eseguire uno di questi contenitori, usare `docker run -it $ImageName` per ottenere un terminale interattivo.</span><span class="sxs-lookup"><span data-stu-id="d41e5-115">To run any of these containers, use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="d41e5-116">Ad esempio, per eseguire un contenitore Linux con PowerShell Core:</span><span class="sxs-lookup"><span data-stu-id="d41e5-116">For example, to run a Linux container with PowerShell Core:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="d41e5-117">Per eseguire un contenitore Windows in Docker, il sistema operativo host deve essere Windows e Docker deve essere impostato per l'esecuzione dei contenitori Windows.</span><span class="sxs-lookup"><span data-stu-id="d41e5-117">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="d41e5-118">Per informazioni su come passare da un ambiente Windows a un ambiente Linux in Docker, vedere il documento Docker [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) (Passare dai contenitori Windows ai contenitori Linux).</span><span class="sxs-lookup"><span data-stu-id="d41e5-118">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="d41e5-119">Usare un contenitore PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="d41e5-119">Use a PowerShell Core container</span></span>

<span data-ttu-id="d41e5-120">I contenitori PowerShell Core vengono forniti con PowerShell Core v6 e il modulo `AzureRM.NetCore`.</span><span class="sxs-lookup"><span data-stu-id="d41e5-120">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="d41e5-121">Eseguire il cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module) e quindi accedere con l'account Azure:</span><span class="sxs-lookup"><span data-stu-id="d41e5-121">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="d41e5-122">Usare il contenitore di Windows con PowerShell</span><span class="sxs-lookup"><span data-stu-id="d41e5-122">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="d41e5-123">Il contenitore di Windows ha il modulo `AzureRM` preinstallato.</span><span class="sxs-lookup"><span data-stu-id="d41e5-123">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="d41e5-124">Eseguire il cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module) e quindi accedere con l'account Azure:</span><span class="sxs-lookup"><span data-stu-id="d41e5-124">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
