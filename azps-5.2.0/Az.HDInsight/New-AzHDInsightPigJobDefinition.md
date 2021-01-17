---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: d9ea9152844db82d345ba1f6f50305b33975ced4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322960"
---
# <span data-ttu-id="0f3c8-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0f3c8-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="0f3c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f3c8-102">SYNOPSIS</span></span>
<span data-ttu-id="0f3c8-103">Crea un oggetto processo Pig.</span><span class="sxs-lookup"><span data-stu-id="0f3c8-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="0f3c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f3c8-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f3c8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f3c8-105">DESCRIPTION</span></span>
<span data-ttu-id="0f3c8-106">Il cmdlet **New-AzHDInsightPigJobDefinition** definisce un oggetto Job di Pig da usare con un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="0f3c8-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="0f3c8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f3c8-107">EXAMPLES</span></span>

### <span data-ttu-id="0f3c8-108">Esempio 1: creare una definizione di processo Pig</span><span class="sxs-lookup"><span data-stu-id="0f3c8-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="0f3c8-109">Questo comando crea una definizione di processo Pig.</span><span class="sxs-lookup"><span data-stu-id="0f3c8-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="0f3c8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f3c8-110">PARAMETERS</span></span>

### <span data-ttu-id="0f3c8-111">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="0f3c8-111">-Arguments</span></span>
<span data-ttu-id="0f3c8-112">Specifica una matrice di argomenti per il processo.</span><span class="sxs-lookup"><span data-stu-id="0f3c8-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="0f3c8-113">Gli argomenti vengono passati come argomenti della riga di comando per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="0f3c8-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="0f3c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f3c8-114">-DefaultProfile</span></span>
<span data-ttu-id="0f3c8-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0f3c8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f3c8-116">-File</span><span class="sxs-lookup"><span data-stu-id="0f3c8-116">-File</span></span>
<span data-ttu-id="0f3c8-117">Specifica il percorso di un file che contiene la query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="0f3c8-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="0f3c8-118">Il file deve essere disponibile nell'account di archiviazione associato al cluster.</span><span class="sxs-lookup"><span data-stu-id="0f3c8-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="0f3c8-119">Puoi usare questo parametro invece del parametro di *query* .</span><span class="sxs-lookup"><span data-stu-id="0f3c8-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="0f3c8-120">-File</span><span class="sxs-lookup"><span data-stu-id="0f3c8-120">-Files</span></span>
<span data-ttu-id="0f3c8-121">Specifica una raccolta di file associati a un processo hive.</span><span class="sxs-lookup"><span data-stu-id="0f3c8-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="0f3c8-122">-Query</span><span class="sxs-lookup"><span data-stu-id="0f3c8-122">-Query</span></span>
<span data-ttu-id="0f3c8-123">Specifica la query Pig.</span><span class="sxs-lookup"><span data-stu-id="0f3c8-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="0f3c8-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="0f3c8-124">-StatusFolder</span></span>
<span data-ttu-id="0f3c8-125">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo.</span><span class="sxs-lookup"><span data-stu-id="0f3c8-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="0f3c8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f3c8-126">CommonParameters</span></span>
<span data-ttu-id="0f3c8-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f3c8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f3c8-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f3c8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f3c8-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f3c8-129">INPUTS</span></span>

### <span data-ttu-id="0f3c8-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0f3c8-130">None</span></span>

## <span data-ttu-id="0f3c8-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f3c8-131">OUTPUTS</span></span>

### <span data-ttu-id="0f3c8-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0f3c8-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="0f3c8-133">Note</span><span class="sxs-lookup"><span data-stu-id="0f3c8-133">NOTES</span></span>

## <span data-ttu-id="0f3c8-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f3c8-134">RELATED LINKS</span></span>

[<span data-ttu-id="0f3c8-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0f3c8-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


