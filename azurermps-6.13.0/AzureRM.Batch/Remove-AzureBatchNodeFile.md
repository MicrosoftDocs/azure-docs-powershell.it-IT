---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
ms.openlocfilehash: a81d77ac1761c37dc3042394a4a70bda6848cc83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685949"
---
# <span data-ttu-id="82a60-101">Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="82a60-101">Remove-AzureBatchNodeFile</span></span>

## <span data-ttu-id="82a60-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82a60-102">SYNOPSIS</span></span>
<span data-ttu-id="82a60-103">Elimina un file di nodo per un'attività o un nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="82a60-103">Deletes a node file for a task or compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82a60-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82a60-104">SYNTAX</span></span>

### <span data-ttu-id="82a60-105">Attività</span><span class="sxs-lookup"><span data-stu-id="82a60-105">Task</span></span>
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82a60-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="82a60-106">ComputeNode</span></span>
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82a60-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="82a60-107">InputObject</span></span>
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82a60-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82a60-108">DESCRIPTION</span></span>
<span data-ttu-id="82a60-109">Il cmdlet **Remove-AzureBatchNodeFile** Elimina un file di nodo batch di Azure per un'attività o un nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="82a60-109">The **Remove-AzureBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="82a60-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82a60-110">EXAMPLES</span></span>

### <span data-ttu-id="82a60-111">Esempio 1: eliminare un file assocated con un'attività</span><span class="sxs-lookup"><span data-stu-id="82a60-111">Example 1: Delete a file assocated with a task</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="82a60-112">Questo comando Elimina il file di nodo denominato wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="82a60-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="82a60-113">Il file è associato all'attività che contiene l'ID Task26 sotto il processo di lavoro-000001.</span><span class="sxs-lookup"><span data-stu-id="82a60-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="82a60-114">Esempio 2: eliminare un file da un nodo Compute</span><span class="sxs-lookup"><span data-stu-id="82a60-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="82a60-115">Questo comando Elimina il file di nodo denominato startup\testFile.txt dal nodo Compute specificato nel pool che contiene l'ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="82a60-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="82a60-116">Esempio 3: rimuovere un file usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="82a60-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="82a60-117">Questo comando ottiene il file del nodo utilizzando **Get-AzureBatchNodeFile**.</span><span class="sxs-lookup"><span data-stu-id="82a60-117">This command gets the node file by using **Get-AzureBatchNodeFile**.</span></span>
<span data-ttu-id="82a60-118">Il file è associato all'attività che contiene l'ID Task26 sotto il processo di lavoro-000001.</span><span class="sxs-lookup"><span data-stu-id="82a60-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="82a60-119">Il comando passa il file al cmdlet corrente tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="82a60-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="82a60-120">Il cmdlet corrente rimuove il file del nodo.</span><span class="sxs-lookup"><span data-stu-id="82a60-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="82a60-121">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="82a60-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="82a60-122">Di conseguenza, il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="82a60-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="82a60-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82a60-123">PARAMETERS</span></span>

### <span data-ttu-id="82a60-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="82a60-124">-BatchContext</span></span>
<span data-ttu-id="82a60-125">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="82a60-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="82a60-126">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="82a60-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="82a60-127">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="82a60-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="82a60-128">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="82a60-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="82a60-129">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="82a60-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="82a60-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="82a60-130">-ComputeNodeId</span></span>
<span data-ttu-id="82a60-131">Specifica l'ID del nodo Compute che contiene il file del nodo batch eliminato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82a60-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82a60-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82a60-132">-DefaultProfile</span></span>
<span data-ttu-id="82a60-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82a60-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82a60-134">-Force</span><span class="sxs-lookup"><span data-stu-id="82a60-134">-Force</span></span>
<span data-ttu-id="82a60-135">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="82a60-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="82a60-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82a60-136">-InputObject</span></span>
<span data-ttu-id="82a60-137">Specifica l'oggetto **PSNodeFile** che rappresenta il file di nodo eliminato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82a60-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="82a60-138">Per ottenere un **PSNodeFile** , usare il cmdlet Get-AzureBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="82a60-138">To obtain a **PSNodeFile** , use the Get-AzureBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82a60-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="82a60-139">-JobId</span></span>
<span data-ttu-id="82a60-140">Specifica l'ID del processo che contiene l'attività.</span><span class="sxs-lookup"><span data-stu-id="82a60-140">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82a60-141">-Path</span><span class="sxs-lookup"><span data-stu-id="82a60-141">-Path</span></span>
<span data-ttu-id="82a60-142">Percorso del file del nodo da eliminare.</span><span class="sxs-lookup"><span data-stu-id="82a60-142">The file path of the node file to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a60-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="82a60-143">-PoolId</span></span>
<span data-ttu-id="82a60-144">Specifica l'ID del pool che contiene i nodi compute per cui questo cmdlet rimuove un file.</span><span class="sxs-lookup"><span data-stu-id="82a60-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82a60-145">-Ricorsiva</span><span class="sxs-lookup"><span data-stu-id="82a60-145">-Recursive</span></span>
<span data-ttu-id="82a60-146">Indica che questo cmdlet elimina la cartella e tutte le sottocartelle e i file nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="82a60-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="82a60-147">Questo cmdlet è pertinente solo se il percorso è una cartella.</span><span class="sxs-lookup"><span data-stu-id="82a60-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="82a60-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="82a60-148">-TaskId</span></span>
<span data-ttu-id="82a60-149">Specifica l'ID dell'attività.</span><span class="sxs-lookup"><span data-stu-id="82a60-149">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82a60-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="82a60-150">-Confirm</span></span>
<span data-ttu-id="82a60-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82a60-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a60-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82a60-152">-WhatIf</span></span>
<span data-ttu-id="82a60-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82a60-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82a60-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82a60-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a60-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a60-155">CommonParameters</span></span>
<span data-ttu-id="82a60-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82a60-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a60-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82a60-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a60-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82a60-158">INPUTS</span></span>

### <span data-ttu-id="82a60-159">System. String</span><span class="sxs-lookup"><span data-stu-id="82a60-159">System.String</span></span>

### <span data-ttu-id="82a60-160">Microsoft.Azure.Commands.Batch. Models. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="82a60-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>
<span data-ttu-id="82a60-161">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="82a60-161">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="82a60-162">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="82a60-162">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="82a60-163">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="82a60-163">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="82a60-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82a60-164">OUTPUTS</span></span>

### <span data-ttu-id="82a60-165">System. void</span><span class="sxs-lookup"><span data-stu-id="82a60-165">System.Void</span></span>

## <span data-ttu-id="82a60-166">Note</span><span class="sxs-lookup"><span data-stu-id="82a60-166">NOTES</span></span>

## <span data-ttu-id="82a60-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82a60-167">RELATED LINKS</span></span>

[<span data-ttu-id="82a60-168">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="82a60-168">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="82a60-169">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="82a60-169">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="82a60-170">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="82a60-170">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)


