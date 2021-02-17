---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208074"
---
# Modulo Az.ServiceFabric
## Descrizione
Modulo Azure Service Fabric che consente di automatizzare le operazioni di fine 2, come la creazione di un cluster sicuro, il rolling over di certificati cluster, l'aggiunta o la rimozione di nodi dal cluster e così via. Di seguito è riportato l'elenco completo di tutte le operazioni.

## Cmdlet Az.ServiceFabric
### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Aggiungere il nome comune o l'immagine thumbprint al cluster ai fini dell'autenticazione client.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Aggiungere un certificato cluster secondario al cluster.

### [Add-AzServiceFabricManagedClusterClientCertificate](Add-AzServiceFabricManagedClusterClientCertificate.md)
Aggiungere il nome comune del certificato o l'immagine thumbprint al cluster. Il certificato verrà registrato di nuovo nel cluster ai fini dell'autenticazione client.

### [Add-AzServiceFabricManagedNodeTypeVMExtension](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
Aggiungere l'estensione della macchina virtuale al tipo di nodo.

### [Add-AzServiceFabricManagedNodeTypeVMSecret](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
Aggiungere il segreto certificato al tipo di nodo.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Aggiungere i nodi al tipo di nodo specifico nel cluster.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Aggiungere un nuovo tipo di nodo al cluster esistente.

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
Ottenere i dettagli dell'applicazione Service Fabric.

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
Ottenere i dettagli sul tipo di applicazione Service Fabric.

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
Ottenere i dettagli della versione del tipo di applicazione Service Fabric.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Informazioni dettagliate sulle risorse del cluster.

### [Get-AzServiceFabricManagedCluster](Get-AzServiceFabricManagedCluster.md)
Ottenere i dettagli delle risorse del cluster gestito.

### [Get-AzServiceFabricManagedNodeType](Get-AzServiceFabricManagedNodeType.md)
Ottenere i dettagli delle risorse per il tipo di nodo gestito.

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
Ottenere i dettagli del servizio Service Fabric nell'applicazione e nel cluster specificati.

### [New-AzServiceFabricApplication](New-AzServiceFabricApplication.md)
Creare una nuova applicazione di tessuto di servizio nel gruppo di risorse e nel cluster specificati.

### [New-AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
Creare un nuovo tipo di applicazione tessuto di servizio nel gruppo di risorse e nel cluster specificati.

### [New-AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
Creare una nuova versione del tipo di applicazione nel gruppo di risorse e nel cluster specificati.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
Questo comando usa i certificati forniti dall'utente o i certificati autofirmati generati dal sistema per configurare un nuovo cluster di tessuto di servizio. Può usare un modello predefinito o un modello personalizzato specificato dall'utente. È possibile specificare una cartella in cui esportare i certificati autofirmati o recuperarli in un secondo momento dal vault delle chiavi.

### [New-AzServiceFabricManagedCluster](New-AzServiceFabricManagedCluster.md)
Creare un nuovo cluster gestito.

### [New-AzServiceFabricManagedNodeType](New-AzServiceFabricManagedNodeType.md)
Creare una nuova risorsa tipo di nodo.

### [New-AzServiceFabricService](New-AzServiceFabricService.md)
Creare un nuovo servizio di tessuto di servizio nell'applicazione e nel cluster specificati.

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
Rimuovere un'applicazione dal cluster. Tutti i servizi dell'applicazione verranno così rimosso.

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
Rimuovere un tipo di applicazione da un tipo di applicazione del servizio dal cluster. In questo modo verranno rimuovono tutte le versioni del tipo in questa risorsa.

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
Rimuovere la versione service fabric di un tipo di applicazione dal cluster.

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Rimuovere uno o più certificati client o i nomi degli oggetto del certificato usati per l'autenticazione client nel cluster.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Rimuovere un certificato cluster da usare per la sicurezza dei cluster.

### [Remove-AzServiceFabricManagedCluster](Remove-AzServiceFabricManagedCluster.md)
Rimuovere la risorsa cluster.

### [Remove-AzServiceFabricManagedClusterClientCertificate](Remove-AzServiceFabricManagedClusterClientCertificate.md)
Certificato client di remvoe in base all'immagine thumbprint o al nome comune.

### [Remove-AzServiceFabricManagedNodeType](Remove-AzServiceFabricManagedNodeType.md)
Rimuovere il tipo di nodo o nodi specifici all'interno del tipo di nodo.

### [Remove-AzServiceFabricManagedNodeTypeVMExtension](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
Rimuovere l'estensione della macchina virtuale dal tipo di nodo.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Rimuovere i nodi dal tipo di nodo specifico da un cluster.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Rimuovere un tipo di nodo completo da un cluster.

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
Rimuovere un servizio dal cluster.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Rimuovere una o più impostazioni di Tessuto di servizio dal cluster.

### [Restart-AzServiceFabricManagedNodeType](Restart-AzServiceFabricManagedNodeType.md)
Riavviare nodi specifici dal tipo di nodo.

### [Set-AzServiceFabricManagedCluster](Set-AzServiceFabricManagedCluster.md)
Impostare le proprietà delle risorse cluster.

### [Set-AzServiceFabricManagedNodeType](Set-AzServiceFabricManagedNodeType.md)
Imposta le proprietà delle risorse del tipo di nodo o esegue azioni di reimage su specifici tipi di nodo con il parametro -Reimage.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Aggiungere o aggiornare una o più impostazioni di Service Fabric nel cluster.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Modificare il tipo di aggiornamento Service Fabric del cluster.

### [Update-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
Aggiornare un'applicazione di tessuto di servizio. In questo modo è possibile aggiornare i parametri dell'applicazione e/o aggiornare la versione del tipo di applicazione che attiverà un aggiornamento dell'applicazione.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Aggiornare il livello di durabilità o VmSKU di un tipo di nodo nel cluster.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Aggiornare il livello di affidabilità del tipo di nodo primario in un cluster.

