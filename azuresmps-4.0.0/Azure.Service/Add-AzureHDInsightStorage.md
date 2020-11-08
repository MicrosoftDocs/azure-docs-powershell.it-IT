---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 1B6AC121-1AA0-4D28-B1EA-C96147FDD168
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02435c28ca17666a3b19389fde039353f3d779a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023674"
---
# <span data-ttu-id="52010-101">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="52010-101">Add-AzureHDInsightStorage</span></span>

## <span data-ttu-id="52010-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52010-102">SYNOPSIS</span></span>
<span data-ttu-id="52010-103">Aggiunge una voce dell'account di archiviazione BLOB a una configurazione HDInsight.</span><span class="sxs-lookup"><span data-stu-id="52010-103">Adds a blob storage account entry to an HDInsight configuration.</span></span>

## <span data-ttu-id="52010-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52010-104">SYNTAX</span></span>

```
Add-AzureHDInsightStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="52010-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52010-105">DESCRIPTION</span></span>
<span data-ttu-id="52010-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="52010-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="52010-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="52010-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="52010-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="52010-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="52010-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="52010-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="52010-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="52010-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="52010-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="52010-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="52010-112">Il cmdlet **Add-AzureHDInsightStorage** aggiunge una voce dell'account di archiviazione BLOB a una configurazione di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="52010-112">The **Add-AzureHDInsightStorage** cmdlet adds a blob storage account entry to an Azure HDInsight configuration.</span></span>

## <span data-ttu-id="52010-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52010-113">EXAMPLES</span></span>

### <span data-ttu-id="52010-114">Esempio 1: aggiungere un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="52010-114">Example 1: Add a storage account</span></span>
```
PS C:\>$StoreConfig = Add-AzureHDInsightStorage -Config $Config -StorageAccountName "MyStorage" -StorageAccountKey "Key"
```

<span data-ttu-id="52010-115">Questo comando aggiunge un account di archiviazione denominato archiviazione per l'oggetto di configurazione archiviato in $Config e quindi archivia la configurazione nella variabile $StoreConfig.</span><span class="sxs-lookup"><span data-stu-id="52010-115">This command adds a storage account named MyStorage to the configuration object stored in $Config, and then stores the configuration in the $StoreConfig variable.</span></span>

### <span data-ttu-id="52010-116">Esempio 2: configurare più account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="52010-116">Example 2: Configure multiple storage accounts</span></span>
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="52010-117">Il primo comando usa il cmdlet **Get-AzureSubscription** per ottenere l'ID corrente della sottoscrizione e lo archivia nella variabile $SubId.</span><span class="sxs-lookup"><span data-stu-id="52010-117">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="52010-118">Il secondo e il terzo comando usano il cmdlet **Get-AzureStorageKey** per ottenere le chiavi di archiviazione primarie per MyBlobStorage e MySecondBlobStorage, quindi archiviare rispettivamente le chiavi nelle variabili $Key 1 e $Key 2.</span><span class="sxs-lookup"><span data-stu-id="52010-118">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="52010-119">I comandi quarto, quinto e sesto ottengono le credenziali per l'abbonamento corrente e per oozie e hive e quindi archiviano le credenziali nelle variabili.</span><span class="sxs-lookup"><span data-stu-id="52010-119">The fourth, fifth, and sixth commands get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="52010-120">Il comando finale esegue una sequenza di operazioni usando questi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="52010-120">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="52010-121">**New-AzureHDInsightClusterConfig** per creare una configurazione di cluster HDInsight</span><span class="sxs-lookup"><span data-stu-id="52010-121">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration</span></span>
- <span data-ttu-id="52010-122">**Set-AzureHDInsightDefaultStorage** per impostare l'account di archiviazione predefinito per la configurazione su MyBlobStorage.blob.Core.Windows.NET</span><span class="sxs-lookup"><span data-stu-id="52010-122">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net</span></span>
- <span data-ttu-id="52010-123">**Add-AzureHDInsightStorage** per aggiungere un secondo account di archiviazione denominato MySecondBlobStorage.blob.Core.Windows.NET alla configurazione</span><span class="sxs-lookup"><span data-stu-id="52010-123">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration</span></span>
- <span data-ttu-id="52010-124">**Add-AzureHDInsightStorage** per aggiungere un Metastore per oozie e un Metastore per hive alla configurazione</span><span class="sxs-lookup"><span data-stu-id="52010-124">**Add-AzureHDInsightStorage** to add a metastore for Oozie and a metastore for Hive to the configuration</span></span>
- <span data-ttu-id="52010-125">**New-AzureHDInsightCluster** per creare un cluster HDInsight con la nuova configurazione</span><span class="sxs-lookup"><span data-stu-id="52010-125">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration</span></span>

## <span data-ttu-id="52010-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52010-126">PARAMETERS</span></span>

### <span data-ttu-id="52010-127">-Config</span><span class="sxs-lookup"><span data-stu-id="52010-127">-Config</span></span>
<span data-ttu-id="52010-128">Specifica un oggetto Configuration.</span><span class="sxs-lookup"><span data-stu-id="52010-128">Specifies a configuration object.</span></span>
<span data-ttu-id="52010-129">Questo cmdlet aggiunge le informazioni sull'account di archiviazione all'oggetto specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="52010-129">This cmdlet adds storage account information to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="52010-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="52010-130">-Profile</span></span>
<span data-ttu-id="52010-131">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52010-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="52010-132">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="52010-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="52010-133">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="52010-133">-StorageAccountKey</span></span>
<span data-ttu-id="52010-134">Specifica la chiave dell'account di archiviazione usata per accedere a un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="52010-134">Specifies the storage account key that is used to access a storage account.</span></span>

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

### <span data-ttu-id="52010-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="52010-135">-StorageAccountName</span></span>
<span data-ttu-id="52010-136">Specifica il nome dell'account di archiviazione di Azure da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="52010-136">Specifies the name of the Azure storage account to add.</span></span>

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

### <span data-ttu-id="52010-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52010-137">CommonParameters</span></span>
<span data-ttu-id="52010-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52010-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52010-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52010-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52010-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52010-140">INPUTS</span></span>

## <span data-ttu-id="52010-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52010-141">OUTPUTS</span></span>

## <span data-ttu-id="52010-142">Note</span><span class="sxs-lookup"><span data-stu-id="52010-142">NOTES</span></span>

## <span data-ttu-id="52010-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52010-143">RELATED LINKS</span></span>

[<span data-ttu-id="52010-144">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="52010-144">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="52010-145">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="52010-145">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="52010-146">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="52010-146">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


