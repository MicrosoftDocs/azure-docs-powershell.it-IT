---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: 18a96a72cc965f5e93a035ba6ed7b91ba5419edf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519295"
---
# <span data-ttu-id="b58c2-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b58c2-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="b58c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b58c2-102">SYNOPSIS</span></span>
<span data-ttu-id="b58c2-103">Interrompe un'attività batch.</span><span class="sxs-lookup"><span data-stu-id="b58c2-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b58c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b58c2-104">SYNTAX</span></span>

### <span data-ttu-id="b58c2-105">ID</span><span class="sxs-lookup"><span data-stu-id="b58c2-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b58c2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b58c2-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b58c2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b58c2-107">DESCRIPTION</span></span>
<span data-ttu-id="b58c2-108">Il cmdlet **Stop-AzureBatchTask** interrompe un'attività batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="b58c2-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="b58c2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b58c2-109">EXAMPLES</span></span>

### <span data-ttu-id="b58c2-110">Esempio 1: eliminare un'attività batch in base all'ID</span><span class="sxs-lookup"><span data-stu-id="b58c2-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="b58c2-111">Questo comando Arresta un'attività con ID Task23 sotto il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="b58c2-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="b58c2-112">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="b58c2-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="b58c2-113">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="b58c2-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b58c2-114">Esempio 2: arrestare un'attività batch usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="b58c2-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="b58c2-115">Questo comando ottiene l'attività batch che contiene l'ID Task26 nel processo con l'ID Job-000001 usando il cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="b58c2-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="b58c2-116">Il comando passa l'attività al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="b58c2-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b58c2-117">Il comando interrompe l'attività.</span><span class="sxs-lookup"><span data-stu-id="b58c2-117">The command stops that task.</span></span>

## <span data-ttu-id="b58c2-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b58c2-118">PARAMETERS</span></span>

### <span data-ttu-id="b58c2-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b58c2-119">-BatchContext</span></span>
<span data-ttu-id="b58c2-120">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b58c2-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b58c2-121">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b58c2-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b58c2-122">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="b58c2-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b58c2-123">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b58c2-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b58c2-124">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b58c2-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b58c2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b58c2-125">-DefaultProfile</span></span>
<span data-ttu-id="b58c2-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b58c2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b58c2-127">-ID</span><span class="sxs-lookup"><span data-stu-id="b58c2-127">-Id</span></span>
<span data-ttu-id="b58c2-128">Specifica l'ID dell'attività arrestata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b58c2-128">Specifies the ID of the task that this cmdlet stops.</span></span>

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

### <span data-ttu-id="b58c2-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="b58c2-129">-JobId</span></span>
<span data-ttu-id="b58c2-130">Specifica l'ID del processo che contiene l'attività.</span><span class="sxs-lookup"><span data-stu-id="b58c2-130">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="b58c2-131">-Attività</span><span class="sxs-lookup"><span data-stu-id="b58c2-131">-Task</span></span>
<span data-ttu-id="b58c2-132">Specifica l'attività arrestata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b58c2-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="b58c2-133">Per ottenere un oggetto **PSCloudTask** , usa il cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="b58c2-133">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="b58c2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b58c2-134">CommonParameters</span></span>
<span data-ttu-id="b58c2-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b58c2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b58c2-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b58c2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b58c2-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b58c2-137">INPUTS</span></span>

### <span data-ttu-id="b58c2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b58c2-138">System.String</span></span>

### <span data-ttu-id="b58c2-139">Microsoft.Azure.Commands.Batch. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="b58c2-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="b58c2-140">Parametri: attività (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b58c2-140">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="b58c2-141">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b58c2-141">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="b58c2-142">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b58c2-142">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="b58c2-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b58c2-143">OUTPUTS</span></span>

### <span data-ttu-id="b58c2-144">System. void</span><span class="sxs-lookup"><span data-stu-id="b58c2-144">System.Void</span></span>

## <span data-ttu-id="b58c2-145">Note</span><span class="sxs-lookup"><span data-stu-id="b58c2-145">NOTES</span></span>

## <span data-ttu-id="b58c2-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b58c2-146">RELATED LINKS</span></span>

[<span data-ttu-id="b58c2-147">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b58c2-147">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="b58c2-148">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b58c2-148">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="b58c2-149">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b58c2-149">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="b58c2-150">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="b58c2-150">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


