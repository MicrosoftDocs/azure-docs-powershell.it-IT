---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 6d93775a028e7a590a8da9cc008640fb8484bdf2
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490114"
---
# Modulo AzureRM. ServiceFabric
## Descrizione
Modulo tessuto di Azure Service che consente di automatizzare le operazioni di fine-2-fine come la creazione di un cluster sicuro, il rollforward dei certificati cluster, l'aggiunta o la rimozione di nodi dal cluster e così via. L'elenco completo di tutte le operazioni è elencato di seguito.

## Cmdlet AzureRM. ServiceFabric
### [Add-AzureRmServiceFabricApplicationCertificate](Add-AzureRmServiceFabricApplicationCertificate.md)
Aggiungere un nuovo certificato ai set di scale della macchina virtuale che compongono il cluster. Il certificato è destinato a essere usato come certificato dell'applicazione.

### [Add-AzureRmServiceFabricClientCertificate](Add-AzureRmServiceFabricClientCertificate.md)
Aggiungere il nome o l'identificazione personale comune al cluster per scopi di autenticazione del client.

### [Add-AzureRmServiceFabricClusterCertificate](Add-AzureRmServiceFabricClusterCertificate.md)
Aggiungere un certificato di cluster secondario al cluster.

### [Add-AzureRmServiceFabricNode](Add-AzureRmServiceFabricNode.md)
Aggiungere nodi al tipo di nodo specifico nel cluster.

### [Add-AzureRmServiceFabricNodeType](Add-AzureRmServiceFabricNodeType.md)
Aggiungere un nuovo tipo di nodo al cluster esistente.

### [Get-AzureRmServiceFabricCluster](Get-AzureRmServiceFabricCluster.md)
Ottenere i dettagli delle risorse del cluster.

### [New-AzureRmServiceFabricCluster](New-AzureRmServiceFabricCluster.md)
Questo comando usa i certificati forniti dai certificati autofirmati o generati dal sistema per configurare un nuovo cluster di servizi in tessuto. Può usare un modello predefinito o un modello personalizzato che fornisci. È possibile specificare una cartella in cui esportare i certificati autofirmati o recuperarli in un secondo momento dall'archivio chiavi. 

### [Remove-AzureRmServiceFabricClientCertificate](Remove-AzureRmServiceFabricClientCertificate.md)
Rimuovere il nome o i nomi dei certificati client o degli argomenti del certificato da usare per l'autenticazione del client nel cluster.

### [Remove-AzureRmServiceFabricClusterCertificate](Remove-AzureRmServiceFabricClusterCertificate.md)
Rimuovere un certificato cluster da usare per la sicurezza del cluster.

### [Remove-AzureRmServiceFabricNode](Remove-AzureRmServiceFabricNode.md)
Rimuovere i nodi dal tipo di nodo specifico da un cluster.

### [Remove-AzureRmServiceFabricNodeType](Remove-AzureRmServiceFabricNodeType.md)
Rimuovere un tipo di nodo completo da un cluster.

### [Remove-AzureRmServiceFabricSetting](Remove-AzureRmServiceFabricSetting.md)
Rimuovere una o più impostazioni del tessuto del servizio dal cluster.

### [Set-AzureRmServiceFabricSetting](Set-AzureRmServiceFabricSetting.md)
Aggiungere o aggiornare una o più impostazioni del tessuto del servizio al cluster.

### [Set-AzureRmServiceFabricUpgradeType](Set-AzureRmServiceFabricUpgradeType.md)
Modificare il tipo di aggiornamento del tessuto di servizio del cluster.

### [Update-AzureRmServiceFabricDurability](Update-AzureRmServiceFabricDurability.md)
Aggiornare il livello di durabilità o VmSku di un tipo di nodo nel cluster.

### [Update-AzureRmServiceFabricReliability](Update-AzureRmServiceFabricReliability.md)
Aggiornare il livello di affidabilità del tipo di nodo principale in un cluster.

