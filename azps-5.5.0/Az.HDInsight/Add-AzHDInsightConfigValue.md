---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: 4de1a76d2c9ec2cba7dae67d26f73ef55a5f827f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180606"
---
# <span data-ttu-id="f8249-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="f8249-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="f8249-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8249-102">SYNOPSIS</span></span>
<span data-ttu-id="f8249-103">Aggiunge una personalizzazione del valore di configurazione Hadoop e/o una personalizzazione della raccolta condivisa Hive a un oggetto configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="f8249-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="f8249-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8249-104">SYNTAX</span></span>

```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-Spark2Defaults <Hashtable>]
 [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8249-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f8249-105">DESCRIPTION</span></span>
<span data-ttu-id="f8249-106">Il cmdlet **Add-AzHDInsightConfigValue** aggiunge una personalizzazione del valore di configurazione Hadoop, ad esempio core-site.xml o hive-site.xml e/o una personalizzazione della raccolta condivisa Hive nell'oggetto configurazione HDInsight creato dal cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="f8249-106">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="f8249-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8249-107">EXAMPLES</span></span>

### <span data-ttu-id="f8249-108">Esempio 1: Aggiungere un valore di configurazione personalizzato all'oggetto configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="f8249-108">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
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

<span data-ttu-id="f8249-109">Questo comando aggiunge un valore di configurazione Hadoop al cluster denominato your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="f8249-109">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="f8249-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8249-110">PARAMETERS</span></span>

### <span data-ttu-id="f8249-111">-Configurazione</span><span class="sxs-lookup"><span data-stu-id="f8249-111">-Config</span></span>
<span data-ttu-id="f8249-112">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8249-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="f8249-113">Questo oggetto viene creato dal cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="f8249-113">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="f8249-114">-Core</span><span class="sxs-lookup"><span data-stu-id="f8249-114">-Core</span></span>
<span data-ttu-id="f8249-115">Specifica le configurazioni del sito principale di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8249-115">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8249-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8249-116">-DefaultProfile</span></span>
<span data-ttu-id="f8249-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="f8249-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8249-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="f8249-118">-HBaseEnv</span></span>
<span data-ttu-id="f8249-119">Specifica le configurazioni HBase Env di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8249-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8249-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="f8249-120">-HBaseSite</span></span>
<span data-ttu-id="f8249-121">Specifica le configurazioni del sito HBase di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8249-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8249-122">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="f8249-122">-Hdfs</span></span>
<span data-ttu-id="f8249-123">Specifica le configurazioni HDFS di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8249-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8249-124">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="f8249-124">-HiveEnv</span></span>
<span data-ttu-id="f8249-125">Specifica le configurazioni di Hive Env di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8249-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8249-126">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="f8249-126">-HiveSite</span></span>
<span data-ttu-id="f8249-127">Specifica le configurazioni del sito hive di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8249-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8249-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="f8249-128">-MapRed</span></span>
<span data-ttu-id="f8249-129">Specifica le configurazioni del sito MapRed di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8249-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8249-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="f8249-130">-OozieEnv</span></span>
<span data-ttu-id="f8249-131">Specifica le configurazioni Oozie Env di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8249-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8249-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="f8249-132">-OozieSite</span></span>
<span data-ttu-id="f8249-133">Specifica le configurazioni dei siti Diozie di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8249-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8249-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="f8249-134">-RServer</span></span>
<span data-ttu-id="f8249-135">Specifica le configurazioni RServer.</span><span class="sxs-lookup"><span data-stu-id="f8249-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="f8249-136">Valido solo per cluster RServer.</span><span class="sxs-lookup"><span data-stu-id="f8249-136">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="f8249-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="f8249-137">-Spark2Defaults</span></span>
<span data-ttu-id="f8249-138">Specifica le configurazioni spark2 predefinite di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8249-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8249-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="f8249-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="f8249-140">Specifica le configurazioni Spark2 Thrift SparkConf di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8249-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8249-141">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="f8249-141">-SparkDefaults</span></span>
<span data-ttu-id="f8249-142">Specifica le configurazioni spark defaults di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8249-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8249-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="f8249-143">-SparkThriftConf</span></span>
<span data-ttu-id="f8249-144">Specifica le configurazioni Spark Thrift SparkConf di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8249-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8249-145">-Temporale</span><span class="sxs-lookup"><span data-stu-id="f8249-145">-Storm</span></span>
<span data-ttu-id="f8249-146">Specifica le configurazioni del sito temporale di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8249-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8249-147">-Tez</span><span class="sxs-lookup"><span data-stu-id="f8249-147">-Tez</span></span>
<span data-ttu-id="f8249-148">Specifica le configurazioni dei siti Tez di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8249-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8249-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="f8249-149">-WebHCat</span></span>
<span data-ttu-id="f8249-150">Specifica le configurazioni di siti WebHCat di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8249-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8249-151">-Snodato</span><span class="sxs-lookup"><span data-stu-id="f8249-151">-Yarn</span></span>
<span data-ttu-id="f8249-152">Specifica le configurazioni dei siti PIÙ.SEN di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8249-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8249-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8249-153">CommonParameters</span></span>
<span data-ttu-id="f8249-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8249-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8249-155">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f8249-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8249-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="f8249-156">INPUTS</span></span>

### <span data-ttu-id="f8249-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="f8249-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="f8249-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8249-158">OUTPUTS</span></span>

### <span data-ttu-id="f8249-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="f8249-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="f8249-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="f8249-160">NOTES</span></span>

## <span data-ttu-id="f8249-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8249-161">RELATED LINKS</span></span>

[<span data-ttu-id="f8249-162">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f8249-162">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


