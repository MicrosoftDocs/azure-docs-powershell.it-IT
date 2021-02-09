---
title: Uso di Azure PowerShell in Docker
description: Informazioni su come usare Azure PowerShell preinstallato in un'immagine Docker.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 48935f15241ec965adf4c34d2c17aa670110585a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100012746"
---
# <a name="using-azure-powershell-in-docker"></a>Uso di Azure PowerShell in Docker

Nelle immagini Docker pubblicate è ora incluso Azure PowerShell preinstallato. Questo articolo illustra come iniziare a usare Azure PowerShell nel contenitore Docker.

## <a name="finding-available-images"></a>Individuazione delle immagini disponibili

Le immagini rilasciate richiedono Docker 17.05 o versione successiva. Si presume anche che l'utente sia in grado di eseguire Docker senza `sudo` o diritti amministrativi locali. Seguire le [istruzioni][install] ufficiali di Docker per installare `docker` correttamente.

L'immagine del contenitore più recente contiene la versione più recente di PowerShell e i moduli Azure PowerShell più recenti supportati con il modulo Az.

Per ogni nuova versione del modulo Az si sta rilasciando un'immagine per i sistemi operativi seguenti:

- Ubuntu 18.04 (impostazione predefinita)
- Debian 9
- CentOs 7

Per un elenco completo delle immagini disponibili, vedere la pagina delle [immagini Docker][az image].

## <a name="using-azure-powershell-in-a-container"></a>Uso di Azure PowerShell in un contenitore

I passaggi seguenti descrivono i comandi Docker necessari per scaricare l'immagine e avviare una sessione interattiva di PowerShell.

1. Scaricare l'immagine più recente di azure-powershell.

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. Eseguire il contenitore azure-powershell in modo interattivo:

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

Per gli host Docker di Windows, è necessario abilitare la condivisione file Docker per consentire la condivisione delle unità locali in Windows con i contenitori Linux. Per altre informazioni, vedere [Introduzione a Docker per Windows][file-sharing].

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a>Eseguire il contenitore azure-powershell in modo interattivo con l'autenticazione host

Se Azure PowerShell è già stato installato nel sistema che ospita Docker, è possibile che le credenziali di Azure siano memorizzate nella cache. Queste credenziali possono essere usate nella sessione di PowerShell in esecuzione nel contenitore Docker.

Per impostazione predefinita, le credenziali memorizzate nella cache si trovano nella directory `$HOME/.Azure` dell'host. Per accedere alle credenziali, il servizio Docker deve avere accesso a questo percorso. Il comando seguente consente di avviare il contenitore con la cache delle credenziali montata e di avviare una sessione interattiva di PowerShell.

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a>Rimuovere l'immagine quando non è più necessaria

Il comando seguente viene usato per eliminare il contenitore Docker quando non è più necessario.

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a>Passaggi successivi

Per altre informazioni sui moduli di Azure PowerShell e sulle relative funzionalità, vedere [Introduzione ad Azure PowerShell](get-started-azureps.md).

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
