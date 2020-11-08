---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
ms.openlocfilehash: 7e9aeebebfc5720ab006d43071eadeabe6bcf655
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020387"
---
# <span data-ttu-id="66133-101">Remove-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="66133-101">Remove-AzBatchNodeFile</span></span>

## <span data-ttu-id="66133-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="66133-102">SYNOPSIS</span></span>
<span data-ttu-id="66133-103">Elimina un file di nodo per un'attività o un nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="66133-103">Deletes a node file for a task or compute node.</span></span>

## <span data-ttu-id="66133-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66133-104">SYNTAX</span></span>

### <span data-ttu-id="66133-105">Attività</span><span class="sxs-lookup"><span data-stu-id="66133-105">Task</span></span>
```
Remove-AzBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66133-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="66133-106">ComputeNode</span></span>
```
Remove-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66133-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="66133-107">InputObject</span></span>
```
Remove-AzBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66133-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66133-108">DESCRIPTION</span></span>
<span data-ttu-id="66133-109">Il cmdlet **Remove-AzBatchNodeFile** Elimina un file di nodo batch di Azure per un'attività o un nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="66133-109">The **Remove-AzBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="66133-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66133-110">EXAMPLES</span></span>

### <span data-ttu-id="66133-111">Esempio 1: eliminare un file associato a un'attività</span><span class="sxs-lookup"><span data-stu-id="66133-111">Example 1: Delete a file associated with a task</span></span>
```
PS C:\>Remove-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="66133-112">Questo comando Elimina il file di nodo denominato wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="66133-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="66133-113">Il file è associato all'attività che contiene l'ID Task26 sotto il processo di lavoro-000001.</span><span class="sxs-lookup"><span data-stu-id="66133-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="66133-114">Esempio 2: eliminare un file da un nodo Compute</span><span class="sxs-lookup"><span data-stu-id="66133-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="66133-115">Questo comando Elimina il file di nodo denominato startup\testFile.txt dal nodo Compute specificato nel pool che contiene l'ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="66133-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="66133-116">Esempio 3: rimuovere un file usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="66133-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="66133-117">Questo comando ottiene il file del nodo utilizzando **Get-AzBatchNodeFile**.</span><span class="sxs-lookup"><span data-stu-id="66133-117">This command gets the node file by using **Get-AzBatchNodeFile**.</span></span>
<span data-ttu-id="66133-118">Il file è associato all'attività che contiene l'ID Task26 sotto il processo di lavoro-000001.</span><span class="sxs-lookup"><span data-stu-id="66133-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="66133-119">Il comando passa il file al cmdlet corrente tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="66133-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="66133-120">Il cmdlet corrente rimuove il file del nodo.</span><span class="sxs-lookup"><span data-stu-id="66133-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="66133-121">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="66133-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="66133-122">Di conseguenza, il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="66133-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="66133-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="66133-123">PARAMETERS</span></span>

### <span data-ttu-id="66133-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="66133-124">-BatchContext</span></span>
<span data-ttu-id="66133-125">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="66133-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="66133-126">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="66133-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="66133-127">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="66133-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="66133-128">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="66133-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="66133-129">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="66133-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="66133-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="66133-130">-ComputeNodeId</span></span>
<span data-ttu-id="66133-131">Specifica l'ID del nodo Compute che contiene il file del nodo batch eliminato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66133-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="66133-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66133-132">-DefaultProfile</span></span>
<span data-ttu-id="66133-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="66133-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66133-134">-Force</span><span class="sxs-lookup"><span data-stu-id="66133-134">-Force</span></span>
<span data-ttu-id="66133-135">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="66133-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66133-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66133-136">-InputObject</span></span>
<span data-ttu-id="66133-137">Specifica l'oggetto **PSNodeFile** che rappresenta il file di nodo eliminato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66133-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="66133-138">Per ottenere un **PSNodeFile** , usare il cmdlet Get-AzBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="66133-138">To obtain a **PSNodeFile** , use the Get-AzBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="66133-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="66133-139">-JobId</span></span>
<span data-ttu-id="66133-140">Specifica l'ID del processo che contiene l'attività.</span><span class="sxs-lookup"><span data-stu-id="66133-140">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="66133-141">-Path</span><span class="sxs-lookup"><span data-stu-id="66133-141">-Path</span></span>
<span data-ttu-id="66133-142">Percorso del file del nodo da eliminare.</span><span class="sxs-lookup"><span data-stu-id="66133-142">The file path of the node file to delete.</span></span>

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

### <span data-ttu-id="66133-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="66133-143">-PoolId</span></span>
<span data-ttu-id="66133-144">Specifica l'ID del pool che contiene i nodi compute per cui questo cmdlet rimuove un file.</span><span class="sxs-lookup"><span data-stu-id="66133-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="66133-145">-Ricorsiva</span><span class="sxs-lookup"><span data-stu-id="66133-145">-Recursive</span></span>
<span data-ttu-id="66133-146">Indica che questo cmdlet elimina la cartella e tutte le sottocartelle e i file nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="66133-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="66133-147">Questo cmdlet è pertinente solo se il percorso è una cartella.</span><span class="sxs-lookup"><span data-stu-id="66133-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="66133-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="66133-148">-TaskId</span></span>
<span data-ttu-id="66133-149">Specifica l'ID dell'attività.</span><span class="sxs-lookup"><span data-stu-id="66133-149">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="66133-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="66133-150">-Confirm</span></span>
<span data-ttu-id="66133-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66133-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66133-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66133-152">-WhatIf</span></span>
<span data-ttu-id="66133-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66133-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66133-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66133-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66133-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66133-155">CommonParameters</span></span>
<span data-ttu-id="66133-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66133-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66133-157">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66133-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66133-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="66133-158">INPUTS</span></span>

### <span data-ttu-id="66133-159">System. String</span><span class="sxs-lookup"><span data-stu-id="66133-159">System.String</span></span>

### <span data-ttu-id="66133-160">Microsoft.Azure.Commands.Batch. Models. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="66133-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="66133-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="66133-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="66133-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66133-162">OUTPUTS</span></span>

### <span data-ttu-id="66133-163">System. void</span><span class="sxs-lookup"><span data-stu-id="66133-163">System.Void</span></span>

## <span data-ttu-id="66133-164">Note</span><span class="sxs-lookup"><span data-stu-id="66133-164">NOTES</span></span>

## <span data-ttu-id="66133-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66133-165">RELATED LINKS</span></span>

[<span data-ttu-id="66133-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="66133-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="66133-167">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="66133-167">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="66133-168">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="66133-168">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)


