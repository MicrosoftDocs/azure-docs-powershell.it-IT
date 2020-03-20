---
title: Uso di Azure PowerShell in Docker
description: Informazioni su come usare Azure PowerShell preinstallato in un'immagine Docker.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a5746b71cfc41f7c6283b0e95b0940ca4b594ec7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402681"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="6c2dc-103">Uso di Azure PowerShell in Docker</span><span class="sxs-lookup"><span data-stu-id="6c2dc-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="6c2dc-104">Nelle immagini Docker pubblicate è ora incluso Azure PowerShell preinstallato.</span><span class="sxs-lookup"><span data-stu-id="6c2dc-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="6c2dc-105">Questo articolo illustra come iniziare a usare Azure PowerShell nel contenitore Docker.</span><span class="sxs-lookup"><span data-stu-id="6c2dc-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="6c2dc-106">Individuazione delle immagini disponibili</span><span class="sxs-lookup"><span data-stu-id="6c2dc-106">Finding available images</span></span>

<span data-ttu-id="6c2dc-107">Le immagini rilasciate richiedono Docker 17.05 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="6c2dc-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="6c2dc-108">Si presume anche che l'utente sia in grado di eseguire Docker senza `sudo` o diritti amministrativi locali.</span><span class="sxs-lookup"><span data-stu-id="6c2dc-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="6c2dc-109">Seguire le [istruzioni][install] ufficiali di Docker per installare `docker` correttamente.</span><span class="sxs-lookup"><span data-stu-id="6c2dc-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="6c2dc-110">I contenitori rilasciati vengono compilati dai contenitori PowerShell ufficiali, di conseguenza il modulo Az è stato aggiunto come livello.</span><span class="sxs-lookup"><span data-stu-id="6c2dc-110">The released containers are built from the official PowerShell containers, then the Az module added as a layer.</span></span>

<span data-ttu-id="6c2dc-111">L'ultima immagine stabile include:</span><span class="sxs-lookup"><span data-stu-id="6c2dc-111">The latest stable image includes:</span></span>

- <span data-ttu-id="6c2dc-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="6c2dc-112">Ubuntu 18.04</span></span>
- <span data-ttu-id="6c2dc-113">PowerShell versione 6.2.4</span><span class="sxs-lookup"><span data-stu-id="6c2dc-113">PowerShell version 6.2.4</span></span>
- <span data-ttu-id="6c2dc-114">Modulo Az più recente di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6c2dc-114">Azure PowerShell most current Az module</span></span>

<span data-ttu-id="6c2dc-115">Per un elenco completo delle immagini disponibili, vedere la pagina delle [immagini Docker][az image].</span><span class="sxs-lookup"><span data-stu-id="6c2dc-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="6c2dc-116">Uso di Azure PowerShell in un contenitore</span><span class="sxs-lookup"><span data-stu-id="6c2dc-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="6c2dc-117">I passaggi seguenti descrivono i comandi Docker necessari per scaricare l'immagine e avviare una sessione interattiva di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6c2dc-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="6c2dc-118">Scaricare l'immagine più recente di azure-powershell.</span><span class="sxs-lookup"><span data-stu-id="6c2dc-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="6c2dc-119">Eseguire il contenitore azure-powershell in modo interattivo:</span><span class="sxs-lookup"><span data-stu-id="6c2dc-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="6c2dc-120">Eseguire il contenitore azure-powershell in modo interattivo con l'autenticazione host</span><span class="sxs-lookup"><span data-stu-id="6c2dc-120">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="6c2dc-121">Se Azure PowerShell è già stato installato nel sistema che ospita Docker, è possibile che le credenziali di Azure siano memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="6c2dc-121">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="6c2dc-122">Queste credenziali possono essere usate nella sessione di PowerShell in esecuzione nel contenitore Docker.</span><span class="sxs-lookup"><span data-stu-id="6c2dc-122">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="6c2dc-123">Per impostazione predefinita, le credenziali memorizzate nella cache si trovano nella directory `$HOME/.Azure` dell'host.</span><span class="sxs-lookup"><span data-stu-id="6c2dc-123">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="6c2dc-124">Per accedere alle credenziali, il servizio Docker deve avere accesso a questo percorso.</span><span class="sxs-lookup"><span data-stu-id="6c2dc-124">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="6c2dc-125">Il comando seguente consente di avviare il contenitore con la cache delle credenziali montata e di avviare una sessione interattiva di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6c2dc-125">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="6c2dc-126">Rimuovere l'immagine quando non è più necessaria</span><span class="sxs-lookup"><span data-stu-id="6c2dc-126">Remove the image when no longer needed</span></span>

<span data-ttu-id="6c2dc-127">Il comando seguente viene usato per eliminare il contenitore Docker quando non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="6c2dc-127">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="6c2dc-128">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="6c2dc-128">Next steps</span></span>

<span data-ttu-id="6c2dc-129">Per altre informazioni sui moduli di Azure PowerShell e sulle relative funzionalità, vedere [Introduzione ad Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="6c2dc-129">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell