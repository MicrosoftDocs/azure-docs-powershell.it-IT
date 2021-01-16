---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325480"
---
# Modulo AZ. StorageSync
## Descrizione
I cmdlet nel modulo di sincronizzazione dello storage consentono di gestire le operazioni relative alla sincronizzazione di file di Azure in PowerShell.

## Cmdlet AZ. StorageSync
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
Questo comando elenca tutti gli endpoint del cloud all'interno di un gruppo di sincronizzazione specifico.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
Questo comando elenca tutti i gruppi di sincronizzazione all'interno di un servizio di sincronizzazione dello spazio di archiviazione specifico.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
Questo comando elenca tutti i server registrati in un servizio di sincronizzazione dello spazio di archiviazione specifico.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
Questo comando elenca tutti gli endpoint del server all'interno di un gruppo di sincronizzazione specifico.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
Questo comando elenca tutti i servizi di sincronizzazione dello storage all'interno di un ambito specifico del gruppo sottoscrizione/risorsa.

### [Invoke-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
Questo comando può essere usato per avviare manualmente il rilevamento delle modifiche agli spazi dei nomi. Può essere destinata all'intera condivisione, sottocartella o set di file. Può essere rilevato un massimo di 10.000 modifiche. Se l'ambito delle modifiche è noto, limitare l'esecuzione di questo comando alle parti dello spazio dei nomi, in modo che il rilevamento della modifica possa terminare rapidamente e all'interno di un limite di modifiche di 10.000.

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
Controlla i potenziali problemi di compatibilità tra il sistema e la sincronizzazione di file Azure.

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
Questo comando richiama tutti i file di livello sul disco locale.

### [New-AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
Questo comando crea un endpoint cloud di sincronizzazione di Azure file in un gruppo di sincronizzazione.

### [New-AzStorageSyncGroup](New-AzStorageSyncGroup.md)
Questo comando crea un nuovo gruppo di sincronizzazione all'interno di un servizio di sincronizzazione dello spazio di archiviazione specificato.

### [New-AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
Questo comando crea un nuovo endpoint server in un server registrato. Questo consente al percorso specificato sul server di avviare la sincronizzazione dei file con altri endpoint nel gruppo di sincronizzazione.

### [New-AzStorageSyncService](New-AzStorageSyncService.md)
Questo comando crea un nuovo servizio di sincronizzazione dello spazio di archiviazione in un gruppo di risorse.

### [Set-AzStorageSyncService](New-AzStorageSyncService.md)
Questo comando imposta un servizio di sincronizzazione dello storage in un gruppo di risorse.

### [Registro-AzStorageSyncServer](Register-AzStorageSyncServer.md)
Questo comando registra un server in un servizio di sincronizzazione dello spazio di archiviazione che crea una relazione di trust. PowerShell o Azure Portal possono quindi essere usati per configurare la sincronizzazione nel server.

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
Questo comando eliminerà l'endpoint cloud specificato da un gruppo di sincronizzazione. Senza almeno un endpoint nuvola, non è possibile sincronizzare altri endpoint del server in questo gruppo di sincronizzazione.

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
Questo comando eliminerà il gruppo di sincronizzazione specificato.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
Questo comando eliminerà l'endpoint server specificato. La sincronizzazione con questa posizione si arresta immediatamente.

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
Questo comando eliminerà il servizio di sincronizzazione dello spazio di archiviazione specificato.

### [Reset-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
Usare solo per la risoluzione dei problemi. Questo comando consente di eseguire il rollback del certificato del server di sincronizzazione dello storage usato per descrivere l'identità del server al servizio di sincronizzazione dello spazio di archiviazione.

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
Questo comando consente di modificare i parametri regolabili di un endpoint server.

### [Annullamento della registrazione-AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
Avviso: l'annullamento della registrazione di un server comporterà l'eliminazione a cascata di tutti gli endpoint server nel server. Questo comando Annulla la registrazione di un server dal servizio di sincronizzazione dello spazio di archiviazione.

