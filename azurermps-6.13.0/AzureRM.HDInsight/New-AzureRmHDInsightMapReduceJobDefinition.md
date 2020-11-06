---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 284bd75abb2a2deaeaf13ad6edeb16718cbcdacd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521373"
---
# <span data-ttu-id="7377d-101">New-AzureRmHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7377d-101">New-AzureRmHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="7377d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7377d-102">SYNOPSIS</span></span>
<span data-ttu-id="7377d-103">Crea un oggetto processo MapReduce.</span><span class="sxs-lookup"><span data-stu-id="7377d-103">Creates a MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7377d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7377d-104">SYNTAX</span></span>

```
New-AzureRmHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7377d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7377d-105">DESCRIPTION</span></span>
<span data-ttu-id="7377d-106">Il cmdlet **New-AzureRmHDInsightMapReduceJobDefinition** definisce un nuovo processo di MapReduce da usare con un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7377d-106">The **New-AzureRmHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7377d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7377d-107">EXAMPLES</span></span>

### <span data-ttu-id="7377d-108">Esempio 1: creare una definizione di processo MapReduce</span><span class="sxs-lookup"><span data-stu-id="7377d-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="7377d-109">Questo comando crea una definizione di processo MapReduce.</span><span class="sxs-lookup"><span data-stu-id="7377d-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="7377d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7377d-110">PARAMETERS</span></span>

### <span data-ttu-id="7377d-111">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="7377d-111">-Arguments</span></span>
<span data-ttu-id="7377d-112">Specifica una matrice di argomenti per il processo.</span><span class="sxs-lookup"><span data-stu-id="7377d-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="7377d-113">Gli argomenti vengono passati come argomenti della riga di comando per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="7377d-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="7377d-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="7377d-114">-ClassName</span></span>
<span data-ttu-id="7377d-115">Specifica la classe Job nel file JAR.</span><span class="sxs-lookup"><span data-stu-id="7377d-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="7377d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7377d-116">-DefaultProfile</span></span>
<span data-ttu-id="7377d-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7377d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7377d-118">-Definisce</span><span class="sxs-lookup"><span data-stu-id="7377d-118">-Defines</span></span>
<span data-ttu-id="7377d-119">Specifica i valori di configurazione di Hadoop da impostare per l'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="7377d-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="7377d-120">-File</span><span class="sxs-lookup"><span data-stu-id="7377d-120">-Files</span></span>
<span data-ttu-id="7377d-121">Specifica una raccolta di file associati a un processo hive.</span><span class="sxs-lookup"><span data-stu-id="7377d-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="7377d-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="7377d-122">-JarFile</span></span>
<span data-ttu-id="7377d-123">Specifica il file JAR da usare per il processo.</span><span class="sxs-lookup"><span data-stu-id="7377d-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="7377d-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="7377d-124">-JobName</span></span>
<span data-ttu-id="7377d-125">Specifica il nome del processo.</span><span class="sxs-lookup"><span data-stu-id="7377d-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="7377d-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="7377d-126">-LibJars</span></span>
<span data-ttu-id="7377d-127">Specifica gli jar lib per il processo.</span><span class="sxs-lookup"><span data-stu-id="7377d-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="7377d-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="7377d-128">-StatusFolder</span></span>
<span data-ttu-id="7377d-129">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo.</span><span class="sxs-lookup"><span data-stu-id="7377d-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="7377d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7377d-130">CommonParameters</span></span>
<span data-ttu-id="7377d-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7377d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7377d-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7377d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7377d-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7377d-133">INPUTS</span></span>

### <span data-ttu-id="7377d-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7377d-134">None</span></span>

## <span data-ttu-id="7377d-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7377d-135">OUTPUTS</span></span>

### <span data-ttu-id="7377d-136">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7377d-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="7377d-137">Note</span><span class="sxs-lookup"><span data-stu-id="7377d-137">NOTES</span></span>

## <span data-ttu-id="7377d-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7377d-138">RELATED LINKS</span></span>

[<span data-ttu-id="7377d-139">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7377d-139">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


