---
title: Uso di Azure PowerShell in Docker
description: Informazioni su come usare Azure PowerShell preinstallato in un'immagine Docker.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2b487abeecbffa6cd8b7b64276ab301619348385
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241458"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="8d3f9-103">Uso di Azure PowerShell in Docker</span><span class="sxs-lookup"><span data-stu-id="8d3f9-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="8d3f9-104">Nelle immagini Docker pubblicate è ora incluso Azure PowerShell preinstallato.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="8d3f9-105">Questo articolo illustra come iniziare a usare Azure PowerShell nel contenitore Docker.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="8d3f9-106">Individuazione delle immagini disponibili</span><span class="sxs-lookup"><span data-stu-id="8d3f9-106">Finding available images</span></span>

<span data-ttu-id="8d3f9-107">Le immagini rilasciate richiedono Docker 17.05 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="8d3f9-108">Si presume anche che l'utente sia in grado di eseguire Docker senza `sudo` o diritti amministrativi locali.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="8d3f9-109">Seguire le [istruzioni][install] ufficiali di Docker per installare `docker` correttamente.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="8d3f9-110">L'immagine del contenitore più recente contiene la versione più recente di PowerShell e i moduli Azure PowerShell più recenti supportati con il modulo Az.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-110">The latest container image contains the latest version of PowerShell and the latest Azure PowerShell modules supported with the Az module.</span></span>

<span data-ttu-id="8d3f9-111">Per ogni nuova versione del modulo Az si sta rilasciando un'immagine per i sistemi operativi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8d3f9-111">For each new release of the Az module we are releasing an image for the following operating systems:</span></span>

- <span data-ttu-id="8d3f9-112">Ubuntu 18.04 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8d3f9-112">Ubuntu 18.04 (default)</span></span>
- <span data-ttu-id="8d3f9-113">Debian 9</span><span class="sxs-lookup"><span data-stu-id="8d3f9-113">Debian 9</span></span>
- <span data-ttu-id="8d3f9-114">CentOs 7</span><span class="sxs-lookup"><span data-stu-id="8d3f9-114">CentOs 7</span></span>

<span data-ttu-id="8d3f9-115">Per un elenco completo delle immagini disponibili, vedere la pagina delle [immagini Docker][az image].</span><span class="sxs-lookup"><span data-stu-id="8d3f9-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="8d3f9-116">Uso di Azure PowerShell in un contenitore</span><span class="sxs-lookup"><span data-stu-id="8d3f9-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="8d3f9-117">I passaggi seguenti descrivono i comandi Docker necessari per scaricare l'immagine e avviare una sessione interattiva di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="8d3f9-118">Scaricare l'immagine più recente di azure-powershell.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="8d3f9-119">Eseguire il contenitore azure-powershell in modo interattivo:</span><span class="sxs-lookup"><span data-stu-id="8d3f9-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

<span data-ttu-id="8d3f9-120">Per gli host Docker di Windows, è necessario abilitare la condivisione file Docker per consentire la condivisione delle unità locali in Windows con i contenitori Linux.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-120">For Windows Docker hosts, you must enable Docker File Sharing to allow local drives on Windows to be shared with Linux containers.</span></span> <span data-ttu-id="8d3f9-121">Per altre informazioni, vedere [Introduzione a Docker per Windows][file-sharing].</span><span class="sxs-lookup"><span data-stu-id="8d3f9-121">For more information see [Get started with Docker for Windows][file-sharing].</span></span>

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="8d3f9-122">Eseguire il contenitore azure-powershell in modo interattivo con l'autenticazione host</span><span class="sxs-lookup"><span data-stu-id="8d3f9-122">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="8d3f9-123">Se Azure PowerShell è già stato installato nel sistema che ospita Docker, è possibile che le credenziali di Azure siano memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-123">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="8d3f9-124">Queste credenziali possono essere usate nella sessione di PowerShell in esecuzione nel contenitore Docker.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-124">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="8d3f9-125">Per impostazione predefinita, le credenziali memorizzate nella cache si trovano nella directory `$HOME/.Azure` dell'host.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-125">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="8d3f9-126">Per accedere alle credenziali, il servizio Docker deve avere accesso a questo percorso.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-126">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="8d3f9-127">Il comando seguente consente di avviare il contenitore con la cache delle credenziali montata e di avviare una sessione interattiva di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-127">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="8d3f9-128">Rimuovere l'immagine quando non è più necessaria</span><span class="sxs-lookup"><span data-stu-id="8d3f9-128">Remove the image when no longer needed</span></span>

<span data-ttu-id="8d3f9-129">Il comando seguente viene usato per eliminare il contenitore Docker quando non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-129">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="8d3f9-130">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="8d3f9-130">Next steps</span></span>

<span data-ttu-id="8d3f9-131">Per altre informazioni sui moduli di Azure PowerShell e sulle relative funzionalità, vedere [Introduzione ad Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="8d3f9-131">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
