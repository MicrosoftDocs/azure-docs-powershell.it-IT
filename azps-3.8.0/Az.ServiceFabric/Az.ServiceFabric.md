---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 5d963384d08dfed2e7e8516b892d2a3680c9332c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022250"
---
# Modulo AZ. ServiceFabric
## Descrizione
Modulo tessuto di Azure Service che consente di automatizzare le operazioni di fine-2-fine come la creazione di un cluster sicuro, il rollforward dei certificati cluster, l'aggiunta o la rimozione di nodi dal cluster e così via. L'elenco completo di tutte le operazioni è elencato di seguito.

## Cmdlet AZ. ServiceFabric

### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Aggiungere il nome o l'identificazione personale comune al cluster per scopi di autenticazione del client.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Aggiungere un certificato di cluster secondario al cluster.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Aggiungere nodi al tipo di nodo specifico nel cluster.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Aggiungere un nuovo tipo di nodo al cluster esistente.

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
Ottenere i dettagli delle applicazioni in tessuto di servizio.

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
Ottenere i dettagli del tipo di applicazione tessuto servizio.

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
Ottenere i dettagli della versione del tipo di servizio in tessuto.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Ottenere i dettagli delle risorse del cluster.

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
Ottenere i dettagli del servizio Fabric servizio nell'applicazione e nel cluster specificati.

### [New-AzServiceFabricApplication](New-AzServiceFabricApplication.md)
Creare un'applicazione nuova in tessuto del servizio in un gruppo di risorse e un cluster specificati.

### [New-AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
Creare un nuovo tipo di applicazione in tessuto del servizio sotto il gruppo e il cluster di risorse specificati.

### [New-AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
Creare una nuova versione del tipo di applicazione sotto il gruppo e il cluster di risorse specificati.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
Questo comando usa i certificati forniti dai certificati autofirmati o generati dal sistema per configurare un nuovo cluster di servizi in tessuto. Può usare un modello predefinito o un modello personalizzato che fornisci. È possibile specificare una cartella in cui esportare i certificati autofirmati o recuperarli in un secondo momento dall'archivio chiavi. 

### [New-AzServiceFabricService](New-AzServiceFabricService.md)
Creare un nuovo servizio tessuto servizio nell'applicazione e nel cluster specificati.

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
Rimuovere un'applicazione dal cluster. Verranno rimossi tutti i servizi sotto l'applicazione.

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
Rimuovere il tessuto del servizio un tipo di applicazione dal cluster. In questo modo verranno rimosse tutte le versioni di tipo in questa risorsa.

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
Rimuovere il tessuto di servizio una versione del tipo di applicazione dal cluster.

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Rimuovere il nome o i nomi dei certificati client o degli argomenti del certificato da usare per l'autenticazione del client nel cluster.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Rimuovere un certificato cluster da usare per la sicurezza del cluster.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Rimuovere i nodi dal tipo di nodo specifico da un cluster.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Rimuovere un tipo di nodo completo da un cluster.

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
Rimuovere un servizio dal cluster.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Rimuovere una o più impostazioni del tessuto del servizio dal cluster.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Aggiungere o aggiornare una o più impostazioni del tessuto del servizio al cluster.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Modificare il tipo di aggiornamento del tessuto di servizio del cluster.

### [Update-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
Aggiornare un'applicazione fabric di servizi. Questo consente di aggiornare i parametri dell'applicazione e/o aggiornare la versione del tipo di applicazione che attiverà un aggiornamento dell'applicazione.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Aggiornare il livello di durabilità o VmSku di un tipo di nodo nel cluster.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Aggiornare il livello di affidabilità del tipo di nodo principale in un cluster.

