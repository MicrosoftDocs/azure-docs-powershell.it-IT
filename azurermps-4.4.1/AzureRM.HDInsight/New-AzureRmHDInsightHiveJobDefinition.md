---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
ms.openlocfilehash: fd933d157748de424aa425179701897772d93569
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521651"
---
# <span data-ttu-id="11a14-101">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="11a14-101">New-AzureRmHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="11a14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11a14-102">SYNOPSIS</span></span>
<span data-ttu-id="11a14-103">Crea un oggetto processo hive.</span><span class="sxs-lookup"><span data-stu-id="11a14-103">Creates a Hive job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11a14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11a14-104">SYNTAX</span></span>

```
New-AzureRmHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11a14-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11a14-105">DESCRIPTION</span></span>
<span data-ttu-id="11a14-106">Il cmdlet **New-AzureRmHDInsightHiveJobDefinition** definisce un oggetto processo hive da usare con un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="11a14-106">The **New-AzureRmHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="11a14-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11a14-107">EXAMPLES</span></span>

### <span data-ttu-id="11a14-108">Esempio 1: creare una definizione di processo hive</span><span class="sxs-lookup"><span data-stu-id="11a14-108">Example 1: Create a Hive job definition</span></span>
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

<span data-ttu-id="11a14-109">Questo comando crea una definizione di processo hive.</span><span class="sxs-lookup"><span data-stu-id="11a14-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="11a14-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11a14-110">PARAMETERS</span></span>

### <span data-ttu-id="11a14-111">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="11a14-111">-Arguments</span></span>
<span data-ttu-id="11a14-112">Specifica una matrice di argomenti per il processo.</span><span class="sxs-lookup"><span data-stu-id="11a14-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="11a14-113">Gli argomenti vengono passati come argomenti della riga di comando per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="11a14-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="11a14-114">-Definisce</span><span class="sxs-lookup"><span data-stu-id="11a14-114">-Defines</span></span>
<span data-ttu-id="11a14-115">Specifica i valori di configurazione di Hadoop da impostare per l'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="11a14-115">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="11a14-116">-File</span><span class="sxs-lookup"><span data-stu-id="11a14-116">-File</span></span>
<span data-ttu-id="11a14-117">Specifica il percorso di un file che contiene la query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="11a14-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="11a14-118">Il file deve essere disponibile nell'account di archiviazione associato al cluster.</span><span class="sxs-lookup"><span data-stu-id="11a14-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="11a14-119">Puoi usare questo parametro invece del parametro di *query* .</span><span class="sxs-lookup"><span data-stu-id="11a14-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="11a14-120">-File</span><span class="sxs-lookup"><span data-stu-id="11a14-120">-Files</span></span>
<span data-ttu-id="11a14-121">Specifica una raccolta di file associati a un processo hive.</span><span class="sxs-lookup"><span data-stu-id="11a14-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="11a14-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="11a14-122">-JobName</span></span>
<span data-ttu-id="11a14-123">Specifica il nome del processo.</span><span class="sxs-lookup"><span data-stu-id="11a14-123">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="11a14-124">-Query</span><span class="sxs-lookup"><span data-stu-id="11a14-124">-Query</span></span>
<span data-ttu-id="11a14-125">Specifica la query hive.</span><span class="sxs-lookup"><span data-stu-id="11a14-125">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="11a14-126">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="11a14-126">-RunAsFileJob</span></span>
<span data-ttu-id="11a14-127">Indica che questo cmdlet crea un file nell'account di archiviazione di Azure predefinito in cui archiviare una query.</span><span class="sxs-lookup"><span data-stu-id="11a14-127">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="11a14-128">Questo cmdlet invia il processo che fa riferimento a questo file come script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="11a14-128">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="11a14-129">Puoi usare questa funzionalità per gestire caratteri speciali come il segno di percentuale (%) l'invio di un processo non viene eseguito tramite Templeton, perché Templeton interpreta una query con un segno di percentuale come parametro URL.</span><span class="sxs-lookup"><span data-stu-id="11a14-129">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="11a14-130">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="11a14-130">-StatusFolder</span></span>
<span data-ttu-id="11a14-131">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo.</span><span class="sxs-lookup"><span data-stu-id="11a14-131">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="11a14-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11a14-132">-DefaultProfile</span></span>
<span data-ttu-id="11a14-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11a14-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11a14-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11a14-134">CommonParameters</span></span>
<span data-ttu-id="11a14-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11a14-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11a14-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11a14-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11a14-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11a14-137">INPUTS</span></span>

## <span data-ttu-id="11a14-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11a14-138">OUTPUTS</span></span>

### <span data-ttu-id="11a14-139">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="11a14-139">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="11a14-140">Note</span><span class="sxs-lookup"><span data-stu-id="11a14-140">NOTES</span></span>

## <span data-ttu-id="11a14-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11a14-141">RELATED LINKS</span></span>

[<span data-ttu-id="11a14-142">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="11a14-142">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


