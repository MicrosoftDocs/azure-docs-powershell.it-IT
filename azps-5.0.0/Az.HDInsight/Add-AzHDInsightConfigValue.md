---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: 4de1a76d2c9ec2cba7dae67d26f73ef55a5f827f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193349"
---
# <span data-ttu-id="e0a6b-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="e0a6b-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="e0a6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="e0a6b-103">Aggiunge una personalizzazione del valore di configurazione Hadoop e/o una personalizzazione della raccolta condivisa hive a un oggetto di configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="e0a6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0a6b-104">SYNTAX</span></span>

```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-Spark2Defaults <Hashtable>]
 [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0a6b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0a6b-105">DESCRIPTION</span></span>
<span data-ttu-id="e0a6b-106">Il cmdlet **Add-AzHDInsightConfigValue** aggiunge una personalizzazione del valore di configurazione Hadoop, ad esempio core-site.xml o hive-site.xml, e/o una personalizzazione della raccolta condivisa hive per l'oggetto di configurazione HDInsight creato dal cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-106">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="e0a6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0a6b-107">EXAMPLES</span></span>

### <span data-ttu-id="e0a6b-108">Esempio 1: aggiungere un valore di configurazione personalizzato all'oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="e0a6b-108">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightConfigValue `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageAccountContainer
```

<span data-ttu-id="e0a6b-109">Questo comando aggiunge un valore di configurazione Hadoop al cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-109">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="e0a6b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0a6b-110">PARAMETERS</span></span>

### <span data-ttu-id="e0a6b-111">-Config</span><span class="sxs-lookup"><span data-stu-id="e0a6b-111">-Config</span></span>
<span data-ttu-id="e0a6b-112">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="e0a6b-113">Questo oggetto viene creato dal cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-113">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-114">-Core</span><span class="sxs-lookup"><span data-stu-id="e0a6b-114">-Core</span></span>
<span data-ttu-id="e0a6b-115">Specifica le configurazioni del sito principale di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-115">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0a6b-116">-DefaultProfile</span></span>
<span data-ttu-id="e0a6b-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e0a6b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0a6b-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="e0a6b-118">-HBaseEnv</span></span>
<span data-ttu-id="e0a6b-119">Specifica le configurazioni di HBase ENV di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="e0a6b-120">-HBaseSite</span></span>
<span data-ttu-id="e0a6b-121">Specifica le configurazioni del sito HBase di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-122">-HDFS</span><span class="sxs-lookup"><span data-stu-id="e0a6b-122">-Hdfs</span></span>
<span data-ttu-id="e0a6b-123">Specifica le configurazioni HDFS di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-124">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="e0a6b-124">-HiveEnv</span></span>
<span data-ttu-id="e0a6b-125">Specifica le configurazioni di hive ENV di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-126">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="e0a6b-126">-HiveSite</span></span>
<span data-ttu-id="e0a6b-127">Specifica le configurazioni del sito hive di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="e0a6b-128">-MapRed</span></span>
<span data-ttu-id="e0a6b-129">Specifica le configurazioni del sito MapRed di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="e0a6b-130">-OozieEnv</span></span>
<span data-ttu-id="e0a6b-131">Specifica le configurazioni di oozie ENV di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="e0a6b-132">-OozieSite</span></span>
<span data-ttu-id="e0a6b-133">Specifica le configurazioni del sito oozie di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="e0a6b-134">-RServer</span></span>
<span data-ttu-id="e0a6b-135">Specifica le configurazioni di RServer.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="e0a6b-136">Valido solo per i cluster RServer.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-136">Valid only for RServer clusters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="e0a6b-137">-Spark2Defaults</span></span>
<span data-ttu-id="e0a6b-138">Specifica le configurazioni predefinite di Spark2 di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="e0a6b-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="e0a6b-140">Specifica le configurazioni di SparkConf di risparmio Spark2 di questo cluster di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-141">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="e0a6b-141">-SparkDefaults</span></span>
<span data-ttu-id="e0a6b-142">Specifica le configurazioni predefinite Spark di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="e0a6b-143">-SparkThriftConf</span></span>
<span data-ttu-id="e0a6b-144">Specifica le configurazioni di SparkConf di risparmio Spark di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-145">-Storm</span><span class="sxs-lookup"><span data-stu-id="e0a6b-145">-Storm</span></span>
<span data-ttu-id="e0a6b-146">Specifica le configurazioni del sito Storm di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-147">-Tez</span><span class="sxs-lookup"><span data-stu-id="e0a6b-147">-Tez</span></span>
<span data-ttu-id="e0a6b-148">Specifica le configurazioni del sito Tez di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="e0a6b-149">-WebHCat</span></span>
<span data-ttu-id="e0a6b-150">Specifica le configurazioni del sito WebHCat di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-151">-Filato</span><span class="sxs-lookup"><span data-stu-id="e0a6b-151">-Yarn</span></span>
<span data-ttu-id="e0a6b-152">Specifica le configurazioni del sito del filato di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a6b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0a6b-153">CommonParameters</span></span>
<span data-ttu-id="e0a6b-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0a6b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0a6b-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0a6b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0a6b-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0a6b-156">INPUTS</span></span>

### <span data-ttu-id="e0a6b-157">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e0a6b-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="e0a6b-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0a6b-158">OUTPUTS</span></span>

### <span data-ttu-id="e0a6b-159">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e0a6b-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="e0a6b-160">Note</span><span class="sxs-lookup"><span data-stu-id="e0a6b-160">NOTES</span></span>

## <span data-ttu-id="e0a6b-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0a6b-161">RELATED LINKS</span></span>

[<span data-ttu-id="e0a6b-162">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e0a6b-162">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

