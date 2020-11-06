---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
ms.openlocfilehash: 5b8797cf2f6068098d1ca407f0f97283dd171af5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517044"
---
# <span data-ttu-id="5e692-101">Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="5e692-101">Remove-AzureBatchNodeFile</span></span>

## <span data-ttu-id="5e692-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e692-102">SYNOPSIS</span></span>
<span data-ttu-id="5e692-103">Elimina un file di nodo per un'attività o un nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="5e692-103">Deletes a node file for a task or compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e692-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e692-104">SYNTAX</span></span>

### <span data-ttu-id="5e692-105">Attività</span><span class="sxs-lookup"><span data-stu-id="5e692-105">Task</span></span>
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e692-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="5e692-106">ComputeNode</span></span>
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e692-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="5e692-107">InputObject</span></span>
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e692-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e692-108">DESCRIPTION</span></span>
<span data-ttu-id="5e692-109">Il cmdlet **Remove-AzureBatchNodeFile** Elimina un file di nodo batch di Azure per un'attività o un nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="5e692-109">The **Remove-AzureBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="5e692-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e692-110">EXAMPLES</span></span>

### <span data-ttu-id="5e692-111">Esempio 1: eliminare un file assocated con un'attività</span><span class="sxs-lookup"><span data-stu-id="5e692-111">Example 1: Delete a file assocated with a task</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="5e692-112">Questo comando Elimina il file di nodo denominato wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="5e692-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="5e692-113">Il file è associato all'attività che contiene l'ID Task26 sotto il processo di lavoro-000001.</span><span class="sxs-lookup"><span data-stu-id="5e692-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="5e692-114">Esempio 2: eliminare un file da un nodo Compute</span><span class="sxs-lookup"><span data-stu-id="5e692-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Name "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="5e692-115">Questo comando Elimina il file di nodo denominato startup\testFile.txt dal nodo Compute specificato nel pool che contiene l'ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="5e692-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="5e692-116">Esempio 3: rimuovere un file usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="5e692-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="5e692-117">Questo comando ottiene il file del nodo utilizzando **Get-AzureBatchNodeFile**.</span><span class="sxs-lookup"><span data-stu-id="5e692-117">This command gets the node file by using **Get-AzureBatchNodeFile**.</span></span>
<span data-ttu-id="5e692-118">Il file è associato all'attività che contiene l'ID Task26 sotto il processo di lavoro-000001.</span><span class="sxs-lookup"><span data-stu-id="5e692-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="5e692-119">Il comando passa il file al cmdlet corrente tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="5e692-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="5e692-120">Il cmdlet corrente rimuove il file del nodo.</span><span class="sxs-lookup"><span data-stu-id="5e692-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="5e692-121">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="5e692-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="5e692-122">Di conseguenza, il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="5e692-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5e692-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e692-123">PARAMETERS</span></span>

### <span data-ttu-id="5e692-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5e692-124">-BatchContext</span></span>
<span data-ttu-id="5e692-125">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="5e692-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5e692-126">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="5e692-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="5e692-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="5e692-127">-ComputeNodeId</span></span>
<span data-ttu-id="5e692-128">Specifica l'ID del nodo Compute che contiene il file del nodo batch eliminato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e692-128">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="5e692-129">-Force</span><span class="sxs-lookup"><span data-stu-id="5e692-129">-Force</span></span>
<span data-ttu-id="5e692-130">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5e692-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5e692-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e692-131">-InputObject</span></span>
<span data-ttu-id="5e692-132">Specifica l'oggetto **PSNodeFile** che rappresenta il file di nodo eliminato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e692-132">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="5e692-133">Per ottenere un **PSNodeFile** , usare il cmdlet Get-AzureBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="5e692-133">To obtain a **PSNodeFile** , use the Get-AzureBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="5e692-134">-JobId</span><span class="sxs-lookup"><span data-stu-id="5e692-134">-JobId</span></span>
<span data-ttu-id="5e692-135">Specifica l'ID del processo che contiene l'attività.</span><span class="sxs-lookup"><span data-stu-id="5e692-135">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="5e692-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e692-136">-Name</span></span>
<span data-ttu-id="5e692-137">Specifica il nome del file di nodo eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e692-137">Specifies the name of the node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e692-138">-PoolId</span><span class="sxs-lookup"><span data-stu-id="5e692-138">-PoolId</span></span>
<span data-ttu-id="5e692-139">Specifica l'ID del pool che contiene i nodi compute per cui questo cmdlet rimuove un file.</span><span class="sxs-lookup"><span data-stu-id="5e692-139">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="5e692-140">-Ricorsiva</span><span class="sxs-lookup"><span data-stu-id="5e692-140">-Recursive</span></span>
<span data-ttu-id="5e692-141">Indica che questo cmdlet elimina la cartella e tutte le sottocartelle e i file nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="5e692-141">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="5e692-142">Questo cmdlet è pertinente solo se il percorso è una cartella.</span><span class="sxs-lookup"><span data-stu-id="5e692-142">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="5e692-143">-TaskId</span><span class="sxs-lookup"><span data-stu-id="5e692-143">-TaskId</span></span>
<span data-ttu-id="5e692-144">Specifica l'ID dell'attività.</span><span class="sxs-lookup"><span data-stu-id="5e692-144">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="5e692-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5e692-145">-Confirm</span></span>
<span data-ttu-id="5e692-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e692-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e692-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e692-147">-WhatIf</span></span>
<span data-ttu-id="5e692-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e692-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e692-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e692-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e692-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e692-150">-DefaultProfile</span></span>
<span data-ttu-id="5e692-151">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e692-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e692-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e692-152">CommonParameters</span></span>
<span data-ttu-id="5e692-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e692-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e692-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e692-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e692-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e692-155">INPUTS</span></span>

### <span data-ttu-id="5e692-156">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5e692-156">BatchAccountContext</span></span>
<span data-ttu-id="5e692-157">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5e692-157">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5e692-158">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="5e692-158">PSNodeFile</span></span>
<span data-ttu-id="5e692-159">Il parametro ' InputObject ' accetta il valore di tipo ' PSNodeFile ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5e692-159">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="5e692-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e692-160">OUTPUTS</span></span>

## <span data-ttu-id="5e692-161">Note</span><span class="sxs-lookup"><span data-stu-id="5e692-161">NOTES</span></span>

## <span data-ttu-id="5e692-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e692-162">RELATED LINKS</span></span>

[<span data-ttu-id="5e692-163">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5e692-163">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5e692-164">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="5e692-164">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="5e692-165">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="5e692-165">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)


