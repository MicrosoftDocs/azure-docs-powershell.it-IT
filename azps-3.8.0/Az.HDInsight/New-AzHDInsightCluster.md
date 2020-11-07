---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: c0d3d6518025aab22add0859bde69cb1ad279138
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865459"
---
# <span data-ttu-id="ec16d-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ec16d-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="ec16d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec16d-102">SYNOPSIS</span></span>
<span data-ttu-id="ec16d-103">Crea un cluster di Azure HDInsight nel gruppo di risorse specificato per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="ec16d-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="ec16d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec16d-104">SYNTAX</span></span>

### <span data-ttu-id="ec16d-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ec16d-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>] [[-SecurityProfile] <AzureHDInsightSecurityProfile>]
 [[-DisksPerWorkerNode] <Int32>] [[-MinSupportedTlsVersion] <String>]
 [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec16d-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="ec16d-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificateFilePath] <String>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-SecurityProfile] <AzureHDInsightSecurityProfile>] [[-DisksPerWorkerNode] <Int32>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec16d-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="ec16d-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificateFileContents] <Byte[]>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-SecurityProfile] <AzureHDInsightSecurityProfile>] [[-DisksPerWorkerNode] <Int32>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec16d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec16d-108">DESCRIPTION</span></span>
<span data-ttu-id="ec16d-109">La New-AzHDInsightCluster crea un cluster di Azure HDInsight usando i parametri specificati o usando un oggetto Configuration creato usando il cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="ec16d-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="ec16d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec16d-110">EXAMPLES</span></span>

### <span data-ttu-id="ec16d-111">Esempio 1: creare un cluster di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="ec16d-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
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
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
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

<span data-ttu-id="ec16d-112">Questo comando crea un cluster nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="ec16d-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="ec16d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec16d-113">PARAMETERS</span></span>

### <span data-ttu-id="ec16d-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="ec16d-114">-AadTenantId</span></span>
<span data-ttu-id="ec16d-115">Specifica l'ID tenant di Azure AD che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec16d-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ec16d-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="ec16d-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="ec16d-117">Specifica gli account di archiviazione di Azure aggiuntivi per il cluster.</span><span class="sxs-lookup"><span data-stu-id="ec16d-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="ec16d-118">In alternativa, puoi usare il cmdlet Add-AzHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="ec16d-118">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="ec16d-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ec16d-119">-ApplicationId</span></span>
<span data-ttu-id="ec16d-120">Ottiene o imposta l'ID dell'applicazione Principal del servizio per l'accesso a Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="ec16d-120">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="ec16d-121">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="ec16d-121">-CertificateFileContents</span></span>
<span data-ttu-id="ec16d-122">Specifica il contenuto del file del certificato che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec16d-122">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ec16d-123">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="ec16d-123">-CertificateFilePath</span></span>
<span data-ttu-id="ec16d-124">Specifica il percorso del file del certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="ec16d-124">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="ec16d-125">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec16d-125">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ec16d-126">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="ec16d-126">-CertificatePassword</span></span>
<span data-ttu-id="ec16d-127">Specifica la password per il certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="ec16d-127">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="ec16d-128">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec16d-128">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ec16d-129">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ec16d-129">-ClusterName</span></span>
<span data-ttu-id="ec16d-130">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="ec16d-130">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ec16d-131">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="ec16d-131">-ClusterSizeInNodes</span></span>
<span data-ttu-id="ec16d-132">Specifica il numero di nodi di lavoro per il cluster.</span><span class="sxs-lookup"><span data-stu-id="ec16d-132">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="ec16d-133">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="ec16d-133">-ClusterTier</span></span>
<span data-ttu-id="ec16d-134">Specifica il livello del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ec16d-134">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="ec16d-135">Per impostazione predefinita, è standard.</span><span class="sxs-lookup"><span data-stu-id="ec16d-135">By default, this is Standard.</span></span>
<span data-ttu-id="ec16d-136">Il livello Premium può essere usato solo con i cluster Linux e consente l'uso di alcune nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ec16d-136">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="ec16d-137">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="ec16d-137">-ClusterType</span></span>
<span data-ttu-id="ec16d-138">Specifica il tipo di cluster da creare.</span><span class="sxs-lookup"><span data-stu-id="ec16d-138">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="ec16d-139">Le opzioni disponibili sono: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka e RServer</span><span class="sxs-lookup"><span data-stu-id="ec16d-139">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="ec16d-140">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="ec16d-140">-ComponentVersion</span></span>
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

### <span data-ttu-id="ec16d-141">-Config</span><span class="sxs-lookup"><span data-stu-id="ec16d-141">-Config</span></span>
<span data-ttu-id="ec16d-142">Specifica l'oggetto cluster da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="ec16d-142">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="ec16d-143">Questo oggetto può essere creato usando il cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="ec16d-143">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="ec16d-144">-Configurazioni</span><span class="sxs-lookup"><span data-stu-id="ec16d-144">-Configurations</span></span>
<span data-ttu-id="ec16d-145">Specifica le configurazioni di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ec16d-145">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="ec16d-146">In alternativa, puoi usare il cmdlet Add-AzHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="ec16d-146">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="ec16d-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec16d-147">-DefaultProfile</span></span>
<span data-ttu-id="ec16d-148">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ec16d-148">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec16d-149">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ec16d-149">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="ec16d-150">Specifica la chiave dell'account per l'account di archiviazione di Azure predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ec16d-150">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="ec16d-151">In alternativa, puoi usare il cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="ec16d-151">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="ec16d-152">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ec16d-152">-DefaultStorageAccountName</span></span>
<span data-ttu-id="ec16d-153">Specifica il nome dell'account di archiviazione di Azure predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ec16d-153">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="ec16d-154">In alternativa, puoi usare il cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="ec16d-154">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="ec16d-155">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ec16d-155">-DefaultStorageAccountType</span></span>
<span data-ttu-id="ec16d-156">Specifica il tipo di account di archiviazione predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ec16d-156">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="ec16d-157">I valori possibili sono AzureStorage e AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="ec16d-157">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="ec16d-158">Il valore predefinito è AzureStorage se non è specificato.</span><span class="sxs-lookup"><span data-stu-id="ec16d-158">Defaults to AzureStorage if not specified.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec16d-159">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ec16d-159">-DefaultStorageContainer</span></span>
<span data-ttu-id="ec16d-160">Specifica il nome del contenitore predefinito nell'account di archiviazione di Azure predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ec16d-160">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="ec16d-161">In alternativa, puoi usare il cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="ec16d-161">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="ec16d-162">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="ec16d-162">-DefaultStorageRootPath</span></span>
<span data-ttu-id="ec16d-163">Specifica il prefisso Path nell'account dello Store Data Lake che verrà usato dal cluster HDInsight come filesystem predefinito.</span><span class="sxs-lookup"><span data-stu-id="ec16d-163">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="ec16d-164">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="ec16d-164">-DisksPerWorkerNode</span></span>
<span data-ttu-id="ec16d-165">Specifica il numero di dischi per il ruolo di nodo di lavoro nel cluster.</span><span class="sxs-lookup"><span data-stu-id="ec16d-165">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="ec16d-166">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="ec16d-166">-EdgeNodeSize</span></span>
<span data-ttu-id="ec16d-167">Specifica le dimensioni della macchina virtuale per il nodo Edge.</span><span class="sxs-lookup"><span data-stu-id="ec16d-167">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="ec16d-168">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ec16d-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="ec16d-169">Questo parametro è valido solo per i cluster RServer.</span><span class="sxs-lookup"><span data-stu-id="ec16d-169">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="ec16d-170">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="ec16d-170">-HeadNodeSize</span></span>
<span data-ttu-id="ec16d-171">Specifica le dimensioni della macchina virtuale per il nodo head.</span><span class="sxs-lookup"><span data-stu-id="ec16d-171">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="ec16d-172">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ec16d-172">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="ec16d-173">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="ec16d-173">-HiveMetastore</span></span>
<span data-ttu-id="ec16d-174">Specifica il database SQL per archiviare i metadati hive.</span><span class="sxs-lookup"><span data-stu-id="ec16d-174">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="ec16d-175">In alternativa, puoi usare il cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="ec16d-175">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="ec16d-176">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="ec16d-176">-HttpCredential</span></span>
<span data-ttu-id="ec16d-177">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="ec16d-177">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="ec16d-178">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ec16d-178">-Location</span></span>
<span data-ttu-id="ec16d-179">Specifica la posizione per il cluster.</span><span class="sxs-lookup"><span data-stu-id="ec16d-179">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="ec16d-180">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ec16d-180">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="ec16d-181">Ottiene o imposta la versione di TLS supportata minima.</span><span class="sxs-lookup"><span data-stu-id="ec16d-181">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="ec16d-182">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ec16d-182">-ObjectId</span></span>
<span data-ttu-id="ec16d-183">Specifica l'ID oggetto Azure AD (GUID) dell'entità servizio Azure AD che rappresenta il cluster.</span><span class="sxs-lookup"><span data-stu-id="ec16d-183">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="ec16d-184">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec16d-184">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ec16d-185">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="ec16d-185">-OozieMetastore</span></span>
<span data-ttu-id="ec16d-186">Specifica il database SQL per archiviare i metadati di oozie.</span><span class="sxs-lookup"><span data-stu-id="ec16d-186">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="ec16d-187">In alternativa, puoi usare il cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="ec16d-187">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="ec16d-188">-OSType</span><span class="sxs-lookup"><span data-stu-id="ec16d-188">-OSType</span></span>
<span data-ttu-id="ec16d-189">Specifica il sistema operativo per il cluster.</span><span class="sxs-lookup"><span data-stu-id="ec16d-189">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="ec16d-190">Le opzioni disponibili sono: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="ec16d-190">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="ec16d-191">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="ec16d-191">-RdpAccessExpiry</span></span>
<span data-ttu-id="ec16d-192">Specifica la scadenza, come oggetto DateTime, per l'accesso RDP (Remote Desktop Protocol) a un cluster.</span><span class="sxs-lookup"><span data-stu-id="ec16d-192">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="ec16d-193">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="ec16d-193">-RdpCredential</span></span>
<span data-ttu-id="ec16d-194">Specifica le credenziali remote desktop (RDP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="ec16d-194">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="ec16d-195">Questo è solo per i cluster Windows.</span><span class="sxs-lookup"><span data-stu-id="ec16d-195">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="ec16d-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec16d-196">-ResourceGroupName</span></span>
<span data-ttu-id="ec16d-197">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ec16d-197">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ec16d-198">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="ec16d-198">-ScriptActions</span></span>
<span data-ttu-id="ec16d-199">Specifica le azioni di script da eseguire nel cluster alla fine della creazione del cluster.</span><span class="sxs-lookup"><span data-stu-id="ec16d-199">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="ec16d-200">In alternativa, è possibile usare Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="ec16d-200">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="ec16d-201">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="ec16d-201">-SecurityProfile</span></span>
<span data-ttu-id="ec16d-202">Specifica le proprietà correlate alla sicurezza usate per creare un cluster sicuro.</span><span class="sxs-lookup"><span data-stu-id="ec16d-202">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="ec16d-203">In alternativa, puoi usare il cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="ec16d-203">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="ec16d-204">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="ec16d-204">-SshCredential</span></span>
<span data-ttu-id="ec16d-205">Specifica le credenziali SSH da usare per le connessioni SSH.</span><span class="sxs-lookup"><span data-stu-id="ec16d-205">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="ec16d-206">Questo è solo per i cluster Linux.</span><span class="sxs-lookup"><span data-stu-id="ec16d-206">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="ec16d-207">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="ec16d-207">-SshPublicKey</span></span>
<span data-ttu-id="ec16d-208">Specifica la chiave pubblica da usare per le connessioni SSH.</span><span class="sxs-lookup"><span data-stu-id="ec16d-208">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="ec16d-209">Questo è solo per i cluster Linux.</span><span class="sxs-lookup"><span data-stu-id="ec16d-209">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="ec16d-210">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="ec16d-210">-SubnetName</span></span>
<span data-ttu-id="ec16d-211">Specifica il nome di una subnet nella rete virtuale selezionata per il cluster.</span><span class="sxs-lookup"><span data-stu-id="ec16d-211">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="ec16d-212">-Versione</span><span class="sxs-lookup"><span data-stu-id="ec16d-212">-Version</span></span>
<span data-ttu-id="ec16d-213">Specifica la versione HDI del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ec16d-213">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="ec16d-214">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="ec16d-214">-VirtualNetworkId</span></span>
<span data-ttu-id="ec16d-215">Specifica l'ID della rete virtuale in cui eseguire il provisioning del cluster.</span><span class="sxs-lookup"><span data-stu-id="ec16d-215">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="ec16d-216">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="ec16d-216">-WorkerNodeSize</span></span>
<span data-ttu-id="ec16d-217">Specifica le dimensioni della macchina virtuale per il nodo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ec16d-217">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="ec16d-218">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ec16d-218">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="ec16d-219">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="ec16d-219">-ZookeeperNodeSize</span></span>
<span data-ttu-id="ec16d-220">Specifica le dimensioni della macchina virtuale per il nodo Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="ec16d-220">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="ec16d-221">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ec16d-221">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="ec16d-222">Questo parametro è valido solo per i cluster HBase o Storm.</span><span class="sxs-lookup"><span data-stu-id="ec16d-222">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="ec16d-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec16d-223">CommonParameters</span></span>
<span data-ttu-id="ec16d-224">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec16d-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec16d-225">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec16d-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec16d-226">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec16d-226">INPUTS</span></span>

### <span data-ttu-id="ec16d-227">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ec16d-227">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="ec16d-228">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec16d-228">OUTPUTS</span></span>

### <span data-ttu-id="ec16d-229">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ec16d-229">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="ec16d-230">Note</span><span class="sxs-lookup"><span data-stu-id="ec16d-230">NOTES</span></span>
<span data-ttu-id="ec16d-231">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Hadoop, HDInsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="ec16d-231">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="ec16d-232">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec16d-232">RELATED LINKS</span></span>

[<span data-ttu-id="ec16d-233">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="ec16d-233">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

