---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: 94b982eb2add8341b861732bef5e63d88e67a937
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009054"
---
# <span data-ttu-id="e3cd6-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e3cd6-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="e3cd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="e3cd6-103">Crea un cluster Azure HDInsight nel gruppo di risorse specificato per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="e3cd6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3cd6-104">SYNTAX</span></span>

### <span data-ttu-id="e3cd6-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3cd6-105">Default (Default)</span></span>
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
 [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3cd6-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e3cd6-106">CertificateFilePath</span></span>
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
 [-PrivateLink <String>] [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3cd6-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="e3cd6-107">CertificateFileContents</span></span>
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
 [-PrivateLink <String>] [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3cd6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3cd6-108">DESCRIPTION</span></span>
<span data-ttu-id="e3cd6-109">LNew-AzHDInsightCluster crea un cluster HDInsight di Azure usando i parametri specificati o usando un oggetto di configurazione creato con il cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="e3cd6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3cd6-110">EXAMPLES</span></span>

### <span data-ttu-id="e3cd6-111">Esempio 1: Creare un cluster Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="e3cd6-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

<span data-ttu-id="e3cd6-112">Questo comando crea un cluster nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="e3cd6-113">Esempio 2: Creare un cluster con crittografia disco della chiave gestita dal cliente</span><span class="sxs-lookup"><span data-stu-id="e3cd6-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="e3cd6-114">Esempio 3: Creare un cluster Azure HDInsight che abilita la crittografia in transito</span><span class="sxs-lookup"><span data-stu-id="e3cd6-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}}
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

### <span data-ttu-id="e3cd6-115">Esempio 4: Creare un cluster Azure HDInsight con funzionalità di collegamento privato e in uscita di inoltro</span><span class="sxs-lookup"><span data-stu-id="e3cd6-115">Example 4: Create an Azure HDInsight cluster with relay outbound and private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="e3cd6-116">Esempio 5: Creare un cluster Azure HDInsight che abilita la crittografia nell'host</span><span class="sxs-lookup"><span data-stu-id="e3cd6-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="e3cd6-117">Esempio 6: Creare un cluster Azure HDInsight che abilita la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="e3cd6-118">Esempio 7: Creare un cluster Azure HDInsight con proxy Rest di Kafka.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="e3cd6-119">Esempio 8: Creare un cluster Azure HDInsight con archiviazione di Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
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

### <span data-ttu-id="e3cd6-120">Esempio 9: Creare un cluster Azure HDInsight con il pacchetto di sicurezza enterprise (ESP) e abilitare il broker ID HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
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

### <span data-ttu-id="e3cd6-121">Esempio 10: Creare un cluster Azure HDInsight che consente l'isolamento del calcolo.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-121">Example 10: Create an Azure HDInsight cluster which enables compute isolation.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential
        $workerNodeSize="Standard_E16S_V3" # here is just an example
        $headNodeSize="Standard_E8S_V3"
        $zookeeperNodeSize="Standard_E2S_V3"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -WorkerNodeSize $workerNodeSize `
            -HeadNodeSize $headNodeSize `
            -ZookeeperNodeSize $zookeeperNodeSize `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EnableComputeIsolation `
```

## <span data-ttu-id="e3cd6-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3cd6-122">PARAMETERS</span></span>

### <span data-ttu-id="e3cd6-123">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="e3cd6-123">-AadTenantId</span></span>
<span data-ttu-id="e3cd6-124">Specifica l'ID tenant di Azure AD che verrà usato quando si accede ad Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-124">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e3cd6-125">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="e3cd6-125">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="e3cd6-126">Specifica gli altri account di Archiviazione di Azure per il cluster.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-126">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="e3cd6-127">In alternativa, è possibile usare Add-AzHDInsightStorage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-127">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="e3cd6-128">-AmbariDatabase</span><span class="sxs-lookup"><span data-stu-id="e3cd6-128">-AmbariDatabase</span></span>
<span data-ttu-id="e3cd6-129">Ottiene o imposta il database per gli ambari.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-129">Gets or sets the database for ambari.</span></span>

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

### <span data-ttu-id="e3cd6-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e3cd6-130">-ApplicationId</span></span>
<span data-ttu-id="e3cd6-131">Ottiene o imposta l'ID applicazione entità servizio per l'accesso ad Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-131">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="e3cd6-132">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e3cd6-132">-AssignedIdentity</span></span>
<span data-ttu-id="e3cd6-133">Ottiene o imposta l'identità assegnata.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-133">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="e3cd6-134">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3cd6-134">-AutoscaleConfiguration</span></span>
<span data-ttu-id="e3cd6-135">Ottiene o imposta la configurazione di gradazioni automatica</span><span class="sxs-lookup"><span data-stu-id="e3cd6-135">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="e3cd6-136">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="e3cd6-136">-CertificateFileContents</span></span>
<span data-ttu-id="e3cd6-137">Specifica il contenuto del file del certificato che verrà usato quando si accede ad Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-137">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e3cd6-138">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e3cd6-138">-CertificateFilePath</span></span>
<span data-ttu-id="e3cd6-139">Specifica il percorso del file del certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-139">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e3cd6-140">Il cluster userà questa impostazione per l'accesso ad Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-140">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e3cd6-141">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e3cd6-141">-CertificatePassword</span></span>
<span data-ttu-id="e3cd6-142">Specifica la password per il certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-142">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e3cd6-143">Il cluster userà questa impostazione per l'accesso ad Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-143">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e3cd6-144">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e3cd6-144">-ClusterName</span></span>
<span data-ttu-id="e3cd6-145">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-145">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e3cd6-146">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="e3cd6-146">-ClusterSizeInNodes</span></span>
<span data-ttu-id="e3cd6-147">Specifica il numero di nodi di lavoro per il cluster.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-147">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="e3cd6-148">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="e3cd6-148">-ClusterTier</span></span>
<span data-ttu-id="e3cd6-149">Specifica il livello cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-149">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="e3cd6-150">Per impostazione predefinita, questo campo è Standard.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-150">By default, this is Standard.</span></span>
<span data-ttu-id="e3cd6-151">Il livello Premium può essere usato solo con cluster Linux e consente l'uso di alcune nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-151">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="e3cd6-152">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="e3cd6-152">-ClusterType</span></span>
<span data-ttu-id="e3cd6-153">Specifica il tipo di cluster da creare.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-153">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="e3cd6-154">Le opzioni disponibili sono: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka e RServer</span><span class="sxs-lookup"><span data-stu-id="e3cd6-154">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="e3cd6-155">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="e3cd6-155">-ComponentVersion</span></span>
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

### <span data-ttu-id="e3cd6-156">-ComputeIsolationHostSku</span><span class="sxs-lookup"><span data-stu-id="e3cd6-156">-ComputeIsolationHostSku</span></span>
<span data-ttu-id="e3cd6-157">Ottiene o imposta la SKU host dedicata per l'isolamento del calcolo.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-157">Gets or sets the dedicated host sku for compute isolation.</span></span>

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

### <span data-ttu-id="e3cd6-158">-Config</span><span class="sxs-lookup"><span data-stu-id="e3cd6-158">-Config</span></span>
<span data-ttu-id="e3cd6-159">Specifica l'oggetto cluster da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-159">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="e3cd6-160">Questo oggetto può essere creato con il cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-160">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="e3cd6-161">-Configurations</span><span class="sxs-lookup"><span data-stu-id="e3cd6-161">-Configurations</span></span>
<span data-ttu-id="e3cd6-162">Specifica le configurazioni di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-162">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="e3cd6-163">In alternativa, è possibile usare Add-AzHDInsightConfigValues cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-163">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="e3cd6-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3cd6-164">-DefaultProfile</span></span>
<span data-ttu-id="e3cd6-165">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e3cd6-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3cd6-166">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="e3cd6-166">-DisksPerWorkerNode</span></span>
<span data-ttu-id="e3cd6-167">Specifica il numero di dischi per il ruolo di nodo di lavoro nel cluster.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-167">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="e3cd6-168">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="e3cd6-168">-EdgeNodeSize</span></span>
<span data-ttu-id="e3cd6-169">Specifica le dimensioni della macchina virtuale per il nodo Edge.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-169">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="e3cd6-170">Usa Get-AzVMSize per dimensioni accettabili di VM e consulta la pagina dei prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-170">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="e3cd6-171">Questo parametro è valido solo per i cluster RServer.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-171">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="e3cd6-172">-EnableComputeIsolation</span><span class="sxs-lookup"><span data-stu-id="e3cd6-172">-EnableComputeIsolation</span></span>
<span data-ttu-id="e3cd6-173">Abilita la funzionalità di isolamento dei calcoli HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-173">Enables HDInsight compute isolation feature.</span></span>

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

### <span data-ttu-id="e3cd6-174">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="e3cd6-174">-EnableIDBroker</span></span>
<span data-ttu-id="e3cd6-175">Abilita la funzionalità del broker di identità HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-175">Enables HDInsight Identity Broker feature.</span></span>

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

### <span data-ttu-id="e3cd6-176">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e3cd6-176">-EncryptionAlgorithm</span></span>
<span data-ttu-id="e3cd6-177">Ottiene o imposta l'algoritmo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-177">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="e3cd6-178">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="e3cd6-178">-EncryptionAtHost</span></span>
<span data-ttu-id="e3cd6-179">Ottiene o imposta il flag che indica se abilitare o meno la crittografia nell'host.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-179">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="e3cd6-180">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="e3cd6-180">-EncryptionInTransit</span></span>
<span data-ttu-id="e3cd6-181">Ottiene o imposta il flag che indica se abilitare o meno la crittografia in transito.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-181">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="e3cd6-182">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="e3cd6-182">-EncryptionKeyName</span></span>
<span data-ttu-id="e3cd6-183">Ottiene o imposta il nome della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-183">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="e3cd6-184">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="e3cd6-184">-EncryptionKeyVersion</span></span>
<span data-ttu-id="e3cd6-185">Ottiene o imposta la versione della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-185">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="e3cd6-186">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="e3cd6-186">-EncryptionVaultUri</span></span>
<span data-ttu-id="e3cd6-187">Ottiene o imposta l'URI del vault di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-187">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="e3cd6-188">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="e3cd6-188">-HeadNodeSize</span></span>
<span data-ttu-id="e3cd6-189">Specifica le dimensioni della macchina virtuale per il nodo Head.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-189">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="e3cd6-190">Usa Get-AzVMSize per dimensioni accettabili di VM e consulta la pagina dei prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-190">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="e3cd6-191">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="e3cd6-191">-HiveMetastore</span></span>
<span data-ttu-id="e3cd6-192">Specifica il database SQL in cui memorizzare i metadati Hive.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-192">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="e3cd6-193">In alternativa, è possibile usare Add-AzHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-193">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="e3cd6-194">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="e3cd6-194">-HttpCredential</span></span>
<span data-ttu-id="e3cd6-195">Specifica le credenziali di accesso del cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-195">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="e3cd6-196">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="e3cd6-196">-KafkaClientGroupId</span></span>
<span data-ttu-id="e3cd6-197">Ottiene o imposta l'ID gruppo client per l'accesso proxy Kafka Rest.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-197">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="e3cd6-198">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="e3cd6-198">-KafkaClientGroupName</span></span>
<span data-ttu-id="e3cd6-199">Ottiene o imposta il nome del gruppo client per l'accesso proxy Kafka Rest.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-199">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="e3cd6-200">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="e3cd6-200">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="e3cd6-201">Ottiene o imposta le dimensioni del nodo di gestione di Kafka.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-201">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="e3cd6-202">-Location</span><span class="sxs-lookup"><span data-stu-id="e3cd6-202">-Location</span></span>
<span data-ttu-id="e3cd6-203">Specifica la posizione del cluster.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-203">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="e3cd6-204">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="e3cd6-204">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="e3cd6-205">Ottiene o imposta la versione minima di TLS supportata.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-205">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="e3cd6-206">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e3cd6-206">-ObjectId</span></span>
<span data-ttu-id="e3cd6-207">Specifica l'ID oggetto di Azure AD (un GUID) dell'entità servizio di Azure AD che rappresenta il cluster.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-207">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="e3cd6-208">Il cluster userà questa impostazione per l'accesso ad Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-208">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e3cd6-209">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="e3cd6-209">-OozieMetastore</span></span>
<span data-ttu-id="e3cd6-210">Specifica l'SQL database in cui archiviare i metadati di Oozie.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-210">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="e3cd6-211">In alternativa, è possibile usare Add-AzHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-211">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="e3cd6-212">-OSType</span><span class="sxs-lookup"><span data-stu-id="e3cd6-212">-OSType</span></span>
<span data-ttu-id="e3cd6-213">Specifica il sistema operativo per il cluster.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-213">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="e3cd6-214">Le opzioni disponibili sono: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="e3cd6-214">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="e3cd6-215">-PrivateLink</span><span class="sxs-lookup"><span data-stu-id="e3cd6-215">-PrivateLink</span></span>
<span data-ttu-id="e3cd6-216">Ottiene o imposta il tipo di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-216">Gets or sets the private link type.</span></span>

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

### <span data-ttu-id="e3cd6-217">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="e3cd6-217">-RdpAccessExpiry</span></span>
<span data-ttu-id="e3cd6-218">Specifica la scadenza, come oggetto DateTime, per l'accesso RDP (Remote Desktop Protocol) a un cluster.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-218">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="e3cd6-219">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="e3cd6-219">-RdpCredential</span></span>
<span data-ttu-id="e3cd6-220">Specifica le credenziali di Desktop remoto (RDP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-220">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="e3cd6-221">Questo problema si applica solo ai cluster di Windows.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-221">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="e3cd6-222">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3cd6-222">-ResourceGroupName</span></span>
<span data-ttu-id="e3cd6-223">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-223">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e3cd6-224">-ResourceProviderConnection</span><span class="sxs-lookup"><span data-stu-id="e3cd6-224">-ResourceProviderConnection</span></span>
<span data-ttu-id="e3cd6-225">Ottiene o imposta il tipo di connessione del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-225">Gets or sets the resource provider connection type.</span></span>

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

### <span data-ttu-id="e3cd6-226">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="e3cd6-226">-ScriptActions</span></span>
<span data-ttu-id="e3cd6-227">Specifica le azioni script da eseguire sul cluster al termine della creazione del cluster.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-227">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="e3cd6-228">In alternativa, è possibile usare Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-228">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="e3cd6-229">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="e3cd6-229">-SecurityProfile</span></span>
<span data-ttu-id="e3cd6-230">Specifica le proprietà correlate alla sicurezza usate per creare un cluster sicuro.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-230">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="e3cd6-231">In alternativa, è possibile usare Add-AzHDInsightSecurityProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-231">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="e3cd6-232">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="e3cd6-232">-SshCredential</span></span>
<span data-ttu-id="e3cd6-233">Specifica le credenziali SSH da usare per le connessioni SSH.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-233">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="e3cd6-234">Questo problema si applica solo ai cluster Linux.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-234">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="e3cd6-235">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e3cd6-235">-SshPublicKey</span></span>
<span data-ttu-id="e3cd6-236">Specifica la chiave pubblica da usare per le connessioni SSH.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-236">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="e3cd6-237">Questo problema si applica solo ai cluster Linux.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-237">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="e3cd6-238">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e3cd6-238">-StorageAccountKey</span></span>
<span data-ttu-id="e3cd6-239">Ottiene o imposta la chiave di accesso dell'account di archiviazione per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-239">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="e3cd6-240">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="e3cd6-240">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="e3cd6-241">Ottiene o imposta l'identità gestita dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-241">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="e3cd6-242">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="e3cd6-242">-StorageAccountResourceId</span></span>
<span data-ttu-id="e3cd6-243">Ottiene o imposta l'ID della risorsa di archiviazione per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-243">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="e3cd6-244">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e3cd6-244">-StorageAccountType</span></span>
<span data-ttu-id="e3cd6-245">Ottiene o imposta il tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-245">Gets or sets the type of the storage account.</span></span>

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

### <span data-ttu-id="e3cd6-246">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="e3cd6-246">-StorageContainer</span></span>
<span data-ttu-id="e3cd6-247">Ottiene o imposta il nome StorageContainer per l'account di archiviazione di Azure predefinito</span><span class="sxs-lookup"><span data-stu-id="e3cd6-247">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="e3cd6-248">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="e3cd6-248">-StorageFileSystem</span></span>
<span data-ttu-id="e3cd6-249">Ottiene o imposta il file system per l'account predefinito Azure Data Lake Storage Gen2.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-249">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="e3cd6-250">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="e3cd6-250">-StorageRootPath</span></span>
<span data-ttu-id="e3cd6-251">Ottiene o imposta il percorso alla radice del cluster nell'account predefinito Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-251">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="e3cd6-252">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="e3cd6-252">-SubnetName</span></span>
<span data-ttu-id="e3cd6-253">Ottiene o imposta il nome della subnet per questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-253">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="e3cd6-254">-Version</span><span class="sxs-lookup"><span data-stu-id="e3cd6-254">-Version</span></span>
<span data-ttu-id="e3cd6-255">Specifica la versione HDI del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-255">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="e3cd6-256">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e3cd6-256">-VirtualNetworkId</span></span>
<span data-ttu-id="e3cd6-257">Specifica l'ID della rete virtuale in cui effettuare il provisioning del cluster.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-257">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="e3cd6-258">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="e3cd6-258">-WorkerNodeSize</span></span>
<span data-ttu-id="e3cd6-259">Specifica le dimensioni della macchina virtuale per il nodo Worker.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-259">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="e3cd6-260">Usa Get-AzVMSize per dimensioni accettabili di VM e consulta la pagina dei prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-260">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="e3cd6-261">-MetriakeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="e3cd6-261">-ZookeeperNodeSize</span></span>
<span data-ttu-id="e3cd6-262">Specifica le dimensioni della macchina virtuale per il nodo Guardiano.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-262">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="e3cd6-263">Usa Get-AzVMSize per dimensioni accettabili di VM e consulta la pagina dei prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-263">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="e3cd6-264">Questo parametro è valido solo per cluster HBase o Storm.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-264">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="e3cd6-265">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3cd6-265">CommonParameters</span></span>
<span data-ttu-id="e3cd6-266">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-266">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3cd6-267">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3cd6-267">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3cd6-268">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3cd6-268">INPUTS</span></span>

### <span data-ttu-id="e3cd6-269">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e3cd6-269">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="e3cd6-270">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3cd6-270">OUTPUTS</span></span>

### <span data-ttu-id="e3cd6-271">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e3cd6-271">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="e3cd6-272">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3cd6-272">NOTES</span></span>
<span data-ttu-id="e3cd6-273">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, hadoop, hdinsight, hd, insight</span><span class="sxs-lookup"><span data-stu-id="e3cd6-273">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="e3cd6-274">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3cd6-274">RELATED LINKS</span></span>

[<span data-ttu-id="e3cd6-275">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e3cd6-275">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

