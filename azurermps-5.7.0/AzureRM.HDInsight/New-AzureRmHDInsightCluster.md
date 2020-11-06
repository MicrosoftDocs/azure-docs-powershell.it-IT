---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
ms.openlocfilehash: 2e778f84eabf7e5dc4dd325d2a17361064c5d99f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521919"
---
# <span data-ttu-id="8292d-101">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8292d-101">New-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="8292d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8292d-102">SYNOPSIS</span></span>
<span data-ttu-id="8292d-103">Crea un cluster di Azure HDInsight nel gruppo di risorse specificato per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="8292d-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8292d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8292d-104">SYNTAX</span></span>

### <span data-ttu-id="8292d-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8292d-105">Default (Default)</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificatePassword <String>] [-AadTenantId <Guid>]
 [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8292d-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="8292d-106">CertificateFilePath</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8292d-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="8292d-107">CertificateFileContents</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8292d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8292d-108">DESCRIPTION</span></span>
<span data-ttu-id="8292d-109">La New-AzureHDInsightCluster crea un cluster di Azure HDInsight usando i parametri specificati o usando un oggetto Configuration creato usando il cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="8292d-109">The New-AzureHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="8292d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8292d-110">EXAMPLES</span></span>

### <span data-ttu-id="8292d-111">--------------------------Esempio 1: creare un cluster di Azure HDInsight--------------------------</span><span class="sxs-lookup"><span data-stu-id="8292d-111">--------------------------  Example 1: Create an Azure HDInsight cluster  --------------------------</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzureStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzureRmHDInsightCluster `
            -ClusterType Hadoop `
            -OSType Windows `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="8292d-112">Questo comando crea un cluster nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="8292d-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="8292d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8292d-113">PARAMETERS</span></span>

### <span data-ttu-id="8292d-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="8292d-114">-AadTenantId</span></span>
<span data-ttu-id="8292d-115">Specifica l'ID tenant di Azure AD che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8292d-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="8292d-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="8292d-117">Specifica gli account di archiviazione di Azure aggiuntivi per il cluster.</span><span class="sxs-lookup"><span data-stu-id="8292d-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="8292d-118">In alternativa, puoi usare il cmdlet Add-AzureRmHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="8292d-118">You can alternatively use the Add-AzureRmHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="8292d-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="8292d-119">-CertificateFileContents</span></span>
<span data-ttu-id="8292d-120">Specifica il contenuto del file del certificato che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8292d-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Byte[]
Parameter Sets: CertificateFileContents
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="8292d-121">-CertificateFilePath</span></span>
<span data-ttu-id="8292d-122">Specifica il percorso del file del certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="8292d-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="8292d-123">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8292d-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: CertificateFilePath
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="8292d-124">-CertificatePassword</span></span>
<span data-ttu-id="8292d-125">Specifica la password per il certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="8292d-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="8292d-126">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8292d-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-127">-Clustername</span><span class="sxs-lookup"><span data-stu-id="8292d-127">-ClusterName</span></span>
<span data-ttu-id="8292d-128">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="8292d-128">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-129">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="8292d-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="8292d-130">Specifica il numero di nodi di lavoro per il cluster.</span><span class="sxs-lookup"><span data-stu-id="8292d-130">Specifies the number of Worker nodes for the cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="8292d-131">-ClusterTier</span></span>
<span data-ttu-id="8292d-132">Specifica il livello del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8292d-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="8292d-133">Per impostazione predefinita, è standard.</span><span class="sxs-lookup"><span data-stu-id="8292d-133">By default, this is Standard.</span></span>
<span data-ttu-id="8292d-134">Il livello Premium può essere usato solo con i cluster Linux e consente l'uso di alcune nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="8292d-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Tier
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-135">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="8292d-135">-ClusterType</span></span>
<span data-ttu-id="8292d-136">Specifica il tipo di cluster da creare.</span><span class="sxs-lookup"><span data-stu-id="8292d-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="8292d-137">Le opzioni disponibili sono: Hadoop, HBase, Storm, Spark</span><span class="sxs-lookup"><span data-stu-id="8292d-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="8292d-138">-ComponentVersion</span></span>
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

### <span data-ttu-id="8292d-139">-Config</span><span class="sxs-lookup"><span data-stu-id="8292d-139">-Config</span></span>
<span data-ttu-id="8292d-140">Specifica l'oggetto cluster da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="8292d-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="8292d-141">Questo oggetto può essere creato usando il cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="8292d-141">This object can be created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-142">-Configurazioni</span><span class="sxs-lookup"><span data-stu-id="8292d-142">-Configurations</span></span>
<span data-ttu-id="8292d-143">Specifica le configurazioni di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8292d-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="8292d-144">In alternativa, puoi usare il cmdlet Add-AzureRmHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="8292d-144">You can alternatively use the Add-AzureRmHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="8292d-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8292d-145">-DefaultProfile</span></span>
<span data-ttu-id="8292d-146">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8292d-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8292d-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="8292d-148">Specifica la chiave dell'account per l'account di archiviazione di Azure predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8292d-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="8292d-149">In alternativa, puoi usare il cmdlet Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="8292d-149">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8292d-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="8292d-151">Specifica il nome dell'account di archiviazione di Azure predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8292d-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="8292d-152">In alternativa, puoi usare il cmdlet Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="8292d-152">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="8292d-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="8292d-154">Specifica il tipo di account di archiviazione predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8292d-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="8292d-155">I valori possibili sono AzureStorage e AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="8292d-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="8292d-156">Il valore predefinito è AzureStorage se non è specificato.</span><span class="sxs-lookup"><span data-stu-id="8292d-156">Defaults to AzureStorage if not specified.</span></span>

```yaml
Type: StorageType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8292d-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="8292d-158">Specifica il nome del contenitore predefinito nell'account di archiviazione di Azure predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8292d-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="8292d-159">In alternativa, puoi usare il cmdlet Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="8292d-159">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="8292d-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="8292d-161">Specifica il prefisso Path nell'account dello Store Data Lake che verrà usato dal cluster HDInsight come filesystem predefinito.</span><span class="sxs-lookup"><span data-stu-id="8292d-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-162">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="8292d-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="8292d-163">Specifica il numero di dischi per il ruolo di nodo di lavoro nel cluster.</span><span class="sxs-lookup"><span data-stu-id="8292d-163">Specifies the number of disks for worker node role in the cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="8292d-164">-EdgeNodeSize</span></span>
<span data-ttu-id="8292d-165">Specifica le dimensioni della macchina virtuale per il nodo Edge.</span><span class="sxs-lookup"><span data-stu-id="8292d-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="8292d-166">Usare Get-AzureRmVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8292d-166">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="8292d-167">Questo parametro è valido solo per i cluster RServer.</span><span class="sxs-lookup"><span data-stu-id="8292d-167">This parameter is valid only for RServer clusters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-168">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="8292d-168">-HeadNodeSize</span></span>
<span data-ttu-id="8292d-169">Specifica le dimensioni della macchina virtuale per il nodo head.</span><span class="sxs-lookup"><span data-stu-id="8292d-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="8292d-170">Usare Get-AzureRmVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8292d-170">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-171">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="8292d-171">-HiveMetastore</span></span>
<span data-ttu-id="8292d-172">Specifica il database SQL per archiviare i metadati hive.</span><span class="sxs-lookup"><span data-stu-id="8292d-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="8292d-173">In alternativa, puoi usare il cmdlet Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="8292d-173">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: AzureHDInsightMetastore
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="8292d-174">-HttpCredential</span></span>
<span data-ttu-id="8292d-175">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="8292d-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-176">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8292d-176">-Location</span></span>
<span data-ttu-id="8292d-177">Specifica la posizione per il cluster.</span><span class="sxs-lookup"><span data-stu-id="8292d-177">Specifies the location for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-178">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8292d-178">-ObjectId</span></span>
<span data-ttu-id="8292d-179">Specifica l'ID oggetto Azure AD (GUID) dell'entità servizio Azure AD che rappresenta il cluster.</span><span class="sxs-lookup"><span data-stu-id="8292d-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="8292d-180">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8292d-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-181">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="8292d-181">-OozieMetastore</span></span>
<span data-ttu-id="8292d-182">Specifica il database SQL per archiviare i metadati di oozie.</span><span class="sxs-lookup"><span data-stu-id="8292d-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="8292d-183">In alternativa, puoi usare il cmdlet Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="8292d-183">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: AzureHDInsightMetastore
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="8292d-184">-OSType</span></span>
<span data-ttu-id="8292d-185">Specifica il sistema operativo per il cluster.</span><span class="sxs-lookup"><span data-stu-id="8292d-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="8292d-186">Le opzioni disponibili sono: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="8292d-186">Options are: Windows, Linux</span></span>

```yaml
Type: OSType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-187">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="8292d-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="8292d-188">Specifica la scadenza, come oggetto DateTime, per l'accesso RDP (Remote Desktop Protocol) a un cluster.</span><span class="sxs-lookup"><span data-stu-id="8292d-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="8292d-189">-RdpCredential</span></span>
<span data-ttu-id="8292d-190">Specifica le credenziali remote desktop (RDP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="8292d-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="8292d-191">Questo è solo per i cluster Windows.</span><span class="sxs-lookup"><span data-stu-id="8292d-191">This is only for Windows clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8292d-192">-ResourceGroupName</span></span>
<span data-ttu-id="8292d-193">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8292d-193">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-194">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="8292d-194">-ScriptActions</span></span>
<span data-ttu-id="8292d-195">Specifica le azioni di script da eseguire nel cluster alla fine della creazione del cluster.</span><span class="sxs-lookup"><span data-stu-id="8292d-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="8292d-196">In alternativa, è possibile usare Add-AzureRmHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="8292d-196">You can alternatively use Add-AzureRmHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="8292d-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="8292d-197">-SecurityProfile</span></span>
<span data-ttu-id="8292d-198">Specifica le proprietà correlate alla sicurezza usate per creare un cluster sicuro.</span><span class="sxs-lookup"><span data-stu-id="8292d-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="8292d-199">In alternativa, puoi usare il cmdlet Add-AzureRmHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="8292d-199">You can alternatively use the Add-AzureRmHDInsightSecurityProfile cmdlet.</span></span>

```yaml
Type: AzureHDInsightSecurityProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="8292d-200">-SshCredential</span></span>
<span data-ttu-id="8292d-201">Specifica le credenziali SSH da usare per le connessioni SSH.</span><span class="sxs-lookup"><span data-stu-id="8292d-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="8292d-202">Questo è solo per i cluster Linux.</span><span class="sxs-lookup"><span data-stu-id="8292d-202">This is only for Linux clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="8292d-203">-SshPublicKey</span></span>
<span data-ttu-id="8292d-204">Specifica la chiave pubblica da usare per le connessioni SSH.</span><span class="sxs-lookup"><span data-stu-id="8292d-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="8292d-205">Questo è solo per i cluster Linux.</span><span class="sxs-lookup"><span data-stu-id="8292d-205">This is only for Linux clusters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-206">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="8292d-206">-SubnetName</span></span>
<span data-ttu-id="8292d-207">Specifica il nome di una subnet nella rete virtuale selezionata per il cluster.</span><span class="sxs-lookup"><span data-stu-id="8292d-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-208">-Versione</span><span class="sxs-lookup"><span data-stu-id="8292d-208">-Version</span></span>
<span data-ttu-id="8292d-209">Specifica la versione HDI del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8292d-209">Specifies the HDI version of the HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-210">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="8292d-210">-VirtualNetworkId</span></span>
<span data-ttu-id="8292d-211">Specifica l'ID della rete virtuale in cui eseguire il provisioning del cluster.</span><span class="sxs-lookup"><span data-stu-id="8292d-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-212">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="8292d-212">-WorkerNodeSize</span></span>
<span data-ttu-id="8292d-213">Specifica le dimensioni della macchina virtuale per il nodo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8292d-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="8292d-214">Usare Get-AzureRmVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8292d-214">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="8292d-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="8292d-216">Specifica le dimensioni della macchina virtuale per il nodo Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="8292d-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="8292d-217">Usare Get-AzureRmVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8292d-217">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="8292d-218">Questo parametro è valido solo per i cluster HBase o Storm.</span><span class="sxs-lookup"><span data-stu-id="8292d-218">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8292d-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8292d-219">CommonParameters</span></span>
<span data-ttu-id="8292d-220">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8292d-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8292d-221">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8292d-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8292d-222">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8292d-222">INPUTS</span></span>

### <span data-ttu-id="8292d-223">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="8292d-223">AzureHDInsightConfig</span></span>
<span data-ttu-id="8292d-224">Il parametro ' config ' accetta il valore di tipo ' AzureHDInsightConfig ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8292d-224">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="8292d-225">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8292d-225">OUTPUTS</span></span>

### <span data-ttu-id="8292d-226">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8292d-226">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="8292d-227">Note</span><span class="sxs-lookup"><span data-stu-id="8292d-227">NOTES</span></span>
<span data-ttu-id="8292d-228">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Hadoop, HDInsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="8292d-228">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="8292d-229">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8292d-229">RELATED LINKS</span></span>

[<span data-ttu-id="8292d-230">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="8292d-230">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

