---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
ms.openlocfilehash: 27f2e9d6dbc823f7148db6a299f9e999131c75d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521860"
---
# <span data-ttu-id="8a6ba-101">New-AzureRmHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8a6ba-101">New-AzureRmHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="8a6ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a6ba-102">SYNOPSIS</span></span>
<span data-ttu-id="8a6ba-103">Crea un oggetto processo Pig.</span><span class="sxs-lookup"><span data-stu-id="8a6ba-103">Creates a Pig job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a6ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a6ba-104">SYNTAX</span></span>

```
New-AzureRmHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a6ba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a6ba-105">DESCRIPTION</span></span>
<span data-ttu-id="8a6ba-106">Il cmdlet **New-AzureRmHDInsightPigJobDefinition** definisce un oggetto Job di Pig da usare con un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="8a6ba-106">The **New-AzureRmHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="8a6ba-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a6ba-107">EXAMPLES</span></span>

### <span data-ttu-id="8a6ba-108">Esempio 1: creare una definizione di processo Pig</span><span class="sxs-lookup"><span data-stu-id="8a6ba-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="8a6ba-109">Questo comando crea una definizione di processo Pig.</span><span class="sxs-lookup"><span data-stu-id="8a6ba-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="8a6ba-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a6ba-110">PARAMETERS</span></span>

### <span data-ttu-id="8a6ba-111">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="8a6ba-111">-Arguments</span></span>
<span data-ttu-id="8a6ba-112">Specifica una matrice di argomenti per il processo.</span><span class="sxs-lookup"><span data-stu-id="8a6ba-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="8a6ba-113">Gli argomenti vengono passati come argomenti della riga di comando per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="8a6ba-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="8a6ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a6ba-114">-DefaultProfile</span></span>
<span data-ttu-id="8a6ba-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8a6ba-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a6ba-116">-File</span><span class="sxs-lookup"><span data-stu-id="8a6ba-116">-File</span></span>
<span data-ttu-id="8a6ba-117">Specifica il percorso di un file che contiene la query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="8a6ba-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="8a6ba-118">Il file deve essere disponibile nell'account di archiviazione associato al cluster.</span><span class="sxs-lookup"><span data-stu-id="8a6ba-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="8a6ba-119">Puoi usare questo parametro invece del parametro di *query* .</span><span class="sxs-lookup"><span data-stu-id="8a6ba-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="8a6ba-120">-File</span><span class="sxs-lookup"><span data-stu-id="8a6ba-120">-Files</span></span>
<span data-ttu-id="8a6ba-121">Specifica una raccolta di file associati a un processo hive.</span><span class="sxs-lookup"><span data-stu-id="8a6ba-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="8a6ba-122">-Query</span><span class="sxs-lookup"><span data-stu-id="8a6ba-122">-Query</span></span>
<span data-ttu-id="8a6ba-123">Specifica la query Pig.</span><span class="sxs-lookup"><span data-stu-id="8a6ba-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="8a6ba-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="8a6ba-124">-StatusFolder</span></span>
<span data-ttu-id="8a6ba-125">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo.</span><span class="sxs-lookup"><span data-stu-id="8a6ba-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="8a6ba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a6ba-126">CommonParameters</span></span>
<span data-ttu-id="8a6ba-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a6ba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a6ba-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a6ba-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a6ba-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a6ba-129">INPUTS</span></span>

### <span data-ttu-id="8a6ba-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8a6ba-130">None</span></span>

## <span data-ttu-id="8a6ba-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a6ba-131">OUTPUTS</span></span>

### <span data-ttu-id="8a6ba-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8a6ba-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="8a6ba-133">Note</span><span class="sxs-lookup"><span data-stu-id="8a6ba-133">NOTES</span></span>

## <span data-ttu-id="8a6ba-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a6ba-134">RELATED LINKS</span></span>

[<span data-ttu-id="8a6ba-135">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8a6ba-135">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


