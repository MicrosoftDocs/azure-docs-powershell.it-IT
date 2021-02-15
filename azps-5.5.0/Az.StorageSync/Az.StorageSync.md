---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183127"
---
# Modulo Az.StorageSync
## Descrizione
I cmdlet del modulo Sincronizzazione archiviazione consentono di gestire le operazioni relative a Azure File Sync in PowerShell.

## Cmdlet Az.StorageSync
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
Questo comando elenca tutti gli endpoint cloud all'interno di un determinato gruppo di sincronizzazione.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
Questo comando elenca tutti i gruppi di sincronizzazione all'interno di un determinato servizio di sincronizzazione di archiviazione.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
Questo comando elenca tutti i server registrati con un determinato servizio di sincronizzazione di archiviazione.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
Questo comando elenca tutti gli endpoint del server all'interno di un determinato gruppo di sincronizzazione.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
Questo comando elenca tutti i servizi di sincronizzazione di archiviazione in un determinato ambito della sottoscrizione o del gruppo di risorse.

### [Invoke-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
Questo comando può essere usato per avviare manualmente il rilevamento delle modifiche agli spazi dei nomi. Può essere indirizzato all'intera condivisione, sottocartella o set di file. Possono essere rilevate al massimo 10.000 modifiche. Se si conosce l'ambito delle modifiche, limitare l'esecuzione di questo comando a parti dello spazio dei nomi, in modo che il rilevamento delle modifiche finisca rapidamente e entro un limite di 10.000 modifiche.

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
Verifica la presenza di potenziali problemi di compatibilità tra il sistema e Azure File Sync.

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
Questo comando richiama tutti i file a più livelli nel disco locale.

### [New-AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
Questo comando crea un endpoint cloud di Azure File Sync in un gruppo di sincronizzazione.

### [New-AzStorageSyncGroup](New-AzStorageSyncGroup.md)
Questo comando crea un nuovo gruppo di sincronizzazione all'interno di un servizio di sincronizzazione di archiviazione specificato.

### [New-AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
Questo comando crea un nuovo endpoint server in un server registrato. In questo modo il percorso specificato nel server può avviare la sincronizzazione dei file con altri endpoint nel gruppo di sincronizzazione.

### [New-AzStorageSyncService](New-AzStorageSyncService.md)
Questo comando crea un nuovo servizio di sincronizzazione di archiviazione in un gruppo di risorse.

### [Set-AzStorageSyncService](New-AzStorageSyncService.md)
Questo comando imposta un servizio di sincronizzazione dello spazio di archiviazione in un gruppo di risorse.

### [Register-AzStorageSyncServer](Register-AzStorageSyncServer.md)
Questo comando registra un server in un servizio di sincronizzazione di archiviazione che crea una relazione di trust. PowerShell o il portale di Azure possono quindi essere usati per configurare la sincronizzazione in questo server.

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
Questo comando eliminerà l'endpoint cloud specificato da un gruppo di sincronizzazione. Senza almeno un endpoint cloud, nessun altro endpoint server di questo gruppo di sincronizzazione può eseguire la sincronizzazione.

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
Questo comando eliminerà il gruppo di sincronizzazione specificato.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
Questo comando eliminerà l'endpoint server specificato. La sincronizzazione con questa posizione verrà interrotta immediatamente.

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
Questo comando eliminerà il servizio di sincronizzazione di archiviazione specificato.

### [Reset-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
Usare solo per la risoluzione dei problemi. Questo comando esegue il roll roll del certificato del server di sincronizzazione di archiviazione usato per descrivere l'identità del server nel servizio di sincronizzazione di archiviazione.

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
Questo comando consente di apportare modifiche ai parametri modificabili di un endpoint server.

### [Unregister-AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
Avviso: l'annullamento della registrazione di un server comporta l'eliminazione a catena di tutti gli endpoint server su questo server. Questo comando anregistrerà un server del servizio di sincronizzazione di archiviazione.

