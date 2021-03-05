---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: be8878d338206e1355dc36082d4f9941cf141838
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009005"
---
# <span data-ttu-id="47730-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="47730-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="47730-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47730-102">SYNOPSIS</span></span>
<span data-ttu-id="47730-103">Crea un oggetto processo Hive.</span><span class="sxs-lookup"><span data-stu-id="47730-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="47730-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47730-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47730-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="47730-105">DESCRIPTION</span></span>
<span data-ttu-id="47730-106">Il cmdlet **New-AzHDInsightHiveJobDefinition** definisce un oggetto processo Hive da usare con un cluster Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="47730-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="47730-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47730-107">EXAMPLES</span></span>

### <span data-ttu-id="47730-108">Esempio 1: Creare una definizione di processo hive</span><span class="sxs-lookup"><span data-stu-id="47730-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="47730-109">Questo comando crea una definizione di processo di hive.</span><span class="sxs-lookup"><span data-stu-id="47730-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="47730-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47730-110">PARAMETERS</span></span>

### <span data-ttu-id="47730-111">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="47730-111">-Arguments</span></span>
<span data-ttu-id="47730-112">Specifica una matrice di argomenti per il processo.</span><span class="sxs-lookup"><span data-stu-id="47730-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="47730-113">Gli argomenti vengono passati come argomenti della riga di comando a ogni attività.</span><span class="sxs-lookup"><span data-stu-id="47730-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="47730-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47730-114">-DefaultProfile</span></span>
<span data-ttu-id="47730-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="47730-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47730-116">-Defines</span><span class="sxs-lookup"><span data-stu-id="47730-116">-Defines</span></span>
<span data-ttu-id="47730-117">Specifica i valori di configurazione di Hadoop da impostare per l'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="47730-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="47730-118">-File</span><span class="sxs-lookup"><span data-stu-id="47730-118">-File</span></span>
<span data-ttu-id="47730-119">Specifica il percorso di un file che contiene la query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="47730-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="47730-120">Il file deve essere disponibile nell'account di archiviazione associato al cluster.</span><span class="sxs-lookup"><span data-stu-id="47730-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="47730-121">È possibile usare questo parametro invece del *parametro query.*</span><span class="sxs-lookup"><span data-stu-id="47730-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="47730-122">-File</span><span class="sxs-lookup"><span data-stu-id="47730-122">-Files</span></span>
<span data-ttu-id="47730-123">Specifica una raccolta di file associati a un processo hive.</span><span class="sxs-lookup"><span data-stu-id="47730-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="47730-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="47730-124">-JobName</span></span>
<span data-ttu-id="47730-125">Specifica il nome del processo.</span><span class="sxs-lookup"><span data-stu-id="47730-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="47730-126">-Query</span><span class="sxs-lookup"><span data-stu-id="47730-126">-Query</span></span>
<span data-ttu-id="47730-127">Specifica la query Hive.</span><span class="sxs-lookup"><span data-stu-id="47730-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="47730-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="47730-128">-RunAsFileJob</span></span>
<span data-ttu-id="47730-129">Indica che questo cmdlet crea un file nell'account di archiviazione di Azure predefinito in cui archiviare una query.</span><span class="sxs-lookup"><span data-stu-id="47730-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="47730-130">Questo cmdlet invia il processo che fa riferimento a questo file come script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="47730-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="47730-131">È possibile usare questa funzionalità per gestire caratteri speciali come il segno di percentuale (%) che non verrebbero emesse in un processo inviato tramite Templeton, perché Templeton interpreta una query con un segno di percentuale come parametro dell'URL.</span><span class="sxs-lookup"><span data-stu-id="47730-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47730-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="47730-132">-StatusFolder</span></span>
<span data-ttu-id="47730-133">Specifica il percorso della cartella contenente gli output e gli output di errore standard per un processo.</span><span class="sxs-lookup"><span data-stu-id="47730-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="47730-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47730-134">CommonParameters</span></span>
<span data-ttu-id="47730-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47730-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47730-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="47730-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47730-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="47730-137">INPUTS</span></span>

### <span data-ttu-id="47730-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="47730-138">None</span></span>

## <span data-ttu-id="47730-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47730-139">OUTPUTS</span></span>

### <span data-ttu-id="47730-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="47730-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="47730-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="47730-141">NOTES</span></span>

## <span data-ttu-id="47730-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47730-142">RELATED LINKS</span></span>

[<span data-ttu-id="47730-143">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="47730-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


