---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 242161a7a02cf3767ecd87dfc6e91a7ffba97eb3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193313"
---
# <span data-ttu-id="8a871-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8a871-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="8a871-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a871-102">SYNOPSIS</span></span>
<span data-ttu-id="8a871-103">Crea un oggetto processo hive.</span><span class="sxs-lookup"><span data-stu-id="8a871-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="8a871-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a871-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a871-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a871-105">DESCRIPTION</span></span>
<span data-ttu-id="8a871-106">Il cmdlet **New-AzHDInsightHiveJobDefinition** definisce un oggetto processo hive da usare con un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="8a871-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="8a871-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a871-107">EXAMPLES</span></span>

### <span data-ttu-id="8a871-108">Esempio 1: creare una definizione di processo hive</span><span class="sxs-lookup"><span data-stu-id="8a871-108">Example 1: Create a Hive job definition</span></span>
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

<span data-ttu-id="8a871-109">Questo comando crea una definizione di processo hive.</span><span class="sxs-lookup"><span data-stu-id="8a871-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="8a871-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a871-110">PARAMETERS</span></span>

### <span data-ttu-id="8a871-111">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="8a871-111">-Arguments</span></span>
<span data-ttu-id="8a871-112">Specifica una matrice di argomenti per il processo.</span><span class="sxs-lookup"><span data-stu-id="8a871-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="8a871-113">Gli argomenti vengono passati come argomenti della riga di comando per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="8a871-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="8a871-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a871-114">-DefaultProfile</span></span>
<span data-ttu-id="8a871-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8a871-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a871-116">-Definisce</span><span class="sxs-lookup"><span data-stu-id="8a871-116">-Defines</span></span>
<span data-ttu-id="8a871-117">Specifica i valori di configurazione di Hadoop da impostare per l'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="8a871-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="8a871-118">-File</span><span class="sxs-lookup"><span data-stu-id="8a871-118">-File</span></span>
<span data-ttu-id="8a871-119">Specifica il percorso di un file che contiene la query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="8a871-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="8a871-120">Il file deve essere disponibile nell'account di archiviazione associato al cluster.</span><span class="sxs-lookup"><span data-stu-id="8a871-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="8a871-121">Puoi usare questo parametro invece del parametro di *query* .</span><span class="sxs-lookup"><span data-stu-id="8a871-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="8a871-122">-File</span><span class="sxs-lookup"><span data-stu-id="8a871-122">-Files</span></span>
<span data-ttu-id="8a871-123">Specifica una raccolta di file associati a un processo hive.</span><span class="sxs-lookup"><span data-stu-id="8a871-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="8a871-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="8a871-124">-JobName</span></span>
<span data-ttu-id="8a871-125">Specifica il nome del processo.</span><span class="sxs-lookup"><span data-stu-id="8a871-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="8a871-126">-Query</span><span class="sxs-lookup"><span data-stu-id="8a871-126">-Query</span></span>
<span data-ttu-id="8a871-127">Specifica la query hive.</span><span class="sxs-lookup"><span data-stu-id="8a871-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="8a871-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="8a871-128">-RunAsFileJob</span></span>
<span data-ttu-id="8a871-129">Indica che questo cmdlet crea un file nell'account di archiviazione di Azure predefinito in cui archiviare una query.</span><span class="sxs-lookup"><span data-stu-id="8a871-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="8a871-130">Questo cmdlet invia il processo che fa riferimento a questo file come script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="8a871-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="8a871-131">Puoi usare questa funzionalità per gestire caratteri speciali come il segno di percentuale (%) l'invio di un processo non viene eseguito tramite Templeton, perché Templeton interpreta una query con un segno di percentuale come parametro URL.</span><span class="sxs-lookup"><span data-stu-id="8a871-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="8a871-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="8a871-132">-StatusFolder</span></span>
<span data-ttu-id="8a871-133">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo.</span><span class="sxs-lookup"><span data-stu-id="8a871-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="8a871-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a871-134">CommonParameters</span></span>
<span data-ttu-id="8a871-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a871-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a871-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a871-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a871-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a871-137">INPUTS</span></span>

### <span data-ttu-id="8a871-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8a871-138">None</span></span>

## <span data-ttu-id="8a871-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a871-139">OUTPUTS</span></span>

### <span data-ttu-id="8a871-140">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8a871-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="8a871-141">Note</span><span class="sxs-lookup"><span data-stu-id="8a871-141">NOTES</span></span>

## <span data-ttu-id="8a871-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a871-142">RELATED LINKS</span></span>

[<span data-ttu-id="8a871-143">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8a871-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


