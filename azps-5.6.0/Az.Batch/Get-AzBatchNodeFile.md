---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
ms.openlocfilehash: 0169748ffc6fa2004fe8b0ade542d288677776b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007373"
---
# <span data-ttu-id="6b411-101">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="6b411-101">Get-AzBatchNodeFile</span></span>

## <span data-ttu-id="6b411-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b411-102">SYNOPSIS</span></span>
<span data-ttu-id="6b411-103">Recupera le proprietà dei file batch del nodo.</span><span class="sxs-lookup"><span data-stu-id="6b411-103">Gets the properties of Batch node files.</span></span>

## <span data-ttu-id="6b411-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b411-104">SYNTAX</span></span>

### <span data-ttu-id="6b411-105">ComputeNode_Id (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6b411-105">ComputeNode_Id (Default)</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b411-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="6b411-106">Task_Id</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b411-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="6b411-107">Task_ODataFilter</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b411-108">Attività Padre</span><span class="sxs-lookup"><span data-stu-id="6b411-108">ParentTask</span></span>
```
Get-AzBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b411-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="6b411-109">ComputeNode_ODataFilter</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b411-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="6b411-110">ParentComputeNode</span></span>
```
Get-AzBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b411-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6b411-111">DESCRIPTION</span></span>
<span data-ttu-id="6b411-112">Il cmdlet **Get-AzBatchNodeFile** ottiene le proprietà dei file nodo batch di Azure di un'attività o di un nodo di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="6b411-112">The **Get-AzBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="6b411-113">Per limitare i risultati, è possibile specificare un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="6b411-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="6b411-114">Se si specifica un'attività, ma non un filtro, questo cmdlet restituisce le proprietà per tutti i file nodo per l'attività.</span><span class="sxs-lookup"><span data-stu-id="6b411-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="6b411-115">Se si specifica un nodo di calcolo, ma non un filtro, questo cmdlet restituisce le proprietà per tutti i file nodo per quel nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="6b411-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="6b411-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b411-116">EXAMPLES</span></span>

### <span data-ttu-id="6b411-117">Esempio 1: Ottenere le proprietà di un file nodo associato a un'attività</span><span class="sxs-lookup"><span data-stu-id="6b411-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="6b411-118">Questo comando ottiene le proprietà del file StdOut.txt nodo associato all'attività con ID Attività26 nel processo con ID Processo-000001.</span><span class="sxs-lookup"><span data-stu-id="6b411-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="6b411-119">Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="6b411-119">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="6b411-120">Esempio 2: Ottenere le proprietà dei file nodo associati a un'attività con un filtro</span><span class="sxs-lookup"><span data-stu-id="6b411-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="6b411-121">Questo comando ottiene le proprietà dei file nodo i cui nomi iniziano con st e sono associati all'attività con ID Attività26 nel processo con ID Processo-00002.</span><span class="sxs-lookup"><span data-stu-id="6b411-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="6b411-122">Esempio 3: Recuperare in modo ricorsivo le proprietà dei file nodo associati a un'attività</span><span class="sxs-lookup"><span data-stu-id="6b411-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
True        wd                                                               https://cmdletexample.westus.Batch.contoso...
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="6b411-123">Questo comando ottiene le proprietà di tutti i file associati all'attività con ID Attività31 nel processo 00003.</span><span class="sxs-lookup"><span data-stu-id="6b411-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="6b411-124">Questo comando specifica il *parametro ricorsivo.*</span><span class="sxs-lookup"><span data-stu-id="6b411-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="6b411-125">Di conseguenza, il cmdlet esegue una ricerca ricorsiva nei file e restituisce il file wd\newFile.txt nodo.</span><span class="sxs-lookup"><span data-stu-id="6b411-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="6b411-126">Esempio 4: Ottenere un singolo file da un nodo di calcolo</span><span class="sxs-lookup"><span data-stu-id="6b411-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="6b411-127">Questo comando recupera il file denominato Startup\StdOut.txt dal nodo di calcolo che contiene l'ID ComputeNode01 nel pool con l'ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="6b411-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="6b411-128">Esempio 5: Recuperare tutti i file in una cartella da un nodo di calcolo</span><span class="sxs-lookup"><span data-stu-id="6b411-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso...
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="6b411-129">Questo comando recupera tutti i file nella cartella di avvio dal nodo di elaborazione che contiene l'ID ComputeNode01 nel pool con l'ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="6b411-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="6b411-130">Questo cmdlet specifica il *parametro ricorsivo.*</span><span class="sxs-lookup"><span data-stu-id="6b411-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="6b411-131">Esempio 6: Recuperare i file dalla cartella radice di un nodo di calcolo</span><span class="sxs-lookup"><span data-stu-id="6b411-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso...
True        startup                         https://cmdletexample.westus.Batch.contoso...
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="6b411-132">Questo comando recupera tutti i file nella cartella radice del nodo di elaborazione con ID ComputeNode01 nel pool con l'ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="6b411-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="6b411-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b411-133">PARAMETERS</span></span>

### <span data-ttu-id="6b411-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6b411-134">-BatchContext</span></span>
<span data-ttu-id="6b411-135">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="6b411-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6b411-136">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="6b411-136">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6b411-137">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="6b411-137">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6b411-138">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="6b411-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6b411-139">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6b411-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6b411-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="6b411-140">-ComputeNode</span></span>
<span data-ttu-id="6b411-141">Specifica il nodo di calcolo, come oggetto **PSComputeNode,** che contiene i file del nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="6b411-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="6b411-142">Per ottenere un oggetto nodo di calcolo, usare il cmdlet Get-AzBatchComputeNode di calcolo.</span><span class="sxs-lookup"><span data-stu-id="6b411-142">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="6b411-143">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="6b411-143">-ComputeNodeId</span></span>
<span data-ttu-id="6b411-144">Specifica l'ID del nodo di elaborazione che contiene i file del nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="6b411-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

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

### <span data-ttu-id="6b411-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b411-145">-DefaultProfile</span></span>
<span data-ttu-id="6b411-146">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b411-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b411-147">-Filter</span><span class="sxs-lookup"><span data-stu-id="6b411-147">-Filter</span></span>
<span data-ttu-id="6b411-148">Specifica una clausola del filtro OData.</span><span class="sxs-lookup"><span data-stu-id="6b411-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="6b411-149">Questo cmdlet restituisce le proprietà per i file nodo che corrispondono al filtro specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6b411-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

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

### <span data-ttu-id="6b411-150">-JobId</span><span class="sxs-lookup"><span data-stu-id="6b411-150">-JobId</span></span>
<span data-ttu-id="6b411-151">Specifica l'ID del processo che contiene l'attività di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6b411-151">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="6b411-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6b411-152">-MaxCount</span></span>
<span data-ttu-id="6b411-153">Specifica il numero massimo di file nodo per cui questo cmdlet restituisce le proprietà.</span><span class="sxs-lookup"><span data-stu-id="6b411-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="6b411-154">Se si specifica un valore uguale o inferiore a zero (0), il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="6b411-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="6b411-155">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="6b411-155">The default value is 1000.</span></span>

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

### <span data-ttu-id="6b411-156">-Path</span><span class="sxs-lookup"><span data-stu-id="6b411-156">-Path</span></span>
<span data-ttu-id="6b411-157">Specifica il percorso del file nodo per cui questo cmdlet recupera le proprietà.</span><span class="sxs-lookup"><span data-stu-id="6b411-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="6b411-158">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="6b411-158">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b411-159">-PoolId</span><span class="sxs-lookup"><span data-stu-id="6b411-159">-PoolId</span></span>
<span data-ttu-id="6b411-160">Specifica l'ID del pool che contiene il nodo di calcolo da cui ottenere le proprietà dei file nodo.</span><span class="sxs-lookup"><span data-stu-id="6b411-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

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

### <span data-ttu-id="6b411-161">-Ricorsivo</span><span class="sxs-lookup"><span data-stu-id="6b411-161">-Recursive</span></span>
<span data-ttu-id="6b411-162">Indica che questo cmdlet restituisce un elenco ricorsivo di file.</span><span class="sxs-lookup"><span data-stu-id="6b411-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="6b411-163">In caso contrario, restituisce solo i file nella cartella radice.</span><span class="sxs-lookup"><span data-stu-id="6b411-163">Otherwise, it returns only the files in the root folder.</span></span>

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

### <span data-ttu-id="6b411-164">-Attività</span><span class="sxs-lookup"><span data-stu-id="6b411-164">-Task</span></span>
<span data-ttu-id="6b411-165">Specifica l'attività, come oggetto **PSCloudTask,** a cui sono associati i file nodo.</span><span class="sxs-lookup"><span data-stu-id="6b411-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="6b411-166">Per ottenere un oggetto attività, usare il cmdlet Get-AzBatchTask attività.</span><span class="sxs-lookup"><span data-stu-id="6b411-166">To obtain a task object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="6b411-167">-TaskId</span><span class="sxs-lookup"><span data-stu-id="6b411-167">-TaskId</span></span>
<span data-ttu-id="6b411-168">Specifica l'ID dell'attività per cui questo cmdlet ottiene le proprietà dei file nodo.</span><span class="sxs-lookup"><span data-stu-id="6b411-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

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

### <span data-ttu-id="6b411-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b411-169">CommonParameters</span></span>
<span data-ttu-id="6b411-170">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b411-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b411-171">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6b411-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b411-172">INPUT</span><span class="sxs-lookup"><span data-stu-id="6b411-172">INPUTS</span></span>

### <span data-ttu-id="6b411-173">System.String</span><span class="sxs-lookup"><span data-stu-id="6b411-173">System.String</span></span>

### <span data-ttu-id="6b411-174">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="6b411-174">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="6b411-175">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="6b411-175">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="6b411-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6b411-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6b411-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b411-177">OUTPUTS</span></span>

### <span data-ttu-id="6b411-178">Microsoft.Azure.Commands.Batch. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="6b411-178">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

## <span data-ttu-id="6b411-179">NOTE</span><span class="sxs-lookup"><span data-stu-id="6b411-179">NOTES</span></span>

## <span data-ttu-id="6b411-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b411-180">RELATED LINKS</span></span>

[<span data-ttu-id="6b411-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6b411-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6b411-182">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="6b411-182">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="6b411-183">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="6b411-183">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="6b411-184">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6b411-184">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="6b411-185">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="6b411-185">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
