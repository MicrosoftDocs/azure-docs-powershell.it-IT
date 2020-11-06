---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: fdcc1b7a119028d792000b10d26aa7900ab0477b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517595"
---
# <span data-ttu-id="6db1a-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6db1a-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="6db1a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6db1a-102">SYNOPSIS</span></span>
<span data-ttu-id="6db1a-103">Riattiva un'attività.</span><span class="sxs-lookup"><span data-stu-id="6db1a-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6db1a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6db1a-104">SYNTAX</span></span>

### <span data-ttu-id="6db1a-105">ID</span><span class="sxs-lookup"><span data-stu-id="6db1a-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6db1a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6db1a-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6db1a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6db1a-107">DESCRIPTION</span></span>
<span data-ttu-id="6db1a-108">Il cmdlet **Enable-AzureBatchTask** riattiva un'attività.</span><span class="sxs-lookup"><span data-stu-id="6db1a-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="6db1a-109">Se un'attività ha esaurito il numero di tentativi, questo cmdlet consente comunque l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6db1a-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="6db1a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6db1a-110">EXAMPLES</span></span>

### <span data-ttu-id="6db1a-111">Esempio 1: riattivare un'attività</span><span class="sxs-lookup"><span data-stu-id="6db1a-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="6db1a-112">Questo comando riattiva l'attività Task2 in Job Job7.</span><span class="sxs-lookup"><span data-stu-id="6db1a-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="6db1a-113">Esempio 2: riattivare un'attività usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="6db1a-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="6db1a-114">Questo comando consente di ottenere l'attività batch con ID Task3 nel processo che contiene l'ID Job8 usando il cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="6db1a-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="6db1a-115">Il comando passa l'attività al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="6db1a-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6db1a-116">Il comando riattiva l'attività.</span><span class="sxs-lookup"><span data-stu-id="6db1a-116">The command reactivates that task.</span></span>

## <span data-ttu-id="6db1a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6db1a-117">PARAMETERS</span></span>

### <span data-ttu-id="6db1a-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6db1a-118">-BatchContext</span></span>
<span data-ttu-id="6db1a-119">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="6db1a-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6db1a-120">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="6db1a-120">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6db1a-121">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="6db1a-121">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6db1a-122">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="6db1a-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6db1a-123">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6db1a-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6db1a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db1a-124">-DefaultProfile</span></span>
<span data-ttu-id="6db1a-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6db1a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6db1a-126">-ID</span><span class="sxs-lookup"><span data-stu-id="6db1a-126">-Id</span></span>
<span data-ttu-id="6db1a-127">Specifica l'ID dell'attività da riattivare.</span><span class="sxs-lookup"><span data-stu-id="6db1a-127">Specifies the ID of the task to reactivate.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6db1a-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="6db1a-128">-JobId</span></span>
<span data-ttu-id="6db1a-129">Specifica l'ID del processo che contiene l'attività.</span><span class="sxs-lookup"><span data-stu-id="6db1a-129">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6db1a-130">-Attività</span><span class="sxs-lookup"><span data-stu-id="6db1a-130">-Task</span></span>
<span data-ttu-id="6db1a-131">Specifica l'attività riattivata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6db1a-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="6db1a-132">Per ottenere un oggetto **PSCloudTask** , usa il cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="6db1a-132">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6db1a-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6db1a-133">-Confirm</span></span>
<span data-ttu-id="6db1a-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6db1a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6db1a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6db1a-135">-WhatIf</span></span>
<span data-ttu-id="6db1a-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6db1a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6db1a-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6db1a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6db1a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db1a-138">CommonParameters</span></span>
<span data-ttu-id="6db1a-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6db1a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db1a-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6db1a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db1a-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6db1a-141">INPUTS</span></span>

### <span data-ttu-id="6db1a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6db1a-142">System.String</span></span>

### <span data-ttu-id="6db1a-143">Microsoft.Azure.Commands.Batch. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="6db1a-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="6db1a-144">Parametri: attività (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6db1a-144">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="6db1a-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6db1a-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="6db1a-146">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6db1a-146">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="6db1a-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6db1a-147">OUTPUTS</span></span>

### <span data-ttu-id="6db1a-148">System. void</span><span class="sxs-lookup"><span data-stu-id="6db1a-148">System.Void</span></span>

## <span data-ttu-id="6db1a-149">Note</span><span class="sxs-lookup"><span data-stu-id="6db1a-149">NOTES</span></span>

## <span data-ttu-id="6db1a-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6db1a-150">RELATED LINKS</span></span>

[<span data-ttu-id="6db1a-151">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6db1a-151">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6db1a-152">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6db1a-152">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="6db1a-153">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6db1a-153">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="6db1a-154">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6db1a-154">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="6db1a-155">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6db1a-155">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="6db1a-156">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6db1a-156">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


