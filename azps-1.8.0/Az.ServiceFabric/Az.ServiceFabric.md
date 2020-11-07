---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 01bf8c630f4fc4d137e98be5b1996eaf47ea3363
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "93673371"
---
# Modulo AZ. ServiceFabric
## Descrizione
Modulo tessuto di Azure Service che consente di automatizzare le operazioni di fine-2-fine come la creazione di un cluster sicuro, il rollforward dei certificati cluster, l'aggiunta o la rimozione di nodi dal cluster e così via. L'elenco completo di tutte le operazioni è elencato di seguito.

## Cmdlet AZ. ServiceFabric
### [Add-AzServiceFabricApplicationCertificate](Add-AzServiceFabricApplicationCertificate.md)
Aggiungere un nuovo certificato ai set di scale della macchina virtuale che compongono il cluster. Il certificato è destinato a essere usato come certificato dell'applicazione.

### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Aggiungere il nome o l'identificazione personale comune al cluster per scopi di autenticazione del client.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Aggiungere un certificato di cluster secondario al cluster.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Aggiungere nodi al tipo di nodo specifico nel cluster.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Aggiungere un nuovo tipo di nodo al cluster esistente.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Ottenere i dettagli delle risorse del cluster.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
Questo comando usa i certificati forniti dai certificati autofirmati o generati dal sistema per configurare un nuovo cluster di servizi in tessuto. Può usare un modello predefinito o un modello personalizzato che fornisci. È possibile specificare una cartella in cui esportare i certificati autofirmati o recuperarli in un secondo momento dall'archivio chiavi. 

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Rimuovere il nome o i nomi dei certificati client o degli argomenti del certificato da usare per l'autenticazione del client nel cluster.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Rimuovere un certificato cluster da usare per la sicurezza del cluster.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Rimuovere i nodi dal tipo di nodo specifico da un cluster.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Rimuovere un tipo di nodo completo da un cluster.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Rimuovere una o più impostazioni del tessuto del servizio dal cluster.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Aggiungere o aggiornare una o più impostazioni del tessuto del servizio al cluster.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Modificare il tipo di aggiornamento del tessuto di servizio del cluster.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Aggiornare il livello di durabilità o VmSku di un tipo di nodo nel cluster.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Aggiornare il livello di affidabilità del tipo di nodo principale in un cluster.

