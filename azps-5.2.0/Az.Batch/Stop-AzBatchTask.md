---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 8b84028bc9da854b5aa749867a8759b71d9f7b63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358357"
---
# <span data-ttu-id="0ffaf-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0ffaf-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="0ffaf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ffaf-102">SYNOPSIS</span></span>
<span data-ttu-id="0ffaf-103">Interrompe un'attività batch.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-103">Stops a Batch task.</span></span>

## <span data-ttu-id="0ffaf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ffaf-104">SYNTAX</span></span>

### <span data-ttu-id="0ffaf-105">ID</span><span class="sxs-lookup"><span data-stu-id="0ffaf-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ffaf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0ffaf-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ffaf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ffaf-107">DESCRIPTION</span></span>
<span data-ttu-id="0ffaf-108">Il cmdlet **Stop-AzBatchTask** interrompe un'attività batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="0ffaf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ffaf-109">EXAMPLES</span></span>

### <span data-ttu-id="0ffaf-110">Esempio 1: eliminare un'attività batch in base all'ID</span><span class="sxs-lookup"><span data-stu-id="0ffaf-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="0ffaf-111">Questo comando Arresta un'attività con ID Task23 sotto il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="0ffaf-112">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="0ffaf-113">Usa il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="0ffaf-114">Esempio 2: arrestare un'attività batch usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="0ffaf-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="0ffaf-115">Questo comando ottiene l'attività batch che contiene l'ID Task26 nel processo con l'ID Job-000001 usando il cmdlet Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="0ffaf-116">Il comando passa l'attività al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0ffaf-117">Il comando interrompe l'attività.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-117">The command stops that task.</span></span>

## <span data-ttu-id="0ffaf-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ffaf-118">PARAMETERS</span></span>

### <span data-ttu-id="0ffaf-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0ffaf-119">-BatchContext</span></span>
<span data-ttu-id="0ffaf-120">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0ffaf-121">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0ffaf-122">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0ffaf-123">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0ffaf-124">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0ffaf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ffaf-125">-DefaultProfile</span></span>
<span data-ttu-id="0ffaf-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ffaf-127">-ID</span><span class="sxs-lookup"><span data-stu-id="0ffaf-127">-Id</span></span>
<span data-ttu-id="0ffaf-128">Specifica l'ID dell'attività arrestata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-128">Specifies the ID of the task that this cmdlet stops.</span></span>

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

### <span data-ttu-id="0ffaf-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="0ffaf-129">-JobId</span></span>
<span data-ttu-id="0ffaf-130">Specifica l'ID del processo che contiene l'attività.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-130">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="0ffaf-131">-Attività</span><span class="sxs-lookup"><span data-stu-id="0ffaf-131">-Task</span></span>
<span data-ttu-id="0ffaf-132">Specifica l'attività arrestata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="0ffaf-133">Per ottenere un oggetto **PSCloudTask** , usa il cmdlet Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="0ffaf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ffaf-134">CommonParameters</span></span>
<span data-ttu-id="0ffaf-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ffaf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ffaf-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ffaf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ffaf-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ffaf-137">INPUTS</span></span>

### <span data-ttu-id="0ffaf-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0ffaf-138">System.String</span></span>

### <span data-ttu-id="0ffaf-139">Microsoft.Azure.Commands.Batch. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="0ffaf-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="0ffaf-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0ffaf-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0ffaf-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ffaf-141">OUTPUTS</span></span>

### <span data-ttu-id="0ffaf-142">System. void</span><span class="sxs-lookup"><span data-stu-id="0ffaf-142">System.Void</span></span>

## <span data-ttu-id="0ffaf-143">Note</span><span class="sxs-lookup"><span data-stu-id="0ffaf-143">NOTES</span></span>

## <span data-ttu-id="0ffaf-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ffaf-144">RELATED LINKS</span></span>

[<span data-ttu-id="0ffaf-145">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0ffaf-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="0ffaf-146">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0ffaf-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="0ffaf-147">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0ffaf-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="0ffaf-148">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="0ffaf-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
