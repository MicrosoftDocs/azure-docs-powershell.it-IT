---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 22ddeeffd696de260e13c1c817afedfabe1887a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687320"
---
# <span data-ttu-id="04f0c-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="04f0c-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="04f0c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="04f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="04f0c-103">Crea un oggetto processo di flusso MapReduce.</span><span class="sxs-lookup"><span data-stu-id="04f0c-103">Creates a Streaming MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04f0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04f0c-104">SYNTAX</span></span>

```
New-AzureRmHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>]
 [-Files <String[]>] [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>]
 -InputPath <String> [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04f0c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04f0c-105">DESCRIPTION</span></span>
<span data-ttu-id="04f0c-106">Il cmdlet **New-AzureRmHDInsightStreamingMapReduceJobDefinition** definisce un oggetto processo in streaming MapReduce da usare con un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="04f0c-106">The **New-AzureRmHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="04f0c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04f0c-107">EXAMPLES</span></span>

### <span data-ttu-id="04f0c-108">Esempio 1: creare una definizione di processo di flusso MapReduce</span><span class="sxs-lookup"><span data-stu-id="04f0c-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="04f0c-109">Questo comando crea una definizione di processo di flusso MapReduce.</span><span class="sxs-lookup"><span data-stu-id="04f0c-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="04f0c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="04f0c-110">PARAMETERS</span></span>

### <span data-ttu-id="04f0c-111">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="04f0c-111">-Arguments</span></span>
<span data-ttu-id="04f0c-112">Specifica una matrice di argomenti per il processo.</span><span class="sxs-lookup"><span data-stu-id="04f0c-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="04f0c-113">Gli argomenti vengono passati come argomenti della riga di comando per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="04f0c-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="04f0c-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="04f0c-114">-CommandEnvironment</span></span>
<span data-ttu-id="04f0c-115">Specifica una matrice di variabili di ambiente della riga di comando da impostare quando un processo viene eseguito sui nodi di lavoro.</span><span class="sxs-lookup"><span data-stu-id="04f0c-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="04f0c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04f0c-116">-DefaultProfile</span></span>
<span data-ttu-id="04f0c-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="04f0c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f0c-118">-Definisce</span><span class="sxs-lookup"><span data-stu-id="04f0c-118">-Defines</span></span>
<span data-ttu-id="04f0c-119">Specifica i valori di configurazione di Hadoop da impostare per l'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="04f0c-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="04f0c-120">-File</span><span class="sxs-lookup"><span data-stu-id="04f0c-120">-File</span></span>
<span data-ttu-id="04f0c-121">Specifica il percorso di un file che contiene una query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="04f0c-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="04f0c-122">Puoi usare questo parametro invece del parametro di *query* .</span><span class="sxs-lookup"><span data-stu-id="04f0c-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="04f0c-123">-File</span><span class="sxs-lookup"><span data-stu-id="04f0c-123">-Files</span></span>
<span data-ttu-id="04f0c-124">Specifica una raccolta di file associati a un processo hive.</span><span class="sxs-lookup"><span data-stu-id="04f0c-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="04f0c-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="04f0c-125">-InputPath</span></span>
<span data-ttu-id="04f0c-126">Specifica il percorso dei file di input.</span><span class="sxs-lookup"><span data-stu-id="04f0c-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="04f0c-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="04f0c-127">-Mapper</span></span>
<span data-ttu-id="04f0c-128">Specifica un nome di file di Mapper.</span><span class="sxs-lookup"><span data-stu-id="04f0c-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="04f0c-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="04f0c-129">-OutputPath</span></span>
<span data-ttu-id="04f0c-130">Specifica il percorso per l'output del processo.</span><span class="sxs-lookup"><span data-stu-id="04f0c-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="04f0c-131">-Riduttore</span><span class="sxs-lookup"><span data-stu-id="04f0c-131">-Reducer</span></span>
<span data-ttu-id="04f0c-132">Specifica un nome di file del riduttore.</span><span class="sxs-lookup"><span data-stu-id="04f0c-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="04f0c-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="04f0c-133">-StatusFolder</span></span>
<span data-ttu-id="04f0c-134">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo.</span><span class="sxs-lookup"><span data-stu-id="04f0c-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="04f0c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04f0c-135">CommonParameters</span></span>
<span data-ttu-id="04f0c-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04f0c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04f0c-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04f0c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04f0c-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="04f0c-138">INPUTS</span></span>

### <span data-ttu-id="04f0c-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="04f0c-139">None</span></span>

## <span data-ttu-id="04f0c-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04f0c-140">OUTPUTS</span></span>

### <span data-ttu-id="04f0c-141">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="04f0c-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="04f0c-142">Note</span><span class="sxs-lookup"><span data-stu-id="04f0c-142">NOTES</span></span>

## <span data-ttu-id="04f0c-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04f0c-143">RELATED LINKS</span></span>

[<span data-ttu-id="04f0c-144">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="04f0c-144">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


