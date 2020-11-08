---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: adfa71fb251950f1946b3a43f030ff32b656ec50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032521"
---
# <span data-ttu-id="3d3c1-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3d3c1-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="3d3c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d3c1-102">SYNOPSIS</span></span>
<span data-ttu-id="3d3c1-103">Crea un oggetto processo di flusso MapReduce.</span><span class="sxs-lookup"><span data-stu-id="3d3c1-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="3d3c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d3c1-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d3c1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d3c1-105">DESCRIPTION</span></span>
<span data-ttu-id="3d3c1-106">Il cmdlet **New-AzHDInsightStreamingMapReduceJobDefinition** definisce un oggetto processo in streaming MapReduce da usare con un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3d3c1-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="3d3c1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d3c1-107">EXAMPLES</span></span>

### <span data-ttu-id="3d3c1-108">Esempio 1: creare una definizione di processo di flusso MapReduce</span><span class="sxs-lookup"><span data-stu-id="3d3c1-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="3d3c1-109">Questo comando crea una definizione di processo di flusso MapReduce.</span><span class="sxs-lookup"><span data-stu-id="3d3c1-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="3d3c1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d3c1-110">PARAMETERS</span></span>

### <span data-ttu-id="3d3c1-111">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="3d3c1-111">-Arguments</span></span>
<span data-ttu-id="3d3c1-112">Specifica una matrice di argomenti per il processo.</span><span class="sxs-lookup"><span data-stu-id="3d3c1-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="3d3c1-113">Gli argomenti vengono passati come argomenti della riga di comando per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="3d3c1-113">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3c1-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="3d3c1-114">-CommandEnvironment</span></span>
<span data-ttu-id="3d3c1-115">Specifica una matrice di variabili di ambiente della riga di comando da impostare quando un processo viene eseguito sui nodi di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3d3c1-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="3d3c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d3c1-116">-DefaultProfile</span></span>
<span data-ttu-id="3d3c1-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3d3c1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3c1-118">-Definisce</span><span class="sxs-lookup"><span data-stu-id="3d3c1-118">-Defines</span></span>
<span data-ttu-id="3d3c1-119">Specifica i valori di configurazione di Hadoop da impostare per l'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="3d3c1-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="3d3c1-120">-File</span><span class="sxs-lookup"><span data-stu-id="3d3c1-120">-File</span></span>
<span data-ttu-id="3d3c1-121">Specifica il percorso di un file che contiene una query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="3d3c1-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="3d3c1-122">Puoi usare questo parametro invece del parametro di *query* .</span><span class="sxs-lookup"><span data-stu-id="3d3c1-122">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3c1-123">-File</span><span class="sxs-lookup"><span data-stu-id="3d3c1-123">-Files</span></span>
<span data-ttu-id="3d3c1-124">Specifica una raccolta di file associati a un processo hive.</span><span class="sxs-lookup"><span data-stu-id="3d3c1-124">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3c1-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="3d3c1-125">-InputPath</span></span>
<span data-ttu-id="3d3c1-126">Specifica il percorso dei file di input.</span><span class="sxs-lookup"><span data-stu-id="3d3c1-126">Specifies the path to the input files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3c1-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="3d3c1-127">-Mapper</span></span>
<span data-ttu-id="3d3c1-128">Specifica un nome di file di Mapper.</span><span class="sxs-lookup"><span data-stu-id="3d3c1-128">Specifies a Mapper file name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3c1-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="3d3c1-129">-OutputPath</span></span>
<span data-ttu-id="3d3c1-130">Specifica il percorso per l'output del processo.</span><span class="sxs-lookup"><span data-stu-id="3d3c1-130">Specifies the path for the job output.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3c1-131">-Riduttore</span><span class="sxs-lookup"><span data-stu-id="3d3c1-131">-Reducer</span></span>
<span data-ttu-id="3d3c1-132">Specifica un nome di file del riduttore.</span><span class="sxs-lookup"><span data-stu-id="3d3c1-132">Specifies a Reducer file name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3c1-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="3d3c1-133">-StatusFolder</span></span>
<span data-ttu-id="3d3c1-134">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo.</span><span class="sxs-lookup"><span data-stu-id="3d3c1-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3c1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d3c1-135">CommonParameters</span></span>
<span data-ttu-id="3d3c1-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d3c1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d3c1-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d3c1-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d3c1-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d3c1-138">INPUTS</span></span>

### <span data-ttu-id="3d3c1-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3d3c1-139">None</span></span>

## <span data-ttu-id="3d3c1-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d3c1-140">OUTPUTS</span></span>

### <span data-ttu-id="3d3c1-141">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3d3c1-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="3d3c1-142">Note</span><span class="sxs-lookup"><span data-stu-id="3d3c1-142">NOTES</span></span>

## <span data-ttu-id="3d3c1-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d3c1-143">RELATED LINKS</span></span>

[<span data-ttu-id="3d3c1-144">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="3d3c1-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


