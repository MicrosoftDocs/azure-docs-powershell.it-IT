---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: f4592a371e528c7779e07251bf79677dac47e6df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323366"
---
# <span data-ttu-id="e39ed-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e39ed-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="e39ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e39ed-102">SYNOPSIS</span></span>
<span data-ttu-id="e39ed-103">Crea un cluster di Azure HDInsight nel gruppo di risorse specificato per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e39ed-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="e39ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e39ed-104">SYNTAX</span></span>

### <span data-ttu-id="e39ed-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e39ed-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-StorageAccountManagedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker] [-KafkaClientGroupId <String>]
 [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>] [-PrivateLink <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e39ed-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e39ed-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e39ed-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="e39ed-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e39ed-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e39ed-108">DESCRIPTION</span></span>
<span data-ttu-id="e39ed-109">La New-AzHDInsightCluster crea un cluster di Azure HDInsight usando i parametri specificati o usando un oggetto Configuration creato usando il cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="e39ed-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="e39ed-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e39ed-110">EXAMPLES</span></span>

### <span data-ttu-id="e39ed-111">Esempio 1: creare un cluster di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="e39ed-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="e39ed-112">Questo comando crea un cluster nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e39ed-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="e39ed-113">Esempio 2: creare un cluster con la crittografia del disco con chiave gestita dal cliente</span><span class="sxs-lookup"><span data-stu-id="e39ed-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"
        $clusterCreds = Get-Credential

        # Customer-managed Key info
        $assignedIdentity = "your-ami-resource-id"
        $encryptionKeyName = "new-key"
        $encryptionVaultUri = "https://MyKeyVault.vault.azure.net"
        $encryptionKeyVersion = "00000000000000000000000000000000"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Spark `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="e39ed-114">Esempio 3: creare un cluster di Azure HDInsight che consente la crittografia in transito</span><span class="sxs-lookup"><span data-stu-id="e39ed-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="e39ed-115">Esempio 4: creare un cluster Azure HDInsight con la caratteristica inoltro in uscita e collegamento privato</span><span class="sxs-lookup"><span data-stu-id="e39ed-115">Example 4: Create an Azure HDInsight cluster with relay outbound and private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Virtual network info
        $virtualNetworkId="yourvnetresourceid"
        $subnetName="yoursubnetname"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -ResourceProviderConnection Outbound -PrivateLink Enabled `
```

### <span data-ttu-id="e39ed-116">Esempio 5: creare un cluster di Azure HDInsight che consente la crittografia in host</span><span class="sxs-lookup"><span data-stu-id="e39ed-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="e39ed-117">Esempio 6: creare un cluster di Azure HDInsight che Abilita la scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="e39ed-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create autoscale configuration
        $autoscaleConfiguration=New-AzHDInsightClusterAutoscaleConfiguration `
            -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

### <span data-ttu-id="e39ed-118">Esempio 7: creare un cluster di Azure HDInsight con il proxy REST di Kafka.</span><span class="sxs-lookup"><span data-stu-id="e39ed-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Kafka Rest Proxy configuration info
        $kafkaClientGroupName = "yourclientgroupname"
        $kafkaClientGroupId = "yourclientgroupid"
        $kafkaManagementNodeSize = "Standard_D4_v2"
        $disksPerWorkerNode = 2

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Kafka `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -KafkaClientGroupId  $kafkaClientGroupId -KafkaClientGroupName $kafkaClientGroupName `
            -KafkaManagementNodeSize $kafkaManagementNodeSize -DisksPerWorkerNode $disksPerWorkerNode
```

### <span data-ttu-id="e39ed-119">Esempio 8: creare un cluster di Azure HDInsight con l'archiviazione di Azure Data Lake Gen2 storage.</span><span class="sxs-lookup"><span data-stu-id="e39ed-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageManagedIdentity = "yourstorageusermanagedidentity"
        $storageFileSystem = "filesystem01"
        $storageAccountType=AzureDataLakeStorageGen2

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountManagedIdentity $storageManagedIdentity `
            -StorageFileSystem $storageFileSystem `
            -StorageAccountType $storageAccountType `
            -SshCredential $clusterCreds
```

### <span data-ttu-id="e39ed-120">Esempio 9: creare un cluster di Azure HDInsight con ESP (Enterprise Security Package) e abilitare HDInsight ID Broker.</span><span class="sxs-lookup"><span data-stu-id="e39ed-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountKey = "yourstorageaccountaccesskey"
        $storageContainer = "yourcontainer01"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # ESP configuration
        $domainResourceId = "your Azure AD Domin Service resource id"
        $domainUser = "yourdomainuser"
        $domainPassword = "yourdoaminpasswd"
        $domainPassword = ConvertTo-SecureString $domainPassword -AsPlainText -Force
        $domainCredential = New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
        $clusterUserGroupDns = "dominusergroup"
        $ldapUrls = "ldaps://{your domain name}:636"

        $clusterTier = Premium
        $vnetId = "yourvnetid"
        $subnetName = "yoursubnetname"
        $assignedIdentity = "your user managed assigned identity resourcee id"

        #Create security profile
        $config= New-AzHDInsightClusterConfig|Add-AzHDInsightSecurityProfile -DomainResourceId $domainResourceId -DomainUserCredential $domainCredential -LdapsUrls $ldapUrls -ClusterUsersGroupDNs $clusterUserGroupDns

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusteTier $clusterTier `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $vnetId -SubnetName $subnetName `
            -AssignedIdentity $assignedIdentity `
            -SecurityProfile $config.SecurityProfile -EnableIDBroker
```

## <span data-ttu-id="e39ed-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e39ed-121">PARAMETERS</span></span>

### <span data-ttu-id="e39ed-122">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="e39ed-122">-AadTenantId</span></span>
<span data-ttu-id="e39ed-123">Specifica l'ID tenant di Azure AD che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e39ed-123">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-124">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="e39ed-124">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="e39ed-125">Specifica gli account di archiviazione di Azure aggiuntivi per il cluster.</span><span class="sxs-lookup"><span data-stu-id="e39ed-125">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="e39ed-126">In alternativa, puoi usare il cmdlet Add-AzHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="e39ed-126">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-127">-AmbariDatabase</span><span class="sxs-lookup"><span data-stu-id="e39ed-127">-AmbariDatabase</span></span>
<span data-ttu-id="e39ed-128">Ottiene o imposta il database per Ambari.</span><span class="sxs-lookup"><span data-stu-id="e39ed-128">Gets or sets the database for ambari.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-129">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e39ed-129">-ApplicationId</span></span>
<span data-ttu-id="e39ed-130">Ottiene o imposta l'ID dell'applicazione Principal del servizio per l'accesso a Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="e39ed-130">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-131">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e39ed-131">-AssignedIdentity</span></span>
<span data-ttu-id="e39ed-132">Ottiene o imposta l'identità assegnata.</span><span class="sxs-lookup"><span data-stu-id="e39ed-132">Gets or sets the assigned identity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-133">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e39ed-133">-AutoscaleConfiguration</span></span>
<span data-ttu-id="e39ed-134">Ottiene o imposta la configurazione di scala automatica</span><span class="sxs-lookup"><span data-stu-id="e39ed-134">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-135">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="e39ed-135">-CertificateFileContents</span></span>
<span data-ttu-id="e39ed-136">Specifica il contenuto del file del certificato che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e39ed-136">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-137">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e39ed-137">-CertificateFilePath</span></span>
<span data-ttu-id="e39ed-138">Specifica il percorso del file del certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="e39ed-138">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e39ed-139">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e39ed-139">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-140">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e39ed-140">-CertificatePassword</span></span>
<span data-ttu-id="e39ed-141">Specifica la password per il certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="e39ed-141">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e39ed-142">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e39ed-142">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-143">-Clustername</span><span class="sxs-lookup"><span data-stu-id="e39ed-143">-ClusterName</span></span>
<span data-ttu-id="e39ed-144">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="e39ed-144">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-145">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="e39ed-145">-ClusterSizeInNodes</span></span>
<span data-ttu-id="e39ed-146">Specifica il numero di nodi di lavoro per il cluster.</span><span class="sxs-lookup"><span data-stu-id="e39ed-146">Specifies the number of Worker nodes for the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-147">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="e39ed-147">-ClusterTier</span></span>
<span data-ttu-id="e39ed-148">Specifica il livello del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e39ed-148">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="e39ed-149">Per impostazione predefinita, è standard.</span><span class="sxs-lookup"><span data-stu-id="e39ed-149">By default, this is Standard.</span></span>
<span data-ttu-id="e39ed-150">Il livello Premium può essere usato solo con i cluster Linux e consente l'uso di alcune nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e39ed-150">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.Tier
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-151">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="e39ed-151">-ClusterType</span></span>
<span data-ttu-id="e39ed-152">Specifica il tipo di cluster da creare.</span><span class="sxs-lookup"><span data-stu-id="e39ed-152">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="e39ed-153">Le opzioni disponibili sono: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka e RServer</span><span class="sxs-lookup"><span data-stu-id="e39ed-153">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-154">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="e39ed-154">-ComponentVersion</span></span>
```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-155">-Config</span><span class="sxs-lookup"><span data-stu-id="e39ed-155">-Config</span></span>
<span data-ttu-id="e39ed-156">Specifica l'oggetto cluster da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="e39ed-156">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="e39ed-157">Questo oggetto può essere creato usando il cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="e39ed-157">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-158">-Configurazioni</span><span class="sxs-lookup"><span data-stu-id="e39ed-158">-Configurations</span></span>
<span data-ttu-id="e39ed-159">Specifica le configurazioni di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e39ed-159">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="e39ed-160">In alternativa, puoi usare il cmdlet Add-AzHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="e39ed-160">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e39ed-161">-DefaultProfile</span></span>
<span data-ttu-id="e39ed-162">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e39ed-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-163">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="e39ed-163">-DisksPerWorkerNode</span></span>
<span data-ttu-id="e39ed-164">Specifica il numero di dischi per il ruolo di nodo di lavoro nel cluster.</span><span class="sxs-lookup"><span data-stu-id="e39ed-164">Specifies the number of disks for worker node role in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-165">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="e39ed-165">-EdgeNodeSize</span></span>
<span data-ttu-id="e39ed-166">Specifica le dimensioni della macchina virtuale per il nodo Edge.</span><span class="sxs-lookup"><span data-stu-id="e39ed-166">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="e39ed-167">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e39ed-167">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="e39ed-168">Questo parametro è valido solo per i cluster RServer.</span><span class="sxs-lookup"><span data-stu-id="e39ed-168">This parameter is valid only for RServer clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-169">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="e39ed-169">-EnableIDBroker</span></span>
<span data-ttu-id="e39ed-170">Abilita la caratteristica di HDInsight Identity Broker.</span><span class="sxs-lookup"><span data-stu-id="e39ed-170">Enables HDInsight Identity Broker feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-171">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e39ed-171">-EncryptionAlgorithm</span></span>
<span data-ttu-id="e39ed-172">Ottiene o imposta l'algoritmo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e39ed-172">Gets or sets the encryption algorithm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA-OAEP-256, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-173">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="e39ed-173">-EncryptionAtHost</span></span>
<span data-ttu-id="e39ed-174">Ottiene o imposta il contrassegno che indica se abilitare la crittografia in host o meno.</span><span class="sxs-lookup"><span data-stu-id="e39ed-174">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-175">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="e39ed-175">-EncryptionInTransit</span></span>
<span data-ttu-id="e39ed-176">Ottiene o imposta il contrassegno che indica se abilitare la crittografia in transito o meno.</span><span class="sxs-lookup"><span data-stu-id="e39ed-176">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-177">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="e39ed-177">-EncryptionKeyName</span></span>
<span data-ttu-id="e39ed-178">Ottiene o imposta il nome della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e39ed-178">Gets or sets the encryption key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-179">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="e39ed-179">-EncryptionKeyVersion</span></span>
<span data-ttu-id="e39ed-180">Ottiene o imposta la versione della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e39ed-180">Gets or sets the encryption key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-181">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="e39ed-181">-EncryptionVaultUri</span></span>
<span data-ttu-id="e39ed-182">Ottiene o imposta l'URI del Vault di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e39ed-182">Gets or sets the encryption vault uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-183">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="e39ed-183">-HeadNodeSize</span></span>
<span data-ttu-id="e39ed-184">Specifica le dimensioni della macchina virtuale per il nodo head.</span><span class="sxs-lookup"><span data-stu-id="e39ed-184">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="e39ed-185">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e39ed-185">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-186">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="e39ed-186">-HiveMetastore</span></span>
<span data-ttu-id="e39ed-187">Specifica il database SQL per archiviare i metadati hive.</span><span class="sxs-lookup"><span data-stu-id="e39ed-187">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="e39ed-188">In alternativa, puoi usare il cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="e39ed-188">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-189">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="e39ed-189">-HttpCredential</span></span>
<span data-ttu-id="e39ed-190">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="e39ed-190">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-191">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="e39ed-191">-KafkaClientGroupId</span></span>
<span data-ttu-id="e39ed-192">Ottiene o imposta l'ID del gruppo client per l'accesso al proxy REST di Kafka.</span><span class="sxs-lookup"><span data-stu-id="e39ed-192">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-193">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="e39ed-193">-KafkaClientGroupName</span></span>
<span data-ttu-id="e39ed-194">Ottiene o imposta il nome del gruppo client per l'accesso al proxy REST di Kafka.</span><span class="sxs-lookup"><span data-stu-id="e39ed-194">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-195">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="e39ed-195">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="e39ed-196">Ottiene o imposta le dimensioni del nodo di gestione di Kafka.</span><span class="sxs-lookup"><span data-stu-id="e39ed-196">Gets or sets the size of the Kafka Management Node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-197">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e39ed-197">-Location</span></span>
<span data-ttu-id="e39ed-198">Specifica la posizione per il cluster.</span><span class="sxs-lookup"><span data-stu-id="e39ed-198">Specifies the location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-199">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="e39ed-199">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="e39ed-200">Ottiene o imposta la versione di TLS supportata minima.</span><span class="sxs-lookup"><span data-stu-id="e39ed-200">Gets or sets the minimal supported TLS version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-201">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e39ed-201">-ObjectId</span></span>
<span data-ttu-id="e39ed-202">Specifica l'ID oggetto Azure AD (GUID) dell'entità servizio Azure AD che rappresenta il cluster.</span><span class="sxs-lookup"><span data-stu-id="e39ed-202">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="e39ed-203">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e39ed-203">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-204">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="e39ed-204">-OozieMetastore</span></span>
<span data-ttu-id="e39ed-205">Specifica il database SQL per archiviare i metadati di oozie.</span><span class="sxs-lookup"><span data-stu-id="e39ed-205">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="e39ed-206">In alternativa, puoi usare il cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="e39ed-206">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-207">-OSType</span><span class="sxs-lookup"><span data-stu-id="e39ed-207">-OSType</span></span>
<span data-ttu-id="e39ed-208">Specifica il sistema operativo per il cluster.</span><span class="sxs-lookup"><span data-stu-id="e39ed-208">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="e39ed-209">Le opzioni disponibili sono: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="e39ed-209">Options are: Windows, Linux</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.OSType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-210">-PrivateLink</span><span class="sxs-lookup"><span data-stu-id="e39ed-210">-PrivateLink</span></span>
<span data-ttu-id="e39ed-211">Ottiene o imposta il tipo di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="e39ed-211">Gets or sets the private link type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-212">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="e39ed-212">-RdpAccessExpiry</span></span>
<span data-ttu-id="e39ed-213">Specifica la scadenza, come oggetto DateTime, per l'accesso RDP (Remote Desktop Protocol) a un cluster.</span><span class="sxs-lookup"><span data-stu-id="e39ed-213">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-214">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="e39ed-214">-RdpCredential</span></span>
<span data-ttu-id="e39ed-215">Specifica le credenziali remote desktop (RDP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="e39ed-215">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="e39ed-216">Questo è solo per i cluster Windows.</span><span class="sxs-lookup"><span data-stu-id="e39ed-216">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-217">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e39ed-217">-ResourceGroupName</span></span>
<span data-ttu-id="e39ed-218">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e39ed-218">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-219">-ResourceProviderConnection</span><span class="sxs-lookup"><span data-stu-id="e39ed-219">-ResourceProviderConnection</span></span>
<span data-ttu-id="e39ed-220">Ottiene o imposta il tipo di connessione del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="e39ed-220">Gets or sets the resource provider connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-221">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="e39ed-221">-ScriptActions</span></span>
<span data-ttu-id="e39ed-222">Specifica le azioni di script da eseguire nel cluster alla fine della creazione del cluster.</span><span class="sxs-lookup"><span data-stu-id="e39ed-222">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="e39ed-223">In alternativa, è possibile usare Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="e39ed-223">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-224">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="e39ed-224">-SecurityProfile</span></span>
<span data-ttu-id="e39ed-225">Specifica le proprietà correlate alla sicurezza usate per creare un cluster sicuro.</span><span class="sxs-lookup"><span data-stu-id="e39ed-225">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="e39ed-226">In alternativa, puoi usare il cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="e39ed-226">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-227">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="e39ed-227">-SshCredential</span></span>
<span data-ttu-id="e39ed-228">Specifica le credenziali SSH da usare per le connessioni SSH.</span><span class="sxs-lookup"><span data-stu-id="e39ed-228">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="e39ed-229">Questo è solo per i cluster Linux.</span><span class="sxs-lookup"><span data-stu-id="e39ed-229">This is only for Linux clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-230">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e39ed-230">-SshPublicKey</span></span>
<span data-ttu-id="e39ed-231">Specifica la chiave pubblica da usare per le connessioni SSH.</span><span class="sxs-lookup"><span data-stu-id="e39ed-231">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="e39ed-232">Questo è solo per i cluster Linux.</span><span class="sxs-lookup"><span data-stu-id="e39ed-232">This is only for Linux clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-233">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e39ed-233">-StorageAccountKey</span></span>
<span data-ttu-id="e39ed-234">Ottiene o imposta il codice di accesso dell'account di archiviazione per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e39ed-234">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-235">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="e39ed-235">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="e39ed-236">Ottiene o imposta l'identità gestita dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e39ed-236">Gets or sets the storage account managed identity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-237">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="e39ed-237">-StorageAccountResourceId</span></span>
<span data-ttu-id="e39ed-238">Ottiene o imposta l'ID risorsa di archiviazione per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e39ed-238">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-239">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e39ed-239">-StorageAccountType</span></span>
<span data-ttu-id="e39ed-240">Ottiene o imposta il tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e39ed-240">Gets or sets the type of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-241">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="e39ed-241">-StorageContainer</span></span>
<span data-ttu-id="e39ed-242">Ottiene o imposta il nome StorageContainer per l'account di archiviazione di Azure predefinito</span><span class="sxs-lookup"><span data-stu-id="e39ed-242">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-243">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="e39ed-243">-StorageFileSystem</span></span>
<span data-ttu-id="e39ed-244">Ottiene o imposta il file System per l'account di archiviazione di Gen2 di Azure Data Lake predefinito.</span><span class="sxs-lookup"><span data-stu-id="e39ed-244">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-245">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="e39ed-245">-StorageRootPath</span></span>
<span data-ttu-id="e39ed-246">Ottiene o imposta il percorso della radice del cluster nell'account predefinito di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e39ed-246">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-247">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="e39ed-247">-SubnetName</span></span>
<span data-ttu-id="e39ed-248">Ottiene o imposta il nome della subnet per il cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e39ed-248">Gets or sets the subnet name for this HDInsight cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-249">-Versione</span><span class="sxs-lookup"><span data-stu-id="e39ed-249">-Version</span></span>
<span data-ttu-id="e39ed-250">Specifica la versione HDI del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e39ed-250">Specifies the HDI version of the HDInsight cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-251">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e39ed-251">-VirtualNetworkId</span></span>
<span data-ttu-id="e39ed-252">Specifica l'ID della rete virtuale in cui eseguire il provisioning del cluster.</span><span class="sxs-lookup"><span data-stu-id="e39ed-252">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-253">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="e39ed-253">-WorkerNodeSize</span></span>
<span data-ttu-id="e39ed-254">Specifica le dimensioni della macchina virtuale per il nodo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e39ed-254">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="e39ed-255">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e39ed-255">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-256">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="e39ed-256">-ZookeeperNodeSize</span></span>
<span data-ttu-id="e39ed-257">Specifica le dimensioni della macchina virtuale per il nodo Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="e39ed-257">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="e39ed-258">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e39ed-258">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="e39ed-259">Questo parametro è valido solo per i cluster HBase o Storm.</span><span class="sxs-lookup"><span data-stu-id="e39ed-259">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39ed-260">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e39ed-260">CommonParameters</span></span>
<span data-ttu-id="e39ed-261">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e39ed-261">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e39ed-262">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e39ed-262">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e39ed-263">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e39ed-263">INPUTS</span></span>

### <span data-ttu-id="e39ed-264">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e39ed-264">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="e39ed-265">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e39ed-265">OUTPUTS</span></span>

### <span data-ttu-id="e39ed-266">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e39ed-266">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="e39ed-267">Note</span><span class="sxs-lookup"><span data-stu-id="e39ed-267">NOTES</span></span>
<span data-ttu-id="e39ed-268">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Hadoop, HDInsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="e39ed-268">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="e39ed-269">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e39ed-269">RELATED LINKS</span></span>

[<span data-ttu-id="e39ed-270">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e39ed-270">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

