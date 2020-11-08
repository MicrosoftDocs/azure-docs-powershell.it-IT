---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF41DDBA-6D4B-47A5-BCFF-3D0BB1D375C5
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2b6aaf5e8564b3eea675a57176b8f7118d2c7a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023918"
---
# <span data-ttu-id="5e3e1-101">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="5e3e1-101">Set-AzureHDInsightDefaultStorage</span></span>

## <span data-ttu-id="5e3e1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e3e1-102">SYNOPSIS</span></span>
<span data-ttu-id="5e3e1-103">Imposta l'account di archiviazione predefinito per un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-103">Sets the default storage account for an HDInsight cluster.</span></span>

## <span data-ttu-id="5e3e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e3e1-104">SYNTAX</span></span>

```
Set-AzureHDInsightDefaultStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> -StorageContainerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5e3e1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e3e1-105">DESCRIPTION</span></span>
<span data-ttu-id="5e3e1-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="5e3e1-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="5e3e1-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="5e3e1-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="5e3e1-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="5e3e1-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="5e3e1-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="5e3e1-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5e3e1-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="5e3e1-112">Il cmdlet **set-AzureHDInsightDefaultStorage** imposta l'account di archiviazione predefinito per una configurazione di cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-112">The **Set-AzureHDInsightDefaultStorage** cmdlet sets the default storage account for an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="5e3e1-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e3e1-113">EXAMPLES</span></span>

### <span data-ttu-id="5e3e1-114">Esempio 1: impostare l'account di archiviazione predefinito</span><span class="sxs-lookup"><span data-stu-id="5e3e1-114">Example 1: Set the default storage account</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer"
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="5e3e1-115">Il primo comando usa il cmdlet **Get-AzureSubscription** per ottenere l'ID corrente della sottoscrizione e lo archivia nella variabile $SubId.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="5e3e1-116">Il secondo e il terzo comando usano il cmdlet **Get-AzureStorageKey** per ottenere le chiavi di archiviazione primarie per MyBlobStorage e MySecondBlobStorage, quindi archiviare rispettivamente le chiavi nelle variabili $Key 1 e $Key 2.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="5e3e1-117">I comandi quarto, quinto e sesto usano il cmdlet **Get-Credential** per ottenere le credenziali per l'abbonamento corrente, quindi archiviano le credenziali nelle variabili $Creds, $OozieCreds e $HiveCreds.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription, and then stores the credentials in the $Creds, $OozieCreds, and $HiveCreds variables.</span></span>

<span data-ttu-id="5e3e1-118">Il comando finale esegue una sequenza di operazioni usando questi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5e3e1-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="5e3e1-119">**New-AzureHDInsightClusterConfig** per creare una configurazione di cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="5e3e1-120">**Set-AzureHDInsightDefaultStorage** per impostare l'account di archiviazione predefinito per la configurazione su MyBlobStorage.blob.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="5e3e1-121">**Add-AzureHDInsightStorage** per aggiungere un secondo account di archiviazione denominato MySecondBlobStorage.blob.Core.Windows.NET alla configurazione.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="5e3e1-122">**Add-AzureHDInsightMetastore** per aggiungere un Metastore per oozie e un Metastore per hive alla configurazione.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="5e3e1-123">**New-AzureHDInsightCluster** per creare un cluster HDInsight con la nuova configurazione.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="5e3e1-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e3e1-124">PARAMETERS</span></span>

### <span data-ttu-id="5e3e1-125">-Config</span><span class="sxs-lookup"><span data-stu-id="5e3e1-125">-Config</span></span>
<span data-ttu-id="5e3e1-126">Specifica un oggetto Configuration.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-126">Specifies a configuration object.</span></span>
<span data-ttu-id="5e3e1-127">Questo cmdlet imposta l'account di archiviazione predefinito per l'oggetto specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-127">This cmdlet sets the default storage account for the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="5e3e1-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="5e3e1-128">-Profile</span></span>
<span data-ttu-id="5e3e1-129">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5e3e1-130">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5e3e1-131">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5e3e1-131">-StorageAccountKey</span></span>
<span data-ttu-id="5e3e1-132">Specifica la chiave dell'account di archiviazione usata per accedere all'account di archiviazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-132">Specifies the storage account key that is used to access the default storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e3e1-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5e3e1-133">-StorageAccountName</span></span>
<span data-ttu-id="5e3e1-134">Specifica il nome di un account di archiviazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-134">Specifies the name of a default storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e3e1-135">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="5e3e1-135">-StorageContainerName</span></span>
<span data-ttu-id="5e3e1-136">Specifica il nome del contenitore di archiviazione predefinito per un cluster.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-136">Specifies the name of the default storage container for a cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e3e1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e3e1-137">CommonParameters</span></span>
<span data-ttu-id="5e3e1-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e3e1-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e3e1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e3e1-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e3e1-140">INPUTS</span></span>

## <span data-ttu-id="5e3e1-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e3e1-141">OUTPUTS</span></span>

## <span data-ttu-id="5e3e1-142">Note</span><span class="sxs-lookup"><span data-stu-id="5e3e1-142">NOTES</span></span>

## <span data-ttu-id="5e3e1-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e3e1-143">RELATED LINKS</span></span>

[<span data-ttu-id="5e3e1-144">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="5e3e1-144">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="5e3e1-145">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="5e3e1-145">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="5e3e1-146">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5e3e1-146">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="5e3e1-147">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="5e3e1-147">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


