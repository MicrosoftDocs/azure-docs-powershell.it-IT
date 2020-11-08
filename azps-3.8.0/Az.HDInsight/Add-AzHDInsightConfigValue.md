---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: 6482c6e6804b9d59ddbd752d20f39d3316b75f8f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018889"
---
# <span data-ttu-id="806dd-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="806dd-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="806dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="806dd-102">SYNOPSIS</span></span>
<span data-ttu-id="806dd-103">Aggiunge una personalizzazione del valore di configurazione Hadoop e/o una personalizzazione della raccolta condivisa hive a un oggetto di configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="806dd-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="806dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="806dd-104">SYNTAX</span></span>

### <span data-ttu-id="806dd-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="806dd-105">Spark1</span></span>
```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="806dd-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="806dd-106">Spark2</span></span>
```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="806dd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="806dd-107">DESCRIPTION</span></span>
<span data-ttu-id="806dd-108">Il cmdlet **Add-AzHDInsightConfigValue** aggiunge una personalizzazione del valore di configurazione Hadoop, ad esempio core-site.xml o hive-site.xml, e/o una personalizzazione della raccolta condivisa hive per l'oggetto di configurazione HDInsight creato dal cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="806dd-108">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="806dd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="806dd-109">EXAMPLES</span></span>

### <span data-ttu-id="806dd-110">Esempio 1: aggiungere un valore di configurazione personalizzato all'oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="806dd-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="806dd-111">Questo comando aggiunge un valore di configurazione Hadoop al cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="806dd-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="806dd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="806dd-112">PARAMETERS</span></span>

### <span data-ttu-id="806dd-113">-Config</span><span class="sxs-lookup"><span data-stu-id="806dd-113">-Config</span></span>
<span data-ttu-id="806dd-114">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="806dd-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="806dd-115">Questo oggetto viene creato dal cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="806dd-115">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="806dd-116">-Core</span><span class="sxs-lookup"><span data-stu-id="806dd-116">-Core</span></span>
<span data-ttu-id="806dd-117">Specifica le configurazioni del sito principale di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="806dd-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="806dd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="806dd-118">-DefaultProfile</span></span>
<span data-ttu-id="806dd-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="806dd-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="806dd-120">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="806dd-120">-HBaseEnv</span></span>
<span data-ttu-id="806dd-121">Specifica le configurazioni di HBase ENV di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="806dd-121">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="806dd-122">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="806dd-122">-HBaseSite</span></span>
<span data-ttu-id="806dd-123">Specifica le configurazioni del sito HBase di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="806dd-123">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="806dd-124">-HDFS</span><span class="sxs-lookup"><span data-stu-id="806dd-124">-Hdfs</span></span>
<span data-ttu-id="806dd-125">Specifica le configurazioni HDFS di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="806dd-125">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="806dd-126">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="806dd-126">-HiveEnv</span></span>
<span data-ttu-id="806dd-127">Specifica le configurazioni di hive ENV di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="806dd-127">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="806dd-128">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="806dd-128">-HiveSite</span></span>
<span data-ttu-id="806dd-129">Specifica le configurazioni del sito hive di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="806dd-129">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="806dd-130">-MapRed</span><span class="sxs-lookup"><span data-stu-id="806dd-130">-MapRed</span></span>
<span data-ttu-id="806dd-131">Specifica le configurazioni del sito MapRed di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="806dd-131">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="806dd-132">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="806dd-132">-OozieEnv</span></span>
<span data-ttu-id="806dd-133">Specifica le configurazioni di oozie ENV di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="806dd-133">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="806dd-134">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="806dd-134">-OozieSite</span></span>
<span data-ttu-id="806dd-135">Specifica le configurazioni del sito oozie di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="806dd-135">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="806dd-136">-RServer</span><span class="sxs-lookup"><span data-stu-id="806dd-136">-RServer</span></span>
<span data-ttu-id="806dd-137">Specifica le configurazioni di RServer.</span><span class="sxs-lookup"><span data-stu-id="806dd-137">Specifies the RServer configurations.</span></span> <span data-ttu-id="806dd-138">Valido solo per i cluster RServer.</span><span class="sxs-lookup"><span data-stu-id="806dd-138">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="806dd-139">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="806dd-139">-Spark2Defaults</span></span>
<span data-ttu-id="806dd-140">Specifica le configurazioni predefinite di Spark2 di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="806dd-140">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806dd-141">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="806dd-141">-Spark2ThriftConf</span></span>
<span data-ttu-id="806dd-142">Specifica le configurazioni di SparkConf di risparmio Spark2 di questo cluster di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="806dd-142">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806dd-143">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="806dd-143">-SparkDefaults</span></span>
<span data-ttu-id="806dd-144">Specifica le configurazioni predefinite Spark di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="806dd-144">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806dd-145">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="806dd-145">-SparkThriftConf</span></span>
<span data-ttu-id="806dd-146">Specifica le configurazioni di SparkConf di risparmio Spark di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="806dd-146">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806dd-147">-Storm</span><span class="sxs-lookup"><span data-stu-id="806dd-147">-Storm</span></span>
<span data-ttu-id="806dd-148">Specifica le configurazioni del sito Storm di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="806dd-148">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="806dd-149">-Tez</span><span class="sxs-lookup"><span data-stu-id="806dd-149">-Tez</span></span>
<span data-ttu-id="806dd-150">Specifica le configurazioni del sito Tez di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="806dd-150">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="806dd-151">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="806dd-151">-WebHCat</span></span>
<span data-ttu-id="806dd-152">Specifica le configurazioni del sito WebHCat di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="806dd-152">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="806dd-153">-Filato</span><span class="sxs-lookup"><span data-stu-id="806dd-153">-Yarn</span></span>
<span data-ttu-id="806dd-154">Specifica le configurazioni del sito del filato di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="806dd-154">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="806dd-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="806dd-155">CommonParameters</span></span>
<span data-ttu-id="806dd-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="806dd-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="806dd-157">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="806dd-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="806dd-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="806dd-158">INPUTS</span></span>

### <span data-ttu-id="806dd-159">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="806dd-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="806dd-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="806dd-160">OUTPUTS</span></span>

### <span data-ttu-id="806dd-161">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="806dd-161">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="806dd-162">Note</span><span class="sxs-lookup"><span data-stu-id="806dd-162">NOTES</span></span>

## <span data-ttu-id="806dd-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="806dd-163">RELATED LINKS</span></span>

[<span data-ttu-id="806dd-164">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="806dd-164">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


