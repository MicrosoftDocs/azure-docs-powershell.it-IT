---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 242161a7a02cf3767ecd87dfc6e91a7ffba97eb3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865450"
---
# <span data-ttu-id="af46e-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="af46e-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="af46e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af46e-102">SYNOPSIS</span></span>
<span data-ttu-id="af46e-103">Crea un oggetto processo hive.</span><span class="sxs-lookup"><span data-stu-id="af46e-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="af46e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af46e-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af46e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af46e-105">DESCRIPTION</span></span>
<span data-ttu-id="af46e-106">Il cmdlet **New-AzHDInsightHiveJobDefinition** definisce un oggetto processo hive da usare con un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="af46e-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="af46e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af46e-107">EXAMPLES</span></span>

### <span data-ttu-id="af46e-108">Esempio 1: creare una definizione di processo hive</span><span class="sxs-lookup"><span data-stu-id="af46e-108">Example 1: Create a Hive job definition</span></span>
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

<span data-ttu-id="af46e-109">Questo comando crea una definizione di processo hive.</span><span class="sxs-lookup"><span data-stu-id="af46e-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="af46e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af46e-110">PARAMETERS</span></span>

### <span data-ttu-id="af46e-111">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="af46e-111">-Arguments</span></span>
<span data-ttu-id="af46e-112">Specifica una matrice di argomenti per il processo.</span><span class="sxs-lookup"><span data-stu-id="af46e-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="af46e-113">Gli argomenti vengono passati come argomenti della riga di comando per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="af46e-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="af46e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af46e-114">-DefaultProfile</span></span>
<span data-ttu-id="af46e-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="af46e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af46e-116">-Definisce</span><span class="sxs-lookup"><span data-stu-id="af46e-116">-Defines</span></span>
<span data-ttu-id="af46e-117">Specifica i valori di configurazione di Hadoop da impostare per l'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="af46e-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="af46e-118">-File</span><span class="sxs-lookup"><span data-stu-id="af46e-118">-File</span></span>
<span data-ttu-id="af46e-119">Specifica il percorso di un file che contiene la query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="af46e-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="af46e-120">Il file deve essere disponibile nell'account di archiviazione associato al cluster.</span><span class="sxs-lookup"><span data-stu-id="af46e-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="af46e-121">Puoi usare questo parametro invece del parametro di *query* .</span><span class="sxs-lookup"><span data-stu-id="af46e-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="af46e-122">-File</span><span class="sxs-lookup"><span data-stu-id="af46e-122">-Files</span></span>
<span data-ttu-id="af46e-123">Specifica una raccolta di file associati a un processo hive.</span><span class="sxs-lookup"><span data-stu-id="af46e-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="af46e-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="af46e-124">-JobName</span></span>
<span data-ttu-id="af46e-125">Specifica il nome del processo.</span><span class="sxs-lookup"><span data-stu-id="af46e-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="af46e-126">-Query</span><span class="sxs-lookup"><span data-stu-id="af46e-126">-Query</span></span>
<span data-ttu-id="af46e-127">Specifica la query hive.</span><span class="sxs-lookup"><span data-stu-id="af46e-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="af46e-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="af46e-128">-RunAsFileJob</span></span>
<span data-ttu-id="af46e-129">Indica che questo cmdlet crea un file nell'account di archiviazione di Azure predefinito in cui archiviare una query.</span><span class="sxs-lookup"><span data-stu-id="af46e-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="af46e-130">Questo cmdlet invia il processo che fa riferimento a questo file come script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="af46e-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="af46e-131">Puoi usare questa funzionalità per gestire caratteri speciali come il segno di percentuale (%) l'invio di un processo non viene eseguito tramite Templeton, perché Templeton interpreta una query con un segno di percentuale come parametro URL.</span><span class="sxs-lookup"><span data-stu-id="af46e-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="af46e-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="af46e-132">-StatusFolder</span></span>
<span data-ttu-id="af46e-133">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo.</span><span class="sxs-lookup"><span data-stu-id="af46e-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="af46e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af46e-134">CommonParameters</span></span>
<span data-ttu-id="af46e-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af46e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af46e-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af46e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af46e-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af46e-137">INPUTS</span></span>

### <span data-ttu-id="af46e-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="af46e-138">None</span></span>

## <span data-ttu-id="af46e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af46e-139">OUTPUTS</span></span>

### <span data-ttu-id="af46e-140">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="af46e-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="af46e-141">Note</span><span class="sxs-lookup"><span data-stu-id="af46e-141">NOTES</span></span>

## <span data-ttu-id="af46e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af46e-142">RELATED LINKS</span></span>

[<span data-ttu-id="af46e-143">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="af46e-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


