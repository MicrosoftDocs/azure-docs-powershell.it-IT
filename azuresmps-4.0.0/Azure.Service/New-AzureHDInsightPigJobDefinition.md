---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 227D933A-9272-4C53-89AF-711379B47A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c32a80bec0820123a8ccf1a85f5c99bdac3195d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029472"
---
# <span data-ttu-id="3c023-101">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3c023-101">New-AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="3c023-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c023-102">SYNOPSIS</span></span>
<span data-ttu-id="3c023-103">Definisce un nuovo processo di Pig per un servizio HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3c023-103">Defines a new Pig job for an HDInsight service.</span></span>

## <span data-ttu-id="3c023-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c023-104">SYNTAX</span></span>

```
New-AzureHDInsightPigJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-Query <String>] [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3c023-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c023-105">DESCRIPTION</span></span>
<span data-ttu-id="3c023-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="3c023-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="3c023-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="3c023-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="3c023-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3c023-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="3c023-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="3c023-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="3c023-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="3c023-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="3c023-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3c023-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="3c023-112">Il **nuovo AzureHDInsightPigJobDefinition** definisce un processo di Pig per un servizio HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="3c023-112">The **New-AzureHDInsightPigJobDefinition** defines a Pig job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="3c023-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c023-113">EXAMPLES</span></span>

### <span data-ttu-id="3c023-114">Esempio 1: definire un nuovo processo di Pig</span><span class="sxs-lookup"><span data-stu-id="3c023-114">Example 1: Define a new Pig job</span></span>
```
PS C:\>$0 = '$0';
PS C:\> $QueryString =  "LOGS = LOAD 'wasb:///example/data/sample.log';" + "LEVELS = foreach LOGS generate REGEX_EXTRACT($0, '(TRACE|DEBUG|INFO|WARN|ERROR|FATAL)', 1) as LOGLEVEL;" + "FILTEREDLEVELS = FILTER LEVELS by LOGLEVEL is not null;" + "GROUPEDLEVELS = GROUP FILTEREDLEVELS by LOGLEVEL;" + "FREQUENCIES = foreach GROUPEDLEVELS generate group as LOGLEVEL, COUNT(FILTEREDLEVELS.LOGLEVEL) as COUNT;" + "RESULT = order FREQUENCIES by COUNT desc;" + "DUMP RESULT;"
PS C:\> $PigJobDefinition = New-AzureHDInsightPigJobDefinition -Query $QueryString
```

<span data-ttu-id="3c023-115">Il primo comando dichiara un valore stringa e quindi archivia nella variabile $0.</span><span class="sxs-lookup"><span data-stu-id="3c023-115">The first command declares a string value, and then stores in the $0 variable.</span></span>

<span data-ttu-id="3c023-116">Il secondo comando crea una query di lavoro di maiale e la archivia nella variabile $QueryString.</span><span class="sxs-lookup"><span data-stu-id="3c023-116">The second command creates a Pig job query, and then stores it in the $QueryString variable.</span></span>

<span data-ttu-id="3c023-117">Il comando finale crea una definizione di processo Pig che usa la query in $QueryString e quindi archivia la definizione del processo nella variabile $PigJobDefinition.</span><span class="sxs-lookup"><span data-stu-id="3c023-117">The final command creates a Pig job definition that uses the query in $QueryString, and then stores the job definition in the $PigJobDefinition variable.</span></span>

## <span data-ttu-id="3c023-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c023-118">PARAMETERS</span></span>

### <span data-ttu-id="3c023-119">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="3c023-119">-Arguments</span></span>
<span data-ttu-id="3c023-120">Specifica una matrice di argomenti per un processo di suino.</span><span class="sxs-lookup"><span data-stu-id="3c023-120">Specifies an array of arguments for a Pig job.</span></span>
<span data-ttu-id="3c023-121">Gli argomenti vengono passati come argomenti della riga di comando per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="3c023-121">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Args

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c023-122">-File</span><span class="sxs-lookup"><span data-stu-id="3c023-122">-File</span></span>
<span data-ttu-id="3c023-123">Specifica il percorso di un file che contiene una query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="3c023-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="3c023-124">Puoi usare questo parametro invece del parametro di *query* .</span><span class="sxs-lookup"><span data-stu-id="3c023-124">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="3c023-125">-File</span><span class="sxs-lookup"><span data-stu-id="3c023-125">-Files</span></span>
<span data-ttu-id="3c023-126">Specifica una raccolta di file associati a un processo di suino.</span><span class="sxs-lookup"><span data-stu-id="3c023-126">Specifies a collection of files that are associated with a Pig job.</span></span>

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

### <span data-ttu-id="3c023-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="3c023-127">-Profile</span></span>
<span data-ttu-id="3c023-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c023-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3c023-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3c023-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3c023-130">-Query</span><span class="sxs-lookup"><span data-stu-id="3c023-130">-Query</span></span>
<span data-ttu-id="3c023-131">Specifica una query di lavoro Pig.</span><span class="sxs-lookup"><span data-stu-id="3c023-131">Specifies a Pig job query.</span></span>

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

### <span data-ttu-id="3c023-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="3c023-132">-StatusFolder</span></span>
<span data-ttu-id="3c023-133">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo, inclusi il codice di uscita e i registri delle attività.</span><span class="sxs-lookup"><span data-stu-id="3c023-133">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="3c023-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c023-134">CommonParameters</span></span>
<span data-ttu-id="3c023-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c023-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c023-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c023-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c023-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c023-137">INPUTS</span></span>

## <span data-ttu-id="3c023-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c023-138">OUTPUTS</span></span>

## <span data-ttu-id="3c023-139">Note</span><span class="sxs-lookup"><span data-stu-id="3c023-139">NOTES</span></span>

## <span data-ttu-id="3c023-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c023-140">RELATED LINKS</span></span>

[<span data-ttu-id="3c023-141">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3c023-141">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="3c023-142">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3c023-142">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="3c023-143">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3c023-143">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="3c023-144">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3c023-144">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


