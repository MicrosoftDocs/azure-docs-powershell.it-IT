---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
ms.openlocfilehash: 0a027bd15d4b207baf9c69fcb9104428c2881872
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687549"
---
# <span data-ttu-id="081a7-101">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="081a7-101">Get-AzureBatchNodeFile</span></span>

## <span data-ttu-id="081a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="081a7-102">SYNOPSIS</span></span>
<span data-ttu-id="081a7-103">Ottiene le proprietà dei file del nodo batch.</span><span class="sxs-lookup"><span data-stu-id="081a7-103">Gets the properties of Batch node files.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="081a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="081a7-104">SYNTAX</span></span>

### <span data-ttu-id="081a7-105">ComputeNode_Id (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="081a7-105">ComputeNode_Id (Default)</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Name] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081a7-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="081a7-106">Task_Id</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [[-Name] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081a7-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="081a7-107">Task_ODataFilter</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081a7-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="081a7-108">ParentTask</span></span>
```
Get-AzureBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081a7-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="081a7-109">ComputeNode_ODataFilter</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="081a7-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="081a7-110">ParentComputeNode</span></span>
```
Get-AzureBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="081a7-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="081a7-111">DESCRIPTION</span></span>
<span data-ttu-id="081a7-112">Il cmdlet **Get-AzureBatchNodeFile** ottiene le proprietà dei file di nodo batch di Azure di un'attività o di un nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="081a7-112">The **Get-AzureBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="081a7-113">Per restringere i risultati, è possibile specificare un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="081a7-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="081a7-114">Se si specifica un'attività, ma non un filtro, questo cmdlet restituisce le proprietà per tutti i file di nodo per l'attività.</span><span class="sxs-lookup"><span data-stu-id="081a7-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="081a7-115">Se si specifica un nodo COMPUTE, ma non un filtro, questo cmdlet restituisce le proprietà per tutti i file di nodo per il nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="081a7-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="081a7-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="081a7-116">EXAMPLES</span></span>

### <span data-ttu-id="081a7-117">Esempio 1: ottenere le proprietà di un file di nodo associato a un'attività</span><span class="sxs-lookup"><span data-stu-id="081a7-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="081a7-118">Questo comando consente di ottenere le proprietà del file di nodo StdOut.txt associato all'attività che contiene l'ID Task26 nel processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="081a7-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="081a7-119">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="081a7-119">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="081a7-120">Esempio 2: ottenere le proprietà dei file di nodo associati a un'attività usando un filtro</span><span class="sxs-lookup"><span data-stu-id="081a7-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="081a7-121">Questo comando consente di ottenere le proprietà dei file di nodo i cui nomi iniziano con la St e sono associati a un'attività con l'ID Task26 in job che contiene l'ID Job-00002.</span><span class="sxs-lookup"><span data-stu-id="081a7-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="081a7-122">Esempio 3: ottenere ricorsivamente le proprietà dei file di nodo associati a un'attività</span><span class="sxs-lookup"><span data-stu-id="081a7-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzureBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzureBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        wd                                                               https://cmdletexample.westus.Batch.contoso... 
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="081a7-123">Questo comando consente di ottenere le proprietà di tutti i file associati all'attività che contiene l'ID Task31 nel processo di lavoro-00003.</span><span class="sxs-lookup"><span data-stu-id="081a7-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="081a7-124">Questo comando specifica il parametro *ricorsivo* .</span><span class="sxs-lookup"><span data-stu-id="081a7-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="081a7-125">Di conseguenza, il cmdlet esegue una ricerca ricorsiva di file e restituisce il file del nodo wd\newFile.txt.</span><span class="sxs-lookup"><span data-stu-id="081a7-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="081a7-126">Esempio 4: ottenere un singolo file da un nodo Compute</span><span class="sxs-lookup"><span data-stu-id="081a7-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="081a7-127">Questo comando ottiene il file denominato Startup\StdOut.txt dal nodo Compute che contiene l'ID ComputeNode01 nel pool che contiene l'ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="081a7-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="081a7-128">Esempio 5: ottenere tutti i file in una cartella da un nodo Compute</span><span class="sxs-lookup"><span data-stu-id="081a7-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso... 
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="081a7-129">Questo comando consente di ottenere tutti i file nella cartella di avvio dal nodo Compute che contiene l'ID ComputeNode01 nel pool che contiene l'ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="081a7-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="081a7-130">Questo cmdlet specifica il parametro *ricorsivo* .</span><span class="sxs-lookup"><span data-stu-id="081a7-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="081a7-131">Esempio 6: recuperare i file dalla cartella radice di un nodo Compute</span><span class="sxs-lookup"><span data-stu-id="081a7-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzureBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzureBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso... 
True        startup                         https://cmdletexample.westus.Batch.contoso... 
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="081a7-132">Questo comando consente di ottenere tutti i file nella cartella radice del nodo Compute che contiene l'ID ComputeNode01 nel pool con l'ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="081a7-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="081a7-133">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="081a7-133">PARAMETERS</span></span>

### <span data-ttu-id="081a7-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="081a7-134">-BatchContext</span></span>
<span data-ttu-id="081a7-135">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="081a7-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="081a7-136">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="081a7-136">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="081a7-137">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="081a7-137">-ComputeNode</span></span>
<span data-ttu-id="081a7-138">Specifica il nodo COMPUTE, come oggetto **PSComputeNode** , che contiene i file del nodo batch.</span><span class="sxs-lookup"><span data-stu-id="081a7-138">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="081a7-139">Per ottenere un oggetto compute node, usa il cmdlet Get-AzureBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="081a7-139">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentComputeNode
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="081a7-140">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="081a7-140">-ComputeNodeId</span></span>
<span data-ttu-id="081a7-141">Specifica l'ID del nodo Compute che contiene i file del nodo batch.</span><span class="sxs-lookup"><span data-stu-id="081a7-141">Specifies the ID of the compute node that contains the Batch node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="081a7-142">-Filtro</span><span class="sxs-lookup"><span data-stu-id="081a7-142">-Filter</span></span>
<span data-ttu-id="081a7-143">Specifica una clausola di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="081a7-143">Specifies an OData filter clause.</span></span>
<span data-ttu-id="081a7-144">Questo cmdlet restituisce le proprietà per i file di nodo che corrispondono al filtro specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="081a7-144">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="081a7-145">-JobId</span><span class="sxs-lookup"><span data-stu-id="081a7-145">-JobId</span></span>
<span data-ttu-id="081a7-146">Specifica l'ID del processo che contiene l'attività di destinazione.</span><span class="sxs-lookup"><span data-stu-id="081a7-146">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="081a7-147">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="081a7-147">-MaxCount</span></span>
<span data-ttu-id="081a7-148">Specifica il numero massimo di file di nodo per cui questo cmdlet restituisce le proprietà.</span><span class="sxs-lookup"><span data-stu-id="081a7-148">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="081a7-149">Se specifichi un valore pari a zero (0) o meno, il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="081a7-149">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="081a7-150">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="081a7-150">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="081a7-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="081a7-151">-Name</span></span>
<span data-ttu-id="081a7-152">Specifica il nome del file di nodo per cui questo cmdlet recupera le proprietà.</span><span class="sxs-lookup"><span data-stu-id="081a7-152">Specifies the name of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="081a7-153">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="081a7-153">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="081a7-154">-PoolId</span><span class="sxs-lookup"><span data-stu-id="081a7-154">-PoolId</span></span>
<span data-ttu-id="081a7-155">Specifica l'ID del pool che contiene il nodo Compute da cui ottenere le proprietà dei file di nodo.</span><span class="sxs-lookup"><span data-stu-id="081a7-155">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="081a7-156">-Ricorsiva</span><span class="sxs-lookup"><span data-stu-id="081a7-156">-Recursive</span></span>
<span data-ttu-id="081a7-157">Indica che questo cmdlet restituisce un elenco ricorsivo di file.</span><span class="sxs-lookup"><span data-stu-id="081a7-157">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="081a7-158">In caso contrario, restituisce solo i file nella cartella radice.</span><span class="sxs-lookup"><span data-stu-id="081a7-158">Otherwise, it returns only the files in the root folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="081a7-159">-Attività</span><span class="sxs-lookup"><span data-stu-id="081a7-159">-Task</span></span>
<span data-ttu-id="081a7-160">Specifica l'attività, come oggetto **PSCloudTask** , con cui sono associati i file del nodo.</span><span class="sxs-lookup"><span data-stu-id="081a7-160">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="081a7-161">Per ottenere un oggetto Task, usare il cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="081a7-161">To obtain a task object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentTask
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="081a7-162">-TaskId</span><span class="sxs-lookup"><span data-stu-id="081a7-162">-TaskId</span></span>
<span data-ttu-id="081a7-163">Specifica l'ID dell'attività per cui questo cmdlet ottiene le proprietà dei file di nodi.</span><span class="sxs-lookup"><span data-stu-id="081a7-163">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="081a7-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="081a7-164">-DefaultProfile</span></span>
<span data-ttu-id="081a7-165">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="081a7-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="081a7-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="081a7-166">CommonParameters</span></span>
<span data-ttu-id="081a7-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="081a7-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="081a7-168">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="081a7-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="081a7-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="081a7-169">INPUTS</span></span>

### <span data-ttu-id="081a7-170">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="081a7-170">BatchAccountContext</span></span>
<span data-ttu-id="081a7-171">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="081a7-171">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="081a7-172">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="081a7-172">PSComputeNode</span></span>
<span data-ttu-id="081a7-173">Il parametro ' ComputeNode ' accetta il valore di tipo ' PSComputeNode ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="081a7-173">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

### <span data-ttu-id="081a7-174">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="081a7-174">PSCloudTask</span></span>
<span data-ttu-id="081a7-175">Il parametro ' Task ' accetta il valore di tipo ' PSCloudTask ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="081a7-175">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="081a7-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="081a7-176">OUTPUTS</span></span>

### <span data-ttu-id="081a7-177">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="081a7-177">PSNodeFile</span></span>

## <span data-ttu-id="081a7-178">Note</span><span class="sxs-lookup"><span data-stu-id="081a7-178">NOTES</span></span>

## <span data-ttu-id="081a7-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="081a7-179">RELATED LINKS</span></span>

[<span data-ttu-id="081a7-180">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="081a7-180">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="081a7-181">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="081a7-181">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="081a7-182">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="081a7-182">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="081a7-183">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="081a7-183">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="081a7-184">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="081a7-184">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


