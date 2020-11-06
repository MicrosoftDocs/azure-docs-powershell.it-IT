---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightconfigvalues
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
ms.openlocfilehash: 75d68b98d93168d69db4d5120dde41ca1a8f8f2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514320"
---
# <span data-ttu-id="72efb-101">Add-AzureRmHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="72efb-101">Add-AzureRmHDInsightConfigValues</span></span>

## <span data-ttu-id="72efb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72efb-102">SYNOPSIS</span></span>
<span data-ttu-id="72efb-103">Aggiunge una personalizzazione del valore di configurazione Hadoop e/o una personalizzazione della raccolta condivisa hive a un oggetto di configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="72efb-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72efb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72efb-104">SYNTAX</span></span>

### <span data-ttu-id="72efb-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="72efb-105">Spark1</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="72efb-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="72efb-106">Spark2</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72efb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72efb-107">DESCRIPTION</span></span>
<span data-ttu-id="72efb-108">Il cmdlet **Add-AzureRmHDInsightConfigValues** aggiunge una personalizzazione del valore di configurazione Hadoop, ad esempio core-site.xml o hive-site.xml, e/o una personalizzazione della raccolta condivisa hive per l'oggetto di configurazione HDInsight creato dal cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="72efb-108">The **Add-AzureRmHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="72efb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72efb-109">EXAMPLES</span></span>

### <span data-ttu-id="72efb-110">Esempio 1: aggiungere un valore di configurazione personalizzato all'oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="72efb-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightConfigValues `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="72efb-111">Questo comando aggiunge un valore di configurazione Hadoop al cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="72efb-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="72efb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72efb-112">PARAMETERS</span></span>

### <span data-ttu-id="72efb-113">-Config</span><span class="sxs-lookup"><span data-stu-id="72efb-113">-Config</span></span>
<span data-ttu-id="72efb-114">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72efb-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="72efb-115">Questo oggetto viene creato dal cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="72efb-115">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-116">-Core</span><span class="sxs-lookup"><span data-stu-id="72efb-116">-Core</span></span>
<span data-ttu-id="72efb-117">Specifica le configurazioni del sito principale di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="72efb-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72efb-118">-DefaultProfile</span></span>
<span data-ttu-id="72efb-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="72efb-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72efb-120">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="72efb-120">-HBaseEnv</span></span>
<span data-ttu-id="72efb-121">Specifica le configurazioni di HBase ENV di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="72efb-121">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-122">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="72efb-122">-HBaseSite</span></span>
<span data-ttu-id="72efb-123">Specifica le configurazioni del sito HBase di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="72efb-123">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-124">-HDFS</span><span class="sxs-lookup"><span data-stu-id="72efb-124">-Hdfs</span></span>
<span data-ttu-id="72efb-125">Specifica le configurazioni HDFS di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="72efb-125">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-126">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="72efb-126">-HiveEnv</span></span>
<span data-ttu-id="72efb-127">Specifica le configurazioni di hive ENV di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="72efb-127">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-128">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="72efb-128">-HiveSite</span></span>
<span data-ttu-id="72efb-129">Specifica le configurazioni del sito hive di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="72efb-129">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-130">-MapRed</span><span class="sxs-lookup"><span data-stu-id="72efb-130">-MapRed</span></span>
<span data-ttu-id="72efb-131">Specifica le configurazioni del sito MapRed di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="72efb-131">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-132">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="72efb-132">-OozieEnv</span></span>
<span data-ttu-id="72efb-133">Specifica le configurazioni di oozie ENV di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="72efb-133">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-134">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="72efb-134">-OozieSite</span></span>
<span data-ttu-id="72efb-135">Specifica le configurazioni del sito oozie di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="72efb-135">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-136">-RServer</span><span class="sxs-lookup"><span data-stu-id="72efb-136">-RServer</span></span>
<span data-ttu-id="72efb-137">Specifica le configurazioni di RServer.</span><span class="sxs-lookup"><span data-stu-id="72efb-137">Specifies the RServer configurations.</span></span> <span data-ttu-id="72efb-138">Valido solo per i cluster RServer.</span><span class="sxs-lookup"><span data-stu-id="72efb-138">Valid only for RServer clusters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-139">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="72efb-139">-Spark2Defaults</span></span>
<span data-ttu-id="72efb-140">Specifica le configurazioni predefinite di Spark2 di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="72efb-140">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-141">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="72efb-141">-Spark2ThriftConf</span></span>
<span data-ttu-id="72efb-142">Specifica le configurazioni di SparkConf di risparmio Spark2 di questo cluster di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="72efb-142">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-143">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="72efb-143">-SparkDefaults</span></span>
<span data-ttu-id="72efb-144">Specifica le configurazioni predefinite Spark di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="72efb-144">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-145">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="72efb-145">-SparkThriftConf</span></span>
<span data-ttu-id="72efb-146">Specifica le configurazioni di SparkConf di risparmio Spark di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="72efb-146">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-147">-Storm</span><span class="sxs-lookup"><span data-stu-id="72efb-147">-Storm</span></span>
<span data-ttu-id="72efb-148">Specifica le configurazioni del sito Storm di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="72efb-148">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-149">-Tez</span><span class="sxs-lookup"><span data-stu-id="72efb-149">-Tez</span></span>
<span data-ttu-id="72efb-150">Specifica le configurazioni del sito Tez di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="72efb-150">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-151">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="72efb-151">-WebHCat</span></span>
<span data-ttu-id="72efb-152">Specifica le configurazioni del sito WebHCat di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="72efb-152">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-153">-Filato</span><span class="sxs-lookup"><span data-stu-id="72efb-153">-Yarn</span></span>
<span data-ttu-id="72efb-154">Specifica le configurazioni del sito del filato di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="72efb-154">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72efb-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72efb-155">CommonParameters</span></span>
<span data-ttu-id="72efb-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72efb-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72efb-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72efb-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72efb-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72efb-158">INPUTS</span></span>

### <span data-ttu-id="72efb-159">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="72efb-159">AzureHDInsightConfig</span></span>
<span data-ttu-id="72efb-160">Il parametro ' config ' accetta il valore di tipo ' AzureHDInsightConfig ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="72efb-160">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="72efb-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72efb-161">OUTPUTS</span></span>

### <span data-ttu-id="72efb-162">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="72efb-162">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="72efb-163">Note</span><span class="sxs-lookup"><span data-stu-id="72efb-163">NOTES</span></span>

## <span data-ttu-id="72efb-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72efb-164">RELATED LINKS</span></span>

[<span data-ttu-id="72efb-165">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="72efb-165">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


