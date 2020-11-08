---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0DFCB891-7431-4C00-98DD-263DC2794354
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea6fbc76a76533c07b11935e50e25418d10e38ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023875"
---
# <span data-ttu-id="7c04d-101">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7c04d-101">New-AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="7c04d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c04d-102">SYNOPSIS</span></span>
<span data-ttu-id="7c04d-103">Definisce un nuovo processo hive per un servizio HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7c04d-103">Defines a new Hive job for an HDInsight service.</span></span>

## <span data-ttu-id="7c04d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c04d-104">SYNTAX</span></span>

```
New-AzureHDInsightHiveJobDefinition [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7c04d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c04d-105">DESCRIPTION</span></span>
<span data-ttu-id="7c04d-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="7c04d-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="7c04d-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="7c04d-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="7c04d-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7c04d-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="7c04d-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="7c04d-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="7c04d-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="7c04d-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="7c04d-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7c04d-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="7c04d-112">Il cmdlet **New-AzureHDInsightHiveJobDefinition** definisce un processo hive per un servizio HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="7c04d-112">The **New-AzureHDInsightHiveJobDefinition** cmdlet defines a Hive job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="7c04d-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c04d-113">EXAMPLES</span></span>

### <span data-ttu-id="7c04d-114">Esempio 1: creare una definizione di processo hive</span><span class="sxs-lookup"><span data-stu-id="7c04d-114">Example 1: Create a Hive job definition</span></span>
```
PS C:\>$HiveJobDefinition = New-AzureHDInsightHiveJobDefinition -Query $QueryString
```

<span data-ttu-id="7c04d-115">Questo comando crea una definizione di processo hive che usa una stringa di query predefinita e la archivia nella variabile $HiveJobDefinition.</span><span class="sxs-lookup"><span data-stu-id="7c04d-115">This command creates a Hive job definition that uses a pre-defined query string, and then stores it in the $HiveJobDefinition variable.</span></span>

## <span data-ttu-id="7c04d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c04d-116">PARAMETERS</span></span>

### <span data-ttu-id="7c04d-117">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="7c04d-117">-Arguments</span></span>
<span data-ttu-id="7c04d-118">Specifica una matrice di argomenti per un processo di Hadoop.</span><span class="sxs-lookup"><span data-stu-id="7c04d-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="7c04d-119">Gli argomenti vengono passati come argomenti della riga di comando per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="7c04d-119">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="7c04d-120">-Definisce</span><span class="sxs-lookup"><span data-stu-id="7c04d-120">-Defines</span></span>
<span data-ttu-id="7c04d-121">Specifica i valori di configurazione di Hadoop da impostare per l'esecuzione di un processo.</span><span class="sxs-lookup"><span data-stu-id="7c04d-121">Specifies Hadoop configuration values to set for when a job runs.</span></span>

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

### <span data-ttu-id="7c04d-122">-File</span><span class="sxs-lookup"><span data-stu-id="7c04d-122">-File</span></span>
<span data-ttu-id="7c04d-123">Specifica il percorso di un file che contiene una query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="7c04d-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="7c04d-124">Puoi usare questo parametro invece del parametro di *query* .</span><span class="sxs-lookup"><span data-stu-id="7c04d-124">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="7c04d-125">-File</span><span class="sxs-lookup"><span data-stu-id="7c04d-125">-Files</span></span>
<span data-ttu-id="7c04d-126">Specifica una raccolta di file associati a un processo hive.</span><span class="sxs-lookup"><span data-stu-id="7c04d-126">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="7c04d-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="7c04d-127">-JobName</span></span>
<span data-ttu-id="7c04d-128">Specifica il nome del processo hive da definire.</span><span class="sxs-lookup"><span data-stu-id="7c04d-128">Specifies the name of the Hive job to define.</span></span>
<span data-ttu-id="7c04d-129">Se non specifichi questo parametro, viene usato il nome predefinito: "hive: \<first 100 characters of query\> ".</span><span class="sxs-lookup"><span data-stu-id="7c04d-129">If you do not specify this parameter, the default name is used: "Hive: \<first 100 characters of query\>".</span></span>

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

### <span data-ttu-id="7c04d-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="7c04d-130">-Profile</span></span>
<span data-ttu-id="7c04d-131">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c04d-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7c04d-132">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="7c04d-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7c04d-133">-Query</span><span class="sxs-lookup"><span data-stu-id="7c04d-133">-Query</span></span>
<span data-ttu-id="7c04d-134">Specifica una query hive.</span><span class="sxs-lookup"><span data-stu-id="7c04d-134">Specifies a Hive query.</span></span>

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

### <span data-ttu-id="7c04d-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="7c04d-135">-RunAsFileJob</span></span>
<span data-ttu-id="7c04d-136">Indica che questo cmdlet crea un file nell'account di archiviazione di Azure predefinito in cui archiviare una query.</span><span class="sxs-lookup"><span data-stu-id="7c04d-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="7c04d-137">Questo cmdlet invia il processo che fa riferimento a questo file come script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="7c04d-137">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="7c04d-138">Puoi usare questa funzionalità per gestire caratteri speciali come il segno di percentuale (%) l'invio di un processo non viene eseguito tramite Templeton, perché Templeton interpreta una query con un segno di percentuale come parametro URL.</span><span class="sxs-lookup"><span data-stu-id="7c04d-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="7c04d-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="7c04d-139">-StatusFolder</span></span>
<span data-ttu-id="7c04d-140">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo, inclusi il codice di uscita e i registri delle attività.</span><span class="sxs-lookup"><span data-stu-id="7c04d-140">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="7c04d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c04d-141">CommonParameters</span></span>
<span data-ttu-id="7c04d-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c04d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c04d-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c04d-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c04d-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c04d-144">INPUTS</span></span>

## <span data-ttu-id="7c04d-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c04d-145">OUTPUTS</span></span>

## <span data-ttu-id="7c04d-146">Note</span><span class="sxs-lookup"><span data-stu-id="7c04d-146">NOTES</span></span>

## <span data-ttu-id="7c04d-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c04d-147">RELATED LINKS</span></span>

[<span data-ttu-id="7c04d-148">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7c04d-148">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="7c04d-149">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7c04d-149">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="7c04d-150">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7c04d-150">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="7c04d-151">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7c04d-151">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


