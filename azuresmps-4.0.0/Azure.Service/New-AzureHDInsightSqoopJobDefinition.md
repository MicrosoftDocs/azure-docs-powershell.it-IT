---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E11AAB11-0CBF-4746-91D7-4D5E64801C29
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6dba4c331a69093f49c95728c028eaaf5d0bdb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023873"
---
# <span data-ttu-id="cb53f-101">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cb53f-101">New-AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="cb53f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb53f-102">SYNOPSIS</span></span>
<span data-ttu-id="cb53f-103">Definisce un nuovo processo di Sqoop.</span><span class="sxs-lookup"><span data-stu-id="cb53f-103">Defines a new Sqoop job.</span></span>

## <span data-ttu-id="cb53f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb53f-104">SYNTAX</span></span>

```
New-AzureHDInsightSqoopJobDefinition [-Command <String>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cb53f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb53f-105">DESCRIPTION</span></span>
<span data-ttu-id="cb53f-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="cb53f-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="cb53f-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="cb53f-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="cb53f-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cb53f-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="cb53f-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="cb53f-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="cb53f-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="cb53f-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="cb53f-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="cb53f-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="cb53f-112">Il cmdlet **New-AzureHDInsightSqoopJobDefinition** crea un processo Sqoop per l'esecuzione in un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cb53f-112">The **New-AzureHDInsightSqoopJobDefinition** cmdlet creates a Sqoop job to run on an Azure HDInsight cluster.</span></span>

<span data-ttu-id="cb53f-113">Sqoop è uno strumento per trasferire dati tra cluster Hadoop e database relazionali.</span><span class="sxs-lookup"><span data-stu-id="cb53f-113">Sqoop is a tool to transfer data between Hadoop clusters and relational databases.</span></span>
<span data-ttu-id="cb53f-114">Puoi usare Sqoop per importare dati da un database di SQL Server in un file System distribuito Hadoop (HDFS), trasformare i dati con Hadoop MapReduce e quindi esportare i dati dal HDFS nel database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cb53f-114">You can use Sqoop to import data from a SQL Server database to a Hadoop Distributed File System (HDFS), transform the data with Hadoop MapReduce, and then export the data from the HDFS back to the SQL Server database.</span></span>

## <span data-ttu-id="cb53f-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb53f-115">EXAMPLES</span></span>

### <span data-ttu-id="cb53f-116">Esempio 1: importare dati</span><span class="sxs-lookup"><span data-stu-id="cb53f-116">Example 1: Import data</span></span>
```
PS C:\>$SqoopJobDef = New-AzureHDInsightSqoopJobDefinition -Command "import --connect jdbc:sqlserver://<SQLDatabaseServerName>.database.windows.net:1433;username=<SQLDatabasUsername>@<SQLDatabaseServerName>; password=<SQLDatabasePassword>; database=<SQLDatabaseDatabaseName> --table <TableName> --target-dir wasb://<ContainerName>@<WindowsAzureStorageAccountName>.blob.core.windows.net/<Path>"
```

<span data-ttu-id="cb53f-117">Questo comando definisce un processo Sqoop che importa tutte le righe di una tabella da un database del server AzureSQL a un cluster di HDInsight e quindi archivia la definizione del processo nella variabile $SqoopJobDef.</span><span class="sxs-lookup"><span data-stu-id="cb53f-117">This command defines a Sqoop job that imports all of the rows in a table from an AzureSQL Server database to an HDInsight cluster, and then stores the job definition in the $SqoopJobDef variable.</span></span>

## <span data-ttu-id="cb53f-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb53f-118">PARAMETERS</span></span>

### <span data-ttu-id="cb53f-119">-Comando</span><span class="sxs-lookup"><span data-stu-id="cb53f-119">-Command</span></span>
<span data-ttu-id="cb53f-120">Specifica un comando Sqoop e i relativi argomenti.</span><span class="sxs-lookup"><span data-stu-id="cb53f-120">Specifies a Sqoop command and its arguments.</span></span>

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

### <span data-ttu-id="cb53f-121">-File</span><span class="sxs-lookup"><span data-stu-id="cb53f-121">-File</span></span>
<span data-ttu-id="cb53f-122">Specifica il percorso di un file di script contenente i comandi da eseguire.</span><span class="sxs-lookup"><span data-stu-id="cb53f-122">Specifies the path to a script file that contains the commands to run.</span></span>
<span data-ttu-id="cb53f-123">Il file di script deve trovarsi in WASB.</span><span class="sxs-lookup"><span data-stu-id="cb53f-123">The script file must be located on WASB.</span></span>

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

### <span data-ttu-id="cb53f-124">-File</span><span class="sxs-lookup"><span data-stu-id="cb53f-124">-Files</span></span>
<span data-ttu-id="cb53f-125">Specifica la raccolta di file WASB necessari per un processo.</span><span class="sxs-lookup"><span data-stu-id="cb53f-125">Specifies the collection of WASB files that are required for a job.</span></span>

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

### <span data-ttu-id="cb53f-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="cb53f-126">-Profile</span></span>
<span data-ttu-id="cb53f-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb53f-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cb53f-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="cb53f-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cb53f-129">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="cb53f-129">-StatusFolder</span></span>
<span data-ttu-id="cb53f-130">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo, inclusi il codice di uscita e i registri delle attività.</span><span class="sxs-lookup"><span data-stu-id="cb53f-130">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="cb53f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb53f-131">CommonParameters</span></span>
<span data-ttu-id="cb53f-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb53f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb53f-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb53f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb53f-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb53f-134">INPUTS</span></span>

## <span data-ttu-id="cb53f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb53f-135">OUTPUTS</span></span>

## <span data-ttu-id="cb53f-136">Note</span><span class="sxs-lookup"><span data-stu-id="cb53f-136">NOTES</span></span>

## <span data-ttu-id="cb53f-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb53f-137">RELATED LINKS</span></span>

[<span data-ttu-id="cb53f-138">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cb53f-138">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="cb53f-139">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cb53f-139">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="cb53f-140">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cb53f-140">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="cb53f-141">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cb53f-141">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


