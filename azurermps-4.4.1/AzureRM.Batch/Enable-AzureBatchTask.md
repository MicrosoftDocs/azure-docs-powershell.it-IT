---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 8e7636d83b953997ac1f9269e45fbf3c2278612f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688365"
---
# <span data-ttu-id="2016f-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2016f-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="2016f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2016f-102">SYNOPSIS</span></span>
<span data-ttu-id="2016f-103">Riattiva un'attività.</span><span class="sxs-lookup"><span data-stu-id="2016f-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2016f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2016f-104">SYNTAX</span></span>

### <span data-ttu-id="2016f-105">ID</span><span class="sxs-lookup"><span data-stu-id="2016f-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2016f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2016f-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2016f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2016f-107">DESCRIPTION</span></span>
<span data-ttu-id="2016f-108">Il cmdlet **Enable-AzureBatchTask** riattiva un'attività.</span><span class="sxs-lookup"><span data-stu-id="2016f-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="2016f-109">Se un'attività ha esaurito il numero di tentativi, questo cmdlet consente comunque l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2016f-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="2016f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2016f-110">EXAMPLES</span></span>

### <span data-ttu-id="2016f-111">Esempio 1: riattivare un'attività</span><span class="sxs-lookup"><span data-stu-id="2016f-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="2016f-112">Questo comando riattiva l'attività Task2 in Job Job7.</span><span class="sxs-lookup"><span data-stu-id="2016f-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="2016f-113">Esempio 2: riattivare un'attività usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="2016f-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="2016f-114">Questo comando consente di ottenere l'attività batch con ID Task3 nel processo che contiene l'ID Job8 usando il cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="2016f-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="2016f-115">Il comando passa l'attività al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="2016f-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2016f-116">Il comando riattiva l'attività.</span><span class="sxs-lookup"><span data-stu-id="2016f-116">The command reactivates that task.</span></span>

## <span data-ttu-id="2016f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2016f-117">PARAMETERS</span></span>

### <span data-ttu-id="2016f-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2016f-118">-BatchContext</span></span>
<span data-ttu-id="2016f-119">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="2016f-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2016f-120">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="2016f-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="2016f-121">-ID</span><span class="sxs-lookup"><span data-stu-id="2016f-121">-Id</span></span>
<span data-ttu-id="2016f-122">Specifica l'ID dell'attività da riattivare.</span><span class="sxs-lookup"><span data-stu-id="2016f-122">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="2016f-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="2016f-123">-JobId</span></span>
<span data-ttu-id="2016f-124">Specifica l'ID del processo che contiene l'attività.</span><span class="sxs-lookup"><span data-stu-id="2016f-124">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="2016f-125">-Attività</span><span class="sxs-lookup"><span data-stu-id="2016f-125">-Task</span></span>
<span data-ttu-id="2016f-126">Specifica l'attività riattivata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2016f-126">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="2016f-127">Per ottenere un oggetto **PSCloudTask** , usa il cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="2016f-127">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="2016f-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2016f-128">-Confirm</span></span>
<span data-ttu-id="2016f-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2016f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2016f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2016f-130">-WhatIf</span></span>
<span data-ttu-id="2016f-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2016f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2016f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2016f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2016f-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2016f-133">-DefaultProfile</span></span>
<span data-ttu-id="2016f-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2016f-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2016f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2016f-135">CommonParameters</span></span>
<span data-ttu-id="2016f-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2016f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2016f-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2016f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2016f-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2016f-138">INPUTS</span></span>

### <span data-ttu-id="2016f-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2016f-139">BatchAccountContext</span></span>
<span data-ttu-id="2016f-140">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="2016f-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="2016f-141">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="2016f-141">PSCloudTask</span></span>
<span data-ttu-id="2016f-142">Il parametro ' Task ' accetta il valore di tipo ' PSCloudTask ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="2016f-142">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="2016f-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2016f-143">OUTPUTS</span></span>

## <span data-ttu-id="2016f-144">Note</span><span class="sxs-lookup"><span data-stu-id="2016f-144">NOTES</span></span>

## <span data-ttu-id="2016f-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2016f-145">RELATED LINKS</span></span>

[<span data-ttu-id="2016f-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2016f-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="2016f-147">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2016f-147">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="2016f-148">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2016f-148">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="2016f-149">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2016f-149">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="2016f-150">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2016f-150">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="2016f-151">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2016f-151">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


