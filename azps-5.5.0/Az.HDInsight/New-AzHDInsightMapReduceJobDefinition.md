---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: d6ab15fffd71776188291c58f2e21bbee5f27423
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200223"
---
# <span data-ttu-id="a4b90-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a4b90-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="a4b90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4b90-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b90-103">Crea un oggetto processo MapReduce.</span><span class="sxs-lookup"><span data-stu-id="a4b90-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="a4b90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4b90-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4b90-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a4b90-105">DESCRIPTION</span></span>
<span data-ttu-id="a4b90-106">Il cmdlet **New-AzHDInsightMapReduceJobDefinition** definisce un nuovo processo MapReduce da usare con un cluster Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a4b90-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a4b90-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4b90-107">EXAMPLES</span></span>

### <span data-ttu-id="a4b90-108">Esempio 1: Creare una definizione di processo MapReduce</span><span class="sxs-lookup"><span data-stu-id="a4b90-108">Example 1: Create a MapReduce job definition</span></span>
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

<span data-ttu-id="a4b90-109">Questo comando crea una definizione di processo MapReduce.</span><span class="sxs-lookup"><span data-stu-id="a4b90-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="a4b90-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4b90-110">PARAMETERS</span></span>

### <span data-ttu-id="a4b90-111">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="a4b90-111">-Arguments</span></span>
<span data-ttu-id="a4b90-112">Specifica una matrice di argomenti per il processo.</span><span class="sxs-lookup"><span data-stu-id="a4b90-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="a4b90-113">Gli argomenti vengono passati come argomenti della riga di comando a ogni attività.</span><span class="sxs-lookup"><span data-stu-id="a4b90-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="a4b90-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="a4b90-114">-ClassName</span></span>
<span data-ttu-id="a4b90-115">Specifica la classe di processo nel file JAR.</span><span class="sxs-lookup"><span data-stu-id="a4b90-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="a4b90-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b90-116">-DefaultProfile</span></span>
<span data-ttu-id="a4b90-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="a4b90-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4b90-118">-Defines</span><span class="sxs-lookup"><span data-stu-id="a4b90-118">-Defines</span></span>
<span data-ttu-id="a4b90-119">Specifica i valori di configurazione di Hadoop da impostare per l'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="a4b90-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="a4b90-120">-File</span><span class="sxs-lookup"><span data-stu-id="a4b90-120">-Files</span></span>
<span data-ttu-id="a4b90-121">Specifica una raccolta di file associati a un processo hive.</span><span class="sxs-lookup"><span data-stu-id="a4b90-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="a4b90-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="a4b90-122">-JarFile</span></span>
<span data-ttu-id="a4b90-123">Specifica il file JAR da usare per il processo.</span><span class="sxs-lookup"><span data-stu-id="a4b90-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="a4b90-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="a4b90-124">-JobName</span></span>
<span data-ttu-id="a4b90-125">Specifica il nome del processo.</span><span class="sxs-lookup"><span data-stu-id="a4b90-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="a4b90-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="a4b90-126">-LibJars</span></span>
<span data-ttu-id="a4b90-127">Specifica la lib JARS per il processo.</span><span class="sxs-lookup"><span data-stu-id="a4b90-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="a4b90-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="a4b90-128">-StatusFolder</span></span>
<span data-ttu-id="a4b90-129">Specifica il percorso della cartella contenente gli output e gli output di errore standard per un processo.</span><span class="sxs-lookup"><span data-stu-id="a4b90-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="a4b90-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b90-130">CommonParameters</span></span>
<span data-ttu-id="a4b90-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4b90-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b90-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a4b90-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b90-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="a4b90-133">INPUTS</span></span>

### <span data-ttu-id="a4b90-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a4b90-134">None</span></span>

## <span data-ttu-id="a4b90-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4b90-135">OUTPUTS</span></span>

### <span data-ttu-id="a4b90-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a4b90-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="a4b90-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="a4b90-137">NOTES</span></span>

## <span data-ttu-id="a4b90-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4b90-138">RELATED LINKS</span></span>

[<span data-ttu-id="a4b90-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a4b90-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


