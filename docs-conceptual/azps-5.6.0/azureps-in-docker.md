---
title: Uso di Azure PowerShell in Docker
description: Come usare Azure PowerShell preinstallato in un'immagine docker.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 48935f15241ec965adf4c34d2c17aa670110585a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101881936"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="72229-103">Uso di Azure PowerShell in Docker</span><span class="sxs-lookup"><span data-stu-id="72229-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="72229-104">Si stanno pubblicando immagini Docker con Azure PowerShell preinstallata.</span><span class="sxs-lookup"><span data-stu-id="72229-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="72229-105">Questo articolo illustra come iniziare a usare Azure PowerShell nel contenitore docker.</span><span class="sxs-lookup"><span data-stu-id="72229-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="72229-106">Ricerca di immagini disponibili</span><span class="sxs-lookup"><span data-stu-id="72229-106">Finding available images</span></span>

<span data-ttu-id="72229-107">Le immagini rilasciate richiedono Docker 17,05 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="72229-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="72229-108">Si prevede anche che sia possibile eseguire Docker senza `sudo` diritti amministrativi locali o.</span><span class="sxs-lookup"><span data-stu-id="72229-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="72229-109">Per installare correttamente, seguire [le istruzioni][install] ufficiali di Docker `docker` .</span><span class="sxs-lookup"><span data-stu-id="72229-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="72229-110">L'immagine del contenitore più recente contiene la versione più recente di PowerShell e i moduli Azure PowerShell più recenti supportati con il modulo AZ.</span><span class="sxs-lookup"><span data-stu-id="72229-110">The latest container image contains the latest version of PowerShell and the latest Azure PowerShell modules supported with the Az module.</span></span>

<span data-ttu-id="72229-111">Per ogni nuova versione del modulo AZ si sta rilasciando un'immagine per i sistemi operativi seguenti:</span><span class="sxs-lookup"><span data-stu-id="72229-111">For each new release of the Az module we are releasing an image for the following operating systems:</span></span>

- <span data-ttu-id="72229-112">Ubuntu 18,04 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72229-112">Ubuntu 18.04 (default)</span></span>
- <span data-ttu-id="72229-113">Debian 9</span><span class="sxs-lookup"><span data-stu-id="72229-113">Debian 9</span></span>
- <span data-ttu-id="72229-114">CentOs 7</span><span class="sxs-lookup"><span data-stu-id="72229-114">CentOs 7</span></span>

<span data-ttu-id="72229-115">Un elenco completo delle immagini disponibili è reperibile nella pagina dell' [immagine Docker][az image] .</span><span class="sxs-lookup"><span data-stu-id="72229-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="72229-116">Uso di Azure PowerShell in un contenitore</span><span class="sxs-lookup"><span data-stu-id="72229-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="72229-117">I passaggi seguenti mostrano i comandi di Docker necessari per scaricare l'immagine e avviare una sessione interattiva di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="72229-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="72229-118">Scaricare l'immagine di Azure-PowerShell più recente.</span><span class="sxs-lookup"><span data-stu-id="72229-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="72229-119">Eseguire il contenitore Azure-PowerShell in modalità interattiva:</span><span class="sxs-lookup"><span data-stu-id="72229-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

<span data-ttu-id="72229-120">Per gli host Docker di Windows, è necessario abilitare la condivisione di file Docker per consentire la condivisione delle unità locali in Windows con i contenitori Linux.</span><span class="sxs-lookup"><span data-stu-id="72229-120">For Windows Docker hosts, you must enable Docker File Sharing to allow local drives on Windows to be shared with Linux containers.</span></span> <span data-ttu-id="72229-121">Per ulteriori informazioni, vedere [Introduzione a Docker per Windows][file-sharing].</span><span class="sxs-lookup"><span data-stu-id="72229-121">For more information see [Get started with Docker for Windows][file-sharing].</span></span>

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="72229-122">Eseguire il contenitore Azure-PowerShell in modo interattivo usando l'autenticazione host</span><span class="sxs-lookup"><span data-stu-id="72229-122">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="72229-123">Se è già stato installato Azure PowerShell nell'host di sistema Docker, è possibile che siano state memorizzate nella cache le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="72229-123">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="72229-124">Queste credenziali possono essere usate nella sessione di PowerShell in esecuzione nel contenitore docker.</span><span class="sxs-lookup"><span data-stu-id="72229-124">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="72229-125">Per impostazione predefinita, le credenziali memorizzate nella cache si trovano nella `$HOME/.Azure` directory dell'host.</span><span class="sxs-lookup"><span data-stu-id="72229-125">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="72229-126">Per accedere alle credenziali, il servizio Docker deve avere accesso a questo percorso.</span><span class="sxs-lookup"><span data-stu-id="72229-126">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="72229-127">Il comando seguente avvia il contenitore con la cache delle credenziali montata e avvia una sessione interattiva di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="72229-127">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="72229-128">Rimuovere l'immagine quando non è più necessaria</span><span class="sxs-lookup"><span data-stu-id="72229-128">Remove the image when no longer needed</span></span>

<span data-ttu-id="72229-129">Il comando seguente viene usato per eliminare il contenitore Docker quando non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="72229-129">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="72229-130">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="72229-130">Next steps</span></span>

<span data-ttu-id="72229-131">Per altre informazioni sui moduli di Azure PowerShell e sulle relative funzionalità, vedere [Introduzione ad Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="72229-131">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
