---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
ms.openlocfilehash: 3e4748a8bc5e5c04868fb7c2d4179c07ea63c905
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511171"
---
# <span data-ttu-id="c7988-101">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c7988-101">New-AzureRmHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="c7988-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7988-102">SYNOPSIS</span></span>
<span data-ttu-id="c7988-103">Crea un oggetto processo hive.</span><span class="sxs-lookup"><span data-stu-id="c7988-103">Creates a Hive job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7988-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7988-104">SYNTAX</span></span>

```
New-AzureRmHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7988-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7988-105">DESCRIPTION</span></span>
<span data-ttu-id="c7988-106">Il cmdlet **New-AzureRmHDInsightHiveJobDefinition** definisce un oggetto processo hive da usare con un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7988-106">The **New-AzureRmHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c7988-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7988-107">EXAMPLES</span></span>

### <span data-ttu-id="c7988-108">Esempio 1: creare una definizione di processo hive</span><span class="sxs-lookup"><span data-stu-id="c7988-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="c7988-109">Questo comando crea una definizione di processo hive.</span><span class="sxs-lookup"><span data-stu-id="c7988-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="c7988-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7988-110">PARAMETERS</span></span>

### <span data-ttu-id="c7988-111">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="c7988-111">-Arguments</span></span>
<span data-ttu-id="c7988-112">Specifica una matrice di argomenti per il processo.</span><span class="sxs-lookup"><span data-stu-id="c7988-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="c7988-113">Gli argomenti vengono passati come argomenti della riga di comando per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="c7988-113">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7988-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7988-114">-DefaultProfile</span></span>
<span data-ttu-id="c7988-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c7988-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7988-116">-Definisce</span><span class="sxs-lookup"><span data-stu-id="c7988-116">-Defines</span></span>
<span data-ttu-id="c7988-117">Specifica i valori di configurazione di Hadoop da impostare per l'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="c7988-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7988-118">-File</span><span class="sxs-lookup"><span data-stu-id="c7988-118">-File</span></span>
<span data-ttu-id="c7988-119">Specifica il percorso di un file che contiene la query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="c7988-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="c7988-120">Il file deve essere disponibile nell'account di archiviazione associato al cluster.</span><span class="sxs-lookup"><span data-stu-id="c7988-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="c7988-121">Puoi usare questo parametro invece del parametro di *query* .</span><span class="sxs-lookup"><span data-stu-id="c7988-121">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7988-122">-File</span><span class="sxs-lookup"><span data-stu-id="c7988-122">-Files</span></span>
<span data-ttu-id="c7988-123">Specifica una raccolta di file associati a un processo hive.</span><span class="sxs-lookup"><span data-stu-id="c7988-123">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7988-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="c7988-124">-JobName</span></span>
<span data-ttu-id="c7988-125">Specifica il nome del processo.</span><span class="sxs-lookup"><span data-stu-id="c7988-125">Specifies the name of the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7988-126">-Query</span><span class="sxs-lookup"><span data-stu-id="c7988-126">-Query</span></span>
<span data-ttu-id="c7988-127">Specifica la query hive.</span><span class="sxs-lookup"><span data-stu-id="c7988-127">Specifies the Hive query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7988-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="c7988-128">-RunAsFileJob</span></span>
<span data-ttu-id="c7988-129">Indica che questo cmdlet crea un file nell'account di archiviazione di Azure predefinito in cui archiviare una query.</span><span class="sxs-lookup"><span data-stu-id="c7988-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="c7988-130">Questo cmdlet invia il processo che fa riferimento a questo file come script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="c7988-130">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="c7988-131">Puoi usare questa funzionalità per gestire caratteri speciali come il segno di percentuale (%) l'invio di un processo non viene eseguito tramite Templeton, perché Templeton interpreta una query con un segno di percentuale come parametro URL.</span><span class="sxs-lookup"><span data-stu-id="c7988-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7988-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="c7988-132">-StatusFolder</span></span>
<span data-ttu-id="c7988-133">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo.</span><span class="sxs-lookup"><span data-stu-id="c7988-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7988-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7988-134">CommonParameters</span></span>
<span data-ttu-id="c7988-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7988-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7988-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7988-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7988-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7988-137">INPUTS</span></span>

### <span data-ttu-id="c7988-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c7988-138">None</span></span>
<span data-ttu-id="c7988-139">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c7988-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7988-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7988-140">OUTPUTS</span></span>

### <span data-ttu-id="c7988-141">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c7988-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="c7988-142">Note</span><span class="sxs-lookup"><span data-stu-id="c7988-142">NOTES</span></span>

## <span data-ttu-id="c7988-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7988-143">RELATED LINKS</span></span>

[<span data-ttu-id="c7988-144">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c7988-144">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


