---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: BB01591D-4E1A-4C89-8B2A-5A242C29B125
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8904c5e228d181a3090b3a0d62d74d84005bd2b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029710"
---
# <span data-ttu-id="1c9e4-101">Invoke-AzureHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="1c9e4-101">Invoke-AzureHDInsightHiveJob</span></span>

## <span data-ttu-id="1c9e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c9e4-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9e4-103">Invia query hive a un cluster HDInsight, Mostra lo stato di avanzamento dell'esecuzione della query e ottiene i risultati della query in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-103">Submits Hive queries to an HDInsight cluster, shows progress of the query execution, and gets query results in one operation.</span></span>

## <span data-ttu-id="1c9e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c9e4-104">SYNTAX</span></span>

```
Invoke-AzureHDInsightHiveJob [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1c9e4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c9e4-105">DESCRIPTION</span></span>
<span data-ttu-id="1c9e4-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="1c9e4-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="1c9e4-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="1c9e4-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="1c9e4-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="1c9e4-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="1c9e4-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="1c9e4-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1c9e4-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="1c9e4-112">Il cmdlet **Invoke-AzureHDInsightHiveJob** invia query hive a un cluster HDInsight, Visualizza lo stato dell'esecuzione della query e ottiene i risultati della query in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-112">The **Invoke-AzureHDInsightHiveJob** cmdlet submits Hive queries to an HDInsight cluster, displays the progress of the query execution, and gets the query results in one operation.</span></span>
<span data-ttu-id="1c9e4-113">È necessario eseguire il cmdlet Use-AzureHDInsightCluster prima di eseguire **Invoke-AzureHDInsightHiveJob** per specificare il cluster HDInsight a cui inviare una query.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-113">You must run the Use-AzureHDInsightCluster cmdlet before running **Invoke-AzureHDInsightHiveJob** to specify the HDInsight cluster to which to submit a query.</span></span>

## <span data-ttu-id="1c9e4-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c9e4-114">EXAMPLES</span></span>

### <span data-ttu-id="1c9e4-115">Esempio 1: inviare una query hive</span><span class="sxs-lookup"><span data-stu-id="1c9e4-115">Example 1: Submit a Hive query</span></span>
```
PS C:\>Use-AzureHDInsightCluster "Cluster01" -Subscription (Get-AzureSubscription -Current).SubscriptionId 
PS C:\> Invoke-AzureHDInsightHiveJob "select * from hivesampletable limit 10"
```

<span data-ttu-id="1c9e4-116">Il primo comando usa il cmdlet **use-AzureHDInsightCluster** per specificare un cluster nella sottoscrizione corrente da usare per una query hive.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-116">The first command uses the **Use-AzureHDInsightCluster** cmdlet to specify a cluster in the current subscription to use for a Hive query.</span></span>

<span data-ttu-id="1c9e4-117">Il secondo comando usa il cmdlet **Invoke-AzureHDInsightHiveJob** per inviare la query hive.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-117">The second command uses the **Invoke-AzureHDInsightHiveJob** cmdlet to submit the Hive query.</span></span>

## <span data-ttu-id="1c9e4-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c9e4-118">PARAMETERS</span></span>

### <span data-ttu-id="1c9e4-119">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="1c9e4-119">-Arguments</span></span>
<span data-ttu-id="1c9e4-120">Specifica una matrice di argomenti per un processo di Hadoop.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-120">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="1c9e4-121">Gli argomenti vengono passati come argomenti della riga di comando per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-121">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e4-122">-Definisce</span><span class="sxs-lookup"><span data-stu-id="1c9e4-122">-Defines</span></span>
<span data-ttu-id="1c9e4-123">Specifica i valori di configurazione di Hadoop da impostare quando viene eseguito un processo.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-123">Specifies Hadoop configuration values to set when a job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e4-124">-File</span><span class="sxs-lookup"><span data-stu-id="1c9e4-124">-File</span></span>
<span data-ttu-id="1c9e4-125">Specifica il percorso BLOB di archiviazione di Windows Azure (WASB) per un file in archiviazione BLOB di Azure che contiene la query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-125">Specifies the Windows Azure Storage Blob (WASB) path to a file in Azure blob storage that contains the query to run.</span></span>
<span data-ttu-id="1c9e4-126">Puoi usare questo parametro invece del parametro di *query* .</span><span class="sxs-lookup"><span data-stu-id="1c9e4-126">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e4-127">-File</span><span class="sxs-lookup"><span data-stu-id="1c9e4-127">-Files</span></span>
<span data-ttu-id="1c9e4-128">Specifica una raccolta di file necessari per un processo hive.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-128">Specifies a collection of files that are required for a Hive job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e4-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="1c9e4-129">-JobName</span></span>
<span data-ttu-id="1c9e4-130">Specifica il nome di un processo hive.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-130">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="1c9e4-131">Se non specifichi questo parametro, questo cmdlet usa il valore predefinito: "hive: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="1c9e4-131">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e4-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="1c9e4-132">-Profile</span></span>
<span data-ttu-id="1c9e4-133">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1c9e4-134">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1c9e4-135">-Query</span><span class="sxs-lookup"><span data-stu-id="1c9e4-135">-Query</span></span>
<span data-ttu-id="1c9e4-136">Specifica una query hive.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-136">Specifies a Hive query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryText

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e4-137">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="1c9e4-137">-RunAsFileJob</span></span>
<span data-ttu-id="1c9e4-138">Indica che questo cmdlet crea un file nell'account di archiviazione di Azure predefinito in cui archiviare una query.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-138">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="1c9e4-139">Questo cmdlet invia il processo che fa riferimento a questo file come script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-139">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="1c9e4-140">Puoi usare questa funzionalità per gestire caratteri speciali come il segno di percentuale (%) l'invio di un processo non viene eseguito tramite Templeton, perché Templeton interpreta una query con un segno di percentuale come parametro URL.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-140">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e4-141">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="1c9e4-141">-StatusFolder</span></span>
<span data-ttu-id="1c9e4-142">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo, inclusi il codice di uscita e i registri delle attività.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-142">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="1c9e4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9e4-143">CommonParameters</span></span>
<span data-ttu-id="1c9e4-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9e4-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c9e4-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9e4-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c9e4-146">INPUTS</span></span>

## <span data-ttu-id="1c9e4-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c9e4-147">OUTPUTS</span></span>

## <span data-ttu-id="1c9e4-148">Note</span><span class="sxs-lookup"><span data-stu-id="1c9e4-148">NOTES</span></span>

## <span data-ttu-id="1c9e4-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c9e4-149">RELATED LINKS</span></span>

[<span data-ttu-id="1c9e4-150">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1c9e4-150">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="1c9e4-151">Usare-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1c9e4-151">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


