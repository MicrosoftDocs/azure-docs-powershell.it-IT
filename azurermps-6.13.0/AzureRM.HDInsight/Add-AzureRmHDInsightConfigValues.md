---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightconfigvalues
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
ms.openlocfilehash: dd577b5ae4aa61ff988b872bcd37eab1c911e6cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686074"
---
# <span data-ttu-id="656b6-101">Add-AzureRmHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="656b6-101">Add-AzureRmHDInsightConfigValues</span></span>

## <span data-ttu-id="656b6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="656b6-102">SYNOPSIS</span></span>
<span data-ttu-id="656b6-103">Aggiunge una personalizzazione del valore di configurazione Hadoop e/o una personalizzazione della raccolta condivisa hive a un oggetto di configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="656b6-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="656b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="656b6-104">SYNTAX</span></span>

### <span data-ttu-id="656b6-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="656b6-105">Spark1</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="656b6-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="656b6-106">Spark2</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="656b6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="656b6-107">DESCRIPTION</span></span>
<span data-ttu-id="656b6-108">Il cmdlet **Add-AzureRmHDInsightConfigValues** aggiunge una personalizzazione del valore di configurazione Hadoop, ad esempio core-site.xml o hive-site.xml, e/o una personalizzazione della raccolta condivisa hive per l'oggetto di configurazione HDInsight creato dal cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="656b6-108">The **Add-AzureRmHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="656b6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="656b6-109">EXAMPLES</span></span>

### <span data-ttu-id="656b6-110">Esempio 1: aggiungere un valore di configurazione personalizzato all'oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="656b6-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
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

<span data-ttu-id="656b6-111">Questo comando aggiunge un valore di configurazione Hadoop al cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="656b6-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="656b6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="656b6-112">PARAMETERS</span></span>

### <span data-ttu-id="656b6-113">-Config</span><span class="sxs-lookup"><span data-stu-id="656b6-113">-Config</span></span>
<span data-ttu-id="656b6-114">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="656b6-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="656b6-115">Questo oggetto viene creato dal cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="656b6-115">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="656b6-116">-Core</span><span class="sxs-lookup"><span data-stu-id="656b6-116">-Core</span></span>
<span data-ttu-id="656b6-117">Specifica le configurazioni del sito principale di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="656b6-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="656b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="656b6-118">-DefaultProfile</span></span>
<span data-ttu-id="656b6-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="656b6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="656b6-120">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="656b6-120">-HBaseEnv</span></span>
<span data-ttu-id="656b6-121">Specifica le configurazioni di HBase ENV di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="656b6-121">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="656b6-122">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="656b6-122">-HBaseSite</span></span>
<span data-ttu-id="656b6-123">Specifica le configurazioni del sito HBase di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="656b6-123">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="656b6-124">-HDFS</span><span class="sxs-lookup"><span data-stu-id="656b6-124">-Hdfs</span></span>
<span data-ttu-id="656b6-125">Specifica le configurazioni HDFS di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="656b6-125">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="656b6-126">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="656b6-126">-HiveEnv</span></span>
<span data-ttu-id="656b6-127">Specifica le configurazioni di hive ENV di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="656b6-127">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="656b6-128">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="656b6-128">-HiveSite</span></span>
<span data-ttu-id="656b6-129">Specifica le configurazioni del sito hive di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="656b6-129">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="656b6-130">-MapRed</span><span class="sxs-lookup"><span data-stu-id="656b6-130">-MapRed</span></span>
<span data-ttu-id="656b6-131">Specifica le configurazioni del sito MapRed di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="656b6-131">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="656b6-132">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="656b6-132">-OozieEnv</span></span>
<span data-ttu-id="656b6-133">Specifica le configurazioni di oozie ENV di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="656b6-133">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="656b6-134">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="656b6-134">-OozieSite</span></span>
<span data-ttu-id="656b6-135">Specifica le configurazioni del sito oozie di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="656b6-135">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="656b6-136">-RServer</span><span class="sxs-lookup"><span data-stu-id="656b6-136">-RServer</span></span>
<span data-ttu-id="656b6-137">Specifica le configurazioni di RServer.</span><span class="sxs-lookup"><span data-stu-id="656b6-137">Specifies the RServer configurations.</span></span> <span data-ttu-id="656b6-138">Valido solo per i cluster RServer.</span><span class="sxs-lookup"><span data-stu-id="656b6-138">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="656b6-139">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="656b6-139">-Spark2Defaults</span></span>
<span data-ttu-id="656b6-140">Specifica le configurazioni predefinite di Spark2 di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="656b6-140">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="656b6-141">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="656b6-141">-Spark2ThriftConf</span></span>
<span data-ttu-id="656b6-142">Specifica le configurazioni di SparkConf di risparmio Spark2 di questo cluster di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="656b6-142">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="656b6-143">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="656b6-143">-SparkDefaults</span></span>
<span data-ttu-id="656b6-144">Specifica le configurazioni predefinite Spark di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="656b6-144">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="656b6-145">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="656b6-145">-SparkThriftConf</span></span>
<span data-ttu-id="656b6-146">Specifica le configurazioni di SparkConf di risparmio Spark di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="656b6-146">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="656b6-147">-Storm</span><span class="sxs-lookup"><span data-stu-id="656b6-147">-Storm</span></span>
<span data-ttu-id="656b6-148">Specifica le configurazioni del sito Storm di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="656b6-148">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="656b6-149">-Tez</span><span class="sxs-lookup"><span data-stu-id="656b6-149">-Tez</span></span>
<span data-ttu-id="656b6-150">Specifica le configurazioni del sito Tez di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="656b6-150">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="656b6-151">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="656b6-151">-WebHCat</span></span>
<span data-ttu-id="656b6-152">Specifica le configurazioni del sito WebHCat di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="656b6-152">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="656b6-153">-Filato</span><span class="sxs-lookup"><span data-stu-id="656b6-153">-Yarn</span></span>
<span data-ttu-id="656b6-154">Specifica le configurazioni del sito del filato di questo cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="656b6-154">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="656b6-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="656b6-155">CommonParameters</span></span>
<span data-ttu-id="656b6-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="656b6-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="656b6-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="656b6-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="656b6-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="656b6-158">INPUTS</span></span>

### <span data-ttu-id="656b6-159">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="656b6-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="656b6-160">Parametri: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="656b6-160">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="656b6-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="656b6-161">OUTPUTS</span></span>

### <span data-ttu-id="656b6-162">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="656b6-162">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="656b6-163">Note</span><span class="sxs-lookup"><span data-stu-id="656b6-163">NOTES</span></span>

## <span data-ttu-id="656b6-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="656b6-164">RELATED LINKS</span></span>

[<span data-ttu-id="656b6-165">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="656b6-165">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

