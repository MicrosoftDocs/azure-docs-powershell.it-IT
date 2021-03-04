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
# <a name="using-azure-powershell-in-docker"></a>Uso di Azure PowerShell in Docker

Si stanno pubblicando immagini Docker con Azure PowerShell preinstallata. Questo articolo illustra come iniziare a usare Azure PowerShell nel contenitore docker.

## <a name="finding-available-images"></a>Ricerca di immagini disponibili

Le immagini rilasciate richiedono Docker 17,05 o versione successiva. Si prevede anche che sia possibile eseguire Docker senza `sudo` diritti amministrativi locali o. Per installare correttamente, seguire [le istruzioni][install] ufficiali di Docker `docker` .

L'immagine del contenitore più recente contiene la versione più recente di PowerShell e i moduli Azure PowerShell più recenti supportati con il modulo AZ.

Per ogni nuova versione del modulo AZ si sta rilasciando un'immagine per i sistemi operativi seguenti:

- Ubuntu 18,04 (impostazione predefinita)
- Debian 9
- CentOs 7

Un elenco completo delle immagini disponibili è reperibile nella pagina dell' [immagine Docker][az image] .

## <a name="using-azure-powershell-in-a-container"></a>Uso di Azure PowerShell in un contenitore

I passaggi seguenti mostrano i comandi di Docker necessari per scaricare l'immagine e avviare una sessione interattiva di PowerShell.

1. Scaricare l'immagine di Azure-PowerShell più recente.

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. Eseguire il contenitore Azure-PowerShell in modalità interattiva:

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

Per gli host Docker di Windows, è necessario abilitare la condivisione di file Docker per consentire la condivisione delle unità locali in Windows con i contenitori Linux. Per ulteriori informazioni, vedere [Introduzione a Docker per Windows][file-sharing].

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a>Eseguire il contenitore Azure-PowerShell in modo interattivo usando l'autenticazione host

Se è già stato installato Azure PowerShell nell'host di sistema Docker, è possibile che siano state memorizzate nella cache le credenziali di Azure. Queste credenziali possono essere usate nella sessione di PowerShell in esecuzione nel contenitore docker.

Per impostazione predefinita, le credenziali memorizzate nella cache si trovano nella `$HOME/.Azure` directory dell'host. Per accedere alle credenziali, il servizio Docker deve avere accesso a questo percorso. Il comando seguente avvia il contenitore con la cache delle credenziali montata e avvia una sessione interattiva di PowerShell.

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
