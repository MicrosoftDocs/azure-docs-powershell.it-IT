---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF8AA7DE-1E0F-4F5B-95F6-7820AAF789F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: c36931af0b6927ef4fee26b9f8ade7db77d17db2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023878"
---
# <span data-ttu-id="8db68-101">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="8db68-101">New-AzureHDInsightClusterConfig</span></span>

## <span data-ttu-id="8db68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8db68-102">SYNOPSIS</span></span>
<span data-ttu-id="8db68-103">Crea una configurazione del cluster HDInsight non persistente.</span><span class="sxs-lookup"><span data-stu-id="8db68-103">Creates a non-persisted HDInsight cluster configuration.</span></span>

## <span data-ttu-id="8db68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8db68-104">SYNTAX</span></span>

```
New-AzureHDInsightClusterConfig -ClusterSizeInNodes <Int32> [-HeadNodeVMSize <String>]
 [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>] [-DataNodeVMSize <String>]
 [-ZookeeperNodeVMSize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8db68-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8db68-105">DESCRIPTION</span></span>
<span data-ttu-id="8db68-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="8db68-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="8db68-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="8db68-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="8db68-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8db68-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="8db68-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="8db68-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="8db68-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="8db68-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="8db68-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8db68-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="8db68-112">Il cmdlet **New-AzureHDInsightClusterConfig** crea una configurazione del cluster di Azure HDInsight non persistente.</span><span class="sxs-lookup"><span data-stu-id="8db68-112">The **New-AzureHDInsightClusterConfig** cmdlet creates a non-persisted Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="8db68-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8db68-113">EXAMPLES</span></span>

### <span data-ttu-id="8db68-114">Esempio 1: creare una configurazione cluster</span><span class="sxs-lookup"><span data-stu-id="8db68-114">Example 1: Create a cluster configuration</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyBlobStorage.blob.core.windows.net -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="8db68-115">Il primo comando usa il cmdlet **Get-AzureSubscription** per ottenere l'ID corrente della sottoscrizione e lo archivia nella variabile $SubId.</span><span class="sxs-lookup"><span data-stu-id="8db68-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="8db68-116">Il secondo e il terzo comando usano il cmdlet **Get-AzureStorageKey** per ottenere le chiavi di archiviazione primarie per MyBlobStorage e MySecondBlobStorage, quindi archiviare rispettivamente le chiavi nelle variabili $Key 1 e $Key 2.</span><span class="sxs-lookup"><span data-stu-id="8db68-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="8db68-117">I comandi quarto, quinto e sesto usano il cmdlet **Get-Credential** per ottenere le credenziali per l'abbonamento corrente e per oozie e hive e quindi archiviare le credenziali nelle variabili.</span><span class="sxs-lookup"><span data-stu-id="8db68-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="8db68-118">Il comando finale esegue una sequenza di operazioni usando questi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8db68-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="8db68-119">**New-AzureHDInsightClusterConfig** per creare una configurazione di cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8db68-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="8db68-120">**Set-AzureHDInsightDefaultStorage** per impostare l'account di archiviazione predefinito per la configurazione su MyBlobStorage.blob.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="8db68-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="8db68-121">**Add-AzureHDInsightStorage** per aggiungere un secondo account di archiviazione denominato MySecondBlobStorage.blob.Core.Windows.NET alla configurazione.</span><span class="sxs-lookup"><span data-stu-id="8db68-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="8db68-122">**Add-AzureHDInsightMetastore** per aggiungere un Metastore per oozie e un Metastore per hive alla configurazione.</span><span class="sxs-lookup"><span data-stu-id="8db68-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="8db68-123">**New-AzureHDInsightCluster** per creare un cluster HDInsight con la nuova configurazione.</span><span class="sxs-lookup"><span data-stu-id="8db68-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="8db68-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8db68-124">PARAMETERS</span></span>

### <span data-ttu-id="8db68-125">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="8db68-125">-ClusterSizeInNodes</span></span>
<span data-ttu-id="8db68-126">Specifica il numero di nodi dati da creare per un cluster.</span><span class="sxs-lookup"><span data-stu-id="8db68-126">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8db68-127">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="8db68-127">-ClusterType</span></span>
<span data-ttu-id="8db68-128">Specifica il tipo di cluster da creare.</span><span class="sxs-lookup"><span data-stu-id="8db68-128">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8db68-129">-DataNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="8db68-129">-DataNodeVMSize</span></span>
<span data-ttu-id="8db68-130">Specifica le dimensioni della macchina virtuale per il nodo dati.</span><span class="sxs-lookup"><span data-stu-id="8db68-130">Specifies the size of the virtual machine for the data node.</span></span>

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

### <span data-ttu-id="8db68-131">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="8db68-131">-HeadNodeVMSize</span></span>
<span data-ttu-id="8db68-132">Specifica la dimensione della macchina virtuale del nodo head per il cluster.</span><span class="sxs-lookup"><span data-stu-id="8db68-132">Specifies the virtual machine size of the head node for the cluster.</span></span>

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

### <span data-ttu-id="8db68-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="8db68-133">-Profile</span></span>
<span data-ttu-id="8db68-134">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8db68-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8db68-135">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8db68-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8db68-136">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="8db68-136">-SubnetName</span></span>
<span data-ttu-id="8db68-137">Specifica il nome di una subnet.</span><span class="sxs-lookup"><span data-stu-id="8db68-137">Specifies the name of a subnet.</span></span>

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

### <span data-ttu-id="8db68-138">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="8db68-138">-VirtualNetworkId</span></span>
<span data-ttu-id="8db68-139">Specifica l'ID della rete virtuale in cui eseguire il provisioning del cluster.</span><span class="sxs-lookup"><span data-stu-id="8db68-139">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="8db68-140">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="8db68-140">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="8db68-141">Specifica le dimensioni della macchina virtuale per il nodo ZooKeeper per un cluster HBase o Storm.</span><span class="sxs-lookup"><span data-stu-id="8db68-141">Specifies the size of the virtual machine for the ZooKeeper node for an HBase or Storm cluster.</span></span>

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

### <span data-ttu-id="8db68-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db68-142">CommonParameters</span></span>
<span data-ttu-id="8db68-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8db68-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db68-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8db68-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db68-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8db68-145">INPUTS</span></span>

## <span data-ttu-id="8db68-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8db68-146">OUTPUTS</span></span>

## <span data-ttu-id="8db68-147">Note</span><span class="sxs-lookup"><span data-stu-id="8db68-147">NOTES</span></span>

## <span data-ttu-id="8db68-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8db68-148">RELATED LINKS</span></span>

[<span data-ttu-id="8db68-149">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="8db68-149">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="8db68-150">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="8db68-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="8db68-151">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8db68-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="8db68-152">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="8db68-152">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


