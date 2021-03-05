---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 3217673c01e4d77fe2643765df55ff58747b3133
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971966"
---
# <span data-ttu-id="80926-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="80926-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="80926-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80926-102">SYNOPSIS</span></span>
<span data-ttu-id="80926-103">Crea un oggetto processo di Sqoop.</span><span class="sxs-lookup"><span data-stu-id="80926-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="80926-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80926-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80926-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="80926-105">DESCRIPTION</span></span>
<span data-ttu-id="80926-106">Il cmdlet **New-AzHDInsightSqoopJobDefinition** definisce un oggetto processo Sqoop da usare con un cluster Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="80926-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="80926-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80926-107">EXAMPLES</span></span>

### <span data-ttu-id="80926-108">Esempio 1: Creare una definizione di processo di Sqoop</span><span class="sxs-lookup"><span data-stu-id="80926-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="80926-109">Questo comando crea una definizione di processo di Sqoop.</span><span class="sxs-lookup"><span data-stu-id="80926-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="80926-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80926-110">PARAMETERS</span></span>

### <span data-ttu-id="80926-111">-Command</span><span class="sxs-lookup"><span data-stu-id="80926-111">-Command</span></span>
<span data-ttu-id="80926-112">Specifica il comando Sqoop.</span><span class="sxs-lookup"><span data-stu-id="80926-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="80926-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80926-113">-DefaultProfile</span></span>
<span data-ttu-id="80926-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="80926-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80926-115">-File</span><span class="sxs-lookup"><span data-stu-id="80926-115">-File</span></span>
<span data-ttu-id="80926-116">Specifica il percorso di un file che contiene la query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="80926-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="80926-117">Il file deve essere disponibile nell'account di archiviazione associato al cluster.</span><span class="sxs-lookup"><span data-stu-id="80926-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="80926-118">È possibile usare questo parametro invece del *parametro query.*</span><span class="sxs-lookup"><span data-stu-id="80926-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="80926-119">-File</span><span class="sxs-lookup"><span data-stu-id="80926-119">-Files</span></span>
<span data-ttu-id="80926-120">Specifica una raccolta di file associati a un processo hive.</span><span class="sxs-lookup"><span data-stu-id="80926-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="80926-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="80926-121">-LibDir</span></span>
<span data-ttu-id="80926-122">Specifica la directory di libreria per il processo Sqoop.</span><span class="sxs-lookup"><span data-stu-id="80926-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="80926-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="80926-123">-StatusFolder</span></span>
<span data-ttu-id="80926-124">Specifica il percorso della cartella contenente gli output e gli output di errore standard per un processo.</span><span class="sxs-lookup"><span data-stu-id="80926-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="80926-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80926-125">CommonParameters</span></span>
<span data-ttu-id="80926-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80926-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80926-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="80926-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80926-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="80926-128">INPUTS</span></span>

### <span data-ttu-id="80926-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="80926-129">None</span></span>

## <span data-ttu-id="80926-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80926-130">OUTPUTS</span></span>

### <span data-ttu-id="80926-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="80926-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="80926-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="80926-132">NOTES</span></span>

## <span data-ttu-id="80926-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80926-133">RELATED LINKS</span></span>

[<span data-ttu-id="80926-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="80926-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


