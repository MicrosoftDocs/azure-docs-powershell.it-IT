---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EB196CF5-3E2C-4F38-A983-3365A379672A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 637fc6f65c7168db9ba7e45cea7268208b334c99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023681"
---
# <span data-ttu-id="8abd1-101">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="8abd1-101">Add-AzureHDInsightMetastore</span></span>

## <span data-ttu-id="8abd1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8abd1-102">SYNOPSIS</span></span>
<span data-ttu-id="8abd1-103">Aggiunge un account di database di SQL Server a una configurazione di cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8abd1-103">Adds a SQL Server database account to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="8abd1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8abd1-104">SYNTAX</span></span>

```
Add-AzureHDInsightMetastore -Config <AzureHDInsightConfig> -Credential <PSCredential> -DatabaseName <String>
 -MetastoreType <AzureHDInsightMetastoreType> -SqlAzureServerName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8abd1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8abd1-105">DESCRIPTION</span></span>
<span data-ttu-id="8abd1-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="8abd1-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="8abd1-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="8abd1-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="8abd1-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8abd1-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="8abd1-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="8abd1-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="8abd1-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="8abd1-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="8abd1-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8abd1-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="8abd1-112">Il cmdlet **Add-AzureHDInsightMetastore** aggiunge un database di Microsoft SQL Server a una configurazione di Azure HDInsight creata dal cmdlet **New-AzureHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="8abd1-112">The **Add-AzureHDInsightMetastore** cmdlet adds a Microsoft SQL Server database to an Azure HDInsight configuration that is created by the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>
<span data-ttu-id="8abd1-113">Il database viene usato per archiviare i metadati per hive o oozie, o entrambi.</span><span class="sxs-lookup"><span data-stu-id="8abd1-113">The database is used to store metadata for Hive or Oozie, or both.</span></span>

## <span data-ttu-id="8abd1-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8abd1-114">EXAMPLES</span></span>

### <span data-ttu-id="8abd1-115">Esempio 1: aggiungere un Metastore</span><span class="sxs-lookup"><span data-stu-id="8abd1-115">Example 1: Add a metastore</span></span>
```
PS C:\>$Metaconfig = Add-AzureHDInsightMetastore -Config $Config -SqlAzureServerName "ContosoSQLServer" -DatabaseName "DBname" -Credential (Get-Credential) -MetastoreType HiveMetaStore
```

<span data-ttu-id="8abd1-116">Questo comando aggiunge un database di SQL Server denominato ContosoSQLServer per fungere da Metastore hive per un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8abd1-116">This command adds a SQL Server database named ContosoSQLServer to serve as a Hive metastore for an HDInsight cluster.</span></span>

### <span data-ttu-id="8abd1-117">Esempio 2: configurare lo spazio di archiviazione e aggiungere metastores</span><span class="sxs-lookup"><span data-stu-id="8abd1-117">Example 2: Configure storage and add metastores</span></span>
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

<span data-ttu-id="8abd1-118">Il primo comando usa il cmdlet **Get-AzureSubscription** per ottenere l'ID corrente della sottoscrizione e lo archivia nella variabile $SubId.</span><span class="sxs-lookup"><span data-stu-id="8abd1-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="8abd1-119">Il secondo e il terzo comando usano il cmdlet **Get-AzureStorageKey** per ottenere le chiavi di archiviazione primarie per MyBlobStorage e MySecondBlobStorage, quindi archiviare rispettivamente le chiavi nelle variabili $Key 1 e $Key 2.</span><span class="sxs-lookup"><span data-stu-id="8abd1-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="8abd1-120">I comandi quarto, quinto e sesto usano il cmdlet **Get-Credential** per ottenere le credenziali per l'abbonamento corrente e per oozie e hive e quindi archiviare le credenziali nelle variabili.</span><span class="sxs-lookup"><span data-stu-id="8abd1-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="8abd1-121">Il comando finale esegue una sequenza di operazioni usando questi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8abd1-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="8abd1-122">**New-AzureHDInsightClusterConfig** per creare una configurazione di cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8abd1-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="8abd1-123">**Set-AzureHDInsightDefaultStorage** per impostare l'account di archiviazione predefinito per la configurazione su MyBlobStorage.blob.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="8abd1-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="8abd1-124">**Add-AzureHDInsightStorage** per aggiungere un secondo account di archiviazione denominato MySecondBlobStorage.blob.Core.Windows.NET alla configurazione.</span><span class="sxs-lookup"><span data-stu-id="8abd1-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="8abd1-125">**Add-AzureHDInsightMetastore** per aggiungere un Metastore per oozie e un Metastore per hive alla configurazione.</span><span class="sxs-lookup"><span data-stu-id="8abd1-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="8abd1-126">**New-AzureHDInsightCluster** per creare un cluster HDInsight con la nuova configurazione.</span><span class="sxs-lookup"><span data-stu-id="8abd1-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="8abd1-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8abd1-127">PARAMETERS</span></span>

### <span data-ttu-id="8abd1-128">-Config</span><span class="sxs-lookup"><span data-stu-id="8abd1-128">-Config</span></span>
<span data-ttu-id="8abd1-129">Specifica un oggetto Configuration.</span><span class="sxs-lookup"><span data-stu-id="8abd1-129">Specifies a configuration object.</span></span>
<span data-ttu-id="8abd1-130">Questo cmdlet aggiunge le informazioni sul Metastore all'oggetto Configuration specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8abd1-130">This cmdlet adds metastore information to the configuration object that this parameter specifies.</span></span>

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

### <span data-ttu-id="8abd1-131">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="8abd1-131">-Credential</span></span>
<span data-ttu-id="8abd1-132">Specifica le credenziali usate per accedere a un database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8abd1-132">Specifies the credentials that are used to access a SQL Server database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8abd1-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8abd1-133">-DatabaseName</span></span>
<span data-ttu-id="8abd1-134">Specifica il nome del database per archiviare i metadati hive o oozie.</span><span class="sxs-lookup"><span data-stu-id="8abd1-134">Specifies the name of the database to store Hive or Oozie metadata.</span></span>

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

### <span data-ttu-id="8abd1-135">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="8abd1-135">-MetastoreType</span></span>
<span data-ttu-id="8abd1-136">Specifica il tipo Metastore.</span><span class="sxs-lookup"><span data-stu-id="8abd1-136">Specifies the metastore type.</span></span>
<span data-ttu-id="8abd1-137">I valori accettabili per questo parametro sono: HiveMetaStore o OozieMetaStore.</span><span class="sxs-lookup"><span data-stu-id="8abd1-137">The acceptable values for this parameter are: HiveMetaStore or OozieMetaStore.</span></span>

```yaml
Type: AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8abd1-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="8abd1-138">-Profile</span></span>
<span data-ttu-id="8abd1-139">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8abd1-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8abd1-140">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8abd1-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8abd1-141">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="8abd1-141">-SqlAzureServerName</span></span>
<span data-ttu-id="8abd1-142">Specifica il nome di dominio completo (FQDN) di SQL Server che contiene il database per archiviare i metadati.</span><span class="sxs-lookup"><span data-stu-id="8abd1-142">Specifies the fully qualified domain name (FQDN) of the SQL Server that contains the database to store metadata.</span></span>

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

### <span data-ttu-id="8abd1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8abd1-143">CommonParameters</span></span>
<span data-ttu-id="8abd1-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8abd1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8abd1-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8abd1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8abd1-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8abd1-146">INPUTS</span></span>

## <span data-ttu-id="8abd1-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8abd1-147">OUTPUTS</span></span>

## <span data-ttu-id="8abd1-148">Note</span><span class="sxs-lookup"><span data-stu-id="8abd1-148">NOTES</span></span>

## <span data-ttu-id="8abd1-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8abd1-149">RELATED LINKS</span></span>

[<span data-ttu-id="8abd1-150">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="8abd1-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="8abd1-151">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8abd1-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="8abd1-152">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="8abd1-152">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="8abd1-153">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="8abd1-153">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
