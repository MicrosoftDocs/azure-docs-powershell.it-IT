---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6F89C297-4D3D-4DAD-A63A-FCC51A86BF43
online version: ''
schema: 2.0.0
ms.openlocfilehash: 542b2fb83b69fe5eb63ac6b8b979df6cc8051ed2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023686"
---
# <span data-ttu-id="3a65c-101">Add-AzureHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="3a65c-101">Add-AzureHDInsightConfigValues</span></span>

## <span data-ttu-id="3a65c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a65c-102">SYNOPSIS</span></span>
<span data-ttu-id="3a65c-103">Aggiunge una personalizzazione del valore di configurazione Hadoop o una personalizzazione della raccolta condivisa hive a una configurazione di cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3a65c-103">Adds a Hadoop configuration value customization or a Hive shared library customization to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="3a65c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a65c-104">SYNTAX</span></span>

```
Add-AzureHDInsightConfigValues -Config <AzureHDInsightConfig> [-Core <Hashtable>] [-Yarn <Hashtable>]
 [-Hdfs <Hashtable>] [-Hive <AzureHDInsightHiveConfiguration>]
 [-MapReduce <AzureHDInsightMapReduceConfiguration>] [-Oozie <AzureHDInsightOozieConfiguration>]
 [-Storm <Hashtable>] [-Spark <Hashtable>] [-HBase <AzureHDInsightHBaseConfiguration>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3a65c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a65c-105">DESCRIPTION</span></span>
<span data-ttu-id="3a65c-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="3a65c-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="3a65c-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="3a65c-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="3a65c-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3a65c-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="3a65c-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span><span class="sxs-lookup"><span data-stu-id="3a65c-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="3a65c-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span><span class="sxs-lookup"><span data-stu-id="3a65c-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="3a65c-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span><span class="sxs-lookup"><span data-stu-id="3a65c-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="3a65c-112">Il cmdlet **Add-AzureHDInsightConfigValues** aggiunge una personalizzazione del valore di configurazione Hadoop, ad esempio Core-site.xml o Hive-site.xml, o una personalizzazione della raccolta condivisa hive in una configurazione di cluster Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3a65c-112">The **Add-AzureHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as Core-site.xml or Hive-site.xml, or a Hive shared library customization to an Azure HDInsight cluster configuration.</span></span>

<span data-ttu-id="3a65c-113">Il cmdlet aggiunge valori di configurazione personalizzati a un oggetto di configurazione specificato.</span><span class="sxs-lookup"><span data-stu-id="3a65c-113">The cmdlet adds custom configuration values to a specified configuration object.</span></span>
<span data-ttu-id="3a65c-114">Le impostazioni personalizzate vengono aggiunte ai file di configurazione dei servizi di Hadoop rilevanti quando il cluster viene distribuito.</span><span class="sxs-lookup"><span data-stu-id="3a65c-114">The custom settings are added to the configuration files of the relevant Hadoop services when the cluster is deployed.</span></span>

## <span data-ttu-id="3a65c-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a65c-115">EXAMPLES</span></span>

### <span data-ttu-id="3a65c-116">Esempio 1: configurare un cluster</span><span class="sxs-lookup"><span data-stu-id="3a65c-116">Example 1: Configure a cluster</span></span>
```
PS C:\>$HiveConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightHiveConfiguration'
PS C:\> $HiveConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $HiveConfigValues.AdditionalLibraries = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightDefaultStorageAccount'
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountName = "MyStorageAccount.blob.core.windows.net"
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountKey = (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageContainerName = "MySharedLibContainer"
PS C:\> $OozieConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightOozieConfiguration'
PS C:\> $OozieConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $MapredConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightMapReduceConfiguration'
PS C:\> $MapredConfigValues.Configuration = @{ mapred.map.max.attempts = 2 }
PS C:\> $MapredConfigValues.CapacitySchedulerConfiguration = @{ mapred.capacity-scheduler.init-poll-interval = 1000 }
PS C:\> $Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyStorageAccount.blob.core.windows.net -StorageAccountKey (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary -StorageContainerName "MyStorageContainer"
    | Add-AzureHDInsightConfigValues -Core @{ io.file.buffer.size = 300000 } -MapReduce $MapredConfigValues -Hive $HiveConfigValues -Oozie $OozieConfigValues
PS C:\> $Config | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds -Name "MyCluster" -Location "North Europe"
```

<span data-ttu-id="3a65c-117">Il primo comando crea un nuovo oggetto **AzureHDInsightHiveConfiguration** e lo archivia nella variabile $HiveConfigValues.</span><span class="sxs-lookup"><span data-stu-id="3a65c-117">The first command creates a new **AzureHDInsightHiveConfiguration** object, and then stores it in the $HiveConfigValues variable.</span></span>

<span data-ttu-id="3a65c-118">I cinque comandi seguenti creano valori di configurazione per hive e archiviano tali valori come membri di $HiveConfigValues.</span><span class="sxs-lookup"><span data-stu-id="3a65c-118">The next five commands create configuration values for Hive and store those values as members of $HiveConfigValues.</span></span>

<span data-ttu-id="3a65c-119">Il settimo comando crea un oggetto **AzureHDInsightOozieConfiguration** e lo archivia nella variabile $OozieConfigValues.</span><span class="sxs-lookup"><span data-stu-id="3a65c-119">The seventh command creates an **AzureHDInsightOozieConfiguration** object, and then stores it in the $OozieConfigValues variable.</span></span>
<span data-ttu-id="3a65c-120">L'ottavo comando crea un valore di configurazione per oozie e quindi archivia i valori come membri di $OozieConfigValues.</span><span class="sxs-lookup"><span data-stu-id="3a65c-120">The eighth command creates a configuration value for Oozie, and then stores that values as a member of $OozieConfigValues.</span></span>

<span data-ttu-id="3a65c-121">Il nono comando crea un oggetto **AzureHDInsightMapReduceConfiguration** e lo archivia nella variabile $MapredConfigValues.</span><span class="sxs-lookup"><span data-stu-id="3a65c-121">The ninth command creates an **AzureHDInsightMapReduceConfiguration** object, and then stores it in the $MapredConfigValues variable.</span></span>
<span data-ttu-id="3a65c-122">I due comandi successivi creano i valori di configurazione per MapReduce e archiviano tali valori come membri di $MapredConfigValues.</span><span class="sxs-lookup"><span data-stu-id="3a65c-122">The next two commands create configuration values for MapReduce and store those values as members of $MapredConfigValues.</span></span>

<span data-ttu-id="3a65c-123">Il dodicesimo comando usa il cmdlet **New-AzureHDInsightClusterConfig** per creare una configurazione di cluster HDInsight e lo archivia nella variabile $config.</span><span class="sxs-lookup"><span data-stu-id="3a65c-123">The twelfth command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>
<span data-ttu-id="3a65c-124">Il comando usa l'operatore pipeline per passare $Config al cmdlet **set-AzureHDInsightDefaultStorage** per aggiornare l'impostazione di archiviazione predefinita e il cmdlet **Add-AzureHDInsightConfigValues** per aggiungere i nuovi valori di configurazione alla configurazione del cluster.</span><span class="sxs-lookup"><span data-stu-id="3a65c-124">The command uses the pipeline operator to pass $Config to the **Set-AzureHDInsightDefaultStorage** cmdlet to update the default storage setting and to the **Add-AzureHDInsightConfigValues** cmdlet to add the new configuration values to the cluster configuration.</span></span>

<span data-ttu-id="3a65c-125">Il comando finale usa l'operatore pipeline per passare $Config al cmdlet **New-AzureHDInsightCluster** per creare un nuovo cluster HDInsight con le impostazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="3a65c-125">The final command uses the pipeline operator to pass $Config to the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster with the customized settings.</span></span>

## <span data-ttu-id="3a65c-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a65c-126">PARAMETERS</span></span>

### <span data-ttu-id="3a65c-127">-Config</span><span class="sxs-lookup"><span data-stu-id="3a65c-127">-Config</span></span>
<span data-ttu-id="3a65c-128">Specifica l'oggetto Configuration a cui aggiungere una configurazione Hadoop.</span><span class="sxs-lookup"><span data-stu-id="3a65c-128">Specifies the configuration object to which to add a Hadoop configuration.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a65c-129">-Core</span><span class="sxs-lookup"><span data-stu-id="3a65c-129">-Core</span></span>
<span data-ttu-id="3a65c-130">Specifica un set di valori di configurazione di Hadoop per Core-site.xml.</span><span class="sxs-lookup"><span data-stu-id="3a65c-130">Specifies a set of Hadoop configuration values for Core-site.xml.</span></span>

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

### <span data-ttu-id="3a65c-131">-HBase</span><span class="sxs-lookup"><span data-stu-id="3a65c-131">-HBase</span></span>
<span data-ttu-id="3a65c-132">Specifica un set di valori di configurazione di HBase per Hbase-site.xml.</span><span class="sxs-lookup"><span data-stu-id="3a65c-132">Specifies a set of HBase configuration values for Hbase-site.xml.</span></span>

```yaml
Type: AzureHDInsightHBaseConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a65c-133">-HDFS</span><span class="sxs-lookup"><span data-stu-id="3a65c-133">-Hdfs</span></span>
<span data-ttu-id="3a65c-134">Specifica un set di valori di configurazione di Hadoop per Hdfs-site.xml.</span><span class="sxs-lookup"><span data-stu-id="3a65c-134">Specifies a set of Hadoop configuration values for Hdfs-site.xml.</span></span>

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

### <span data-ttu-id="3a65c-135">-Hive</span><span class="sxs-lookup"><span data-stu-id="3a65c-135">-Hive</span></span>
<span data-ttu-id="3a65c-136">Specifica un oggetto di personalizzazione per il servizio Hive Hadoop, incluso un set di valori di configurazione di Hadoop per Hive-site.xml e le librerie condivise hive.</span><span class="sxs-lookup"><span data-stu-id="3a65c-136">Specifies a customization object for Hadoop Hive service, including a set of Hadoop configuration values for Hive-site.xml and Hive shared libraries.</span></span>

```yaml
Type: AzureHDInsightHiveConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a65c-137">-MapReduce</span><span class="sxs-lookup"><span data-stu-id="3a65c-137">-MapReduce</span></span>
<span data-ttu-id="3a65c-138">Specifica un oggetto di personalizzazione per MapReduce e l'utilità di pianificazione della capacità.</span><span class="sxs-lookup"><span data-stu-id="3a65c-138">Specifies a customization object for MapReduce and the capacity scheduler.</span></span>

```yaml
Type: AzureHDInsightMapReduceConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a65c-139">-Oozie</span><span class="sxs-lookup"><span data-stu-id="3a65c-139">-Oozie</span></span>
<span data-ttu-id="3a65c-140">Specifica un oggetto di personalizzazione per il servizio Hadoop oozie, incluso un set di valori di configurazione di Hadoop per Oozie-site.xml.</span><span class="sxs-lookup"><span data-stu-id="3a65c-140">Specifies a customization object for Hadoop Oozie service, including a set of Hadoop configuration values for Oozie-site.xml.</span></span>

```yaml
Type: AzureHDInsightOozieConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a65c-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="3a65c-141">-Profile</span></span>
<span data-ttu-id="3a65c-142">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a65c-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3a65c-143">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3a65c-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a65c-144">-Spark</span><span class="sxs-lookup"><span data-stu-id="3a65c-144">-Spark</span></span>
<span data-ttu-id="3a65c-145">Specifica un oggetto di personalizzazione per Apache Spark.</span><span class="sxs-lookup"><span data-stu-id="3a65c-145">Specifies a customization object for Apache Spark.</span></span>

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

### <span data-ttu-id="3a65c-146">-Storm</span><span class="sxs-lookup"><span data-stu-id="3a65c-146">-Storm</span></span>
<span data-ttu-id="3a65c-147">Specifica un oggetto di personalizzazione per Apache Storm.</span><span class="sxs-lookup"><span data-stu-id="3a65c-147">Specifies a customization object for Apache Storm.</span></span>

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

### <span data-ttu-id="3a65c-148">-Filato</span><span class="sxs-lookup"><span data-stu-id="3a65c-148">-Yarn</span></span>
<span data-ttu-id="3a65c-149">Specifica un oggetto di personalizzazione per il filato Hadoop, specificando un set di valori di configurazione del filato personalizzati per Yarn-site.xml.</span><span class="sxs-lookup"><span data-stu-id="3a65c-149">Specifies a customization object for Hadoop YARN, specifying a set of customized YARN configuration values for Yarn-site.xml.</span></span>

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

### <span data-ttu-id="3a65c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a65c-150">CommonParameters</span></span>
<span data-ttu-id="3a65c-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a65c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a65c-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a65c-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a65c-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a65c-153">INPUTS</span></span>

## <span data-ttu-id="3a65c-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a65c-154">OUTPUTS</span></span>

## <span data-ttu-id="3a65c-155">Note</span><span class="sxs-lookup"><span data-stu-id="3a65c-155">NOTES</span></span>

## <span data-ttu-id="3a65c-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a65c-156">RELATED LINKS</span></span>

[<span data-ttu-id="3a65c-157">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3a65c-157">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="3a65c-158">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="3a65c-158">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="3a65c-159">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="3a65c-159">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
