---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 45278426ee25337bd484a46b533c72f49dbe9586
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201299"
---
# <span data-ttu-id="bcb5b-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="bcb5b-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="bcb5b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bcb5b-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb5b-103">Crea un oggetto processo MapReduce.</span><span class="sxs-lookup"><span data-stu-id="bcb5b-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="bcb5b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcb5b-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcb5b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcb5b-105">DESCRIPTION</span></span>
<span data-ttu-id="bcb5b-106">Il cmdlet **New-AzHDInsightMapReduceJobDefinition** definisce un nuovo processo di MapReduce da usare con un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bcb5b-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="bcb5b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcb5b-107">EXAMPLES</span></span>

### <span data-ttu-id="bcb5b-108">Esempio 1: creare una definizione di processo MapReduce</span><span class="sxs-lookup"><span data-stu-id="bcb5b-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="bcb5b-109">Questo comando crea una definizione di processo MapReduce.</span><span class="sxs-lookup"><span data-stu-id="bcb5b-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="bcb5b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bcb5b-110">PARAMETERS</span></span>

### <span data-ttu-id="bcb5b-111">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="bcb5b-111">-Arguments</span></span>
<span data-ttu-id="bcb5b-112">Specifica una matrice di argomenti per il processo.</span><span class="sxs-lookup"><span data-stu-id="bcb5b-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="bcb5b-113">Gli argomenti vengono passati come argomenti della riga di comando per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="bcb5b-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="bcb5b-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="bcb5b-114">-ClassName</span></span>
<span data-ttu-id="bcb5b-115">Specifica la classe Job nel file JAR.</span><span class="sxs-lookup"><span data-stu-id="bcb5b-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="bcb5b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb5b-116">-DefaultProfile</span></span>
<span data-ttu-id="bcb5b-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bcb5b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcb5b-118">-Definisce</span><span class="sxs-lookup"><span data-stu-id="bcb5b-118">-Defines</span></span>
<span data-ttu-id="bcb5b-119">Specifica i valori di configurazione di Hadoop da impostare per l'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="bcb5b-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="bcb5b-120">-File</span><span class="sxs-lookup"><span data-stu-id="bcb5b-120">-Files</span></span>
<span data-ttu-id="bcb5b-121">Specifica una raccolta di file associati a un processo hive.</span><span class="sxs-lookup"><span data-stu-id="bcb5b-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="bcb5b-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="bcb5b-122">-JarFile</span></span>
<span data-ttu-id="bcb5b-123">Specifica il file JAR da usare per il processo.</span><span class="sxs-lookup"><span data-stu-id="bcb5b-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="bcb5b-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="bcb5b-124">-JobName</span></span>
<span data-ttu-id="bcb5b-125">Specifica il nome del processo.</span><span class="sxs-lookup"><span data-stu-id="bcb5b-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="bcb5b-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="bcb5b-126">-LibJars</span></span>
<span data-ttu-id="bcb5b-127">Specifica gli jar lib per il processo.</span><span class="sxs-lookup"><span data-stu-id="bcb5b-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="bcb5b-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="bcb5b-128">-StatusFolder</span></span>
<span data-ttu-id="bcb5b-129">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo.</span><span class="sxs-lookup"><span data-stu-id="bcb5b-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="bcb5b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb5b-130">CommonParameters</span></span>
<span data-ttu-id="bcb5b-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcb5b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb5b-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcb5b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb5b-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bcb5b-133">INPUTS</span></span>

### <span data-ttu-id="bcb5b-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bcb5b-134">None</span></span>

## <span data-ttu-id="bcb5b-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcb5b-135">OUTPUTS</span></span>

### <span data-ttu-id="bcb5b-136">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="bcb5b-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="bcb5b-137">Note</span><span class="sxs-lookup"><span data-stu-id="bcb5b-137">NOTES</span></span>

## <span data-ttu-id="bcb5b-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcb5b-138">RELATED LINKS</span></span>

[<span data-ttu-id="bcb5b-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="bcb5b-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


