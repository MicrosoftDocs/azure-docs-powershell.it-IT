---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: a25c31c0b73a42e0d64b567b6bc2529bf4ebf258
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478420"
---
# <span data-ttu-id="327c1-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="327c1-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="327c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="327c1-102">SYNOPSIS</span></span>
<span data-ttu-id="327c1-103">Disabilita un processo batch.</span><span class="sxs-lookup"><span data-stu-id="327c1-103">Disables a Batch job.</span></span>

## <span data-ttu-id="327c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="327c1-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="327c1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="327c1-105">DESCRIPTION</span></span>
<span data-ttu-id="327c1-106">Il cmdlet **Disable-AzBatchJob Disabilita** un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="327c1-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="327c1-107">Dopo l'abilitazione di un processo, le nuove attività possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="327c1-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="327c1-108">I processi disabilitati non eseguono nuove attività.</span><span class="sxs-lookup"><span data-stu-id="327c1-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="327c1-109">È possibile abilitare un processo disabilitato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="327c1-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="327c1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="327c1-110">EXAMPLES</span></span>

### <span data-ttu-id="327c1-111">Esempio 1: disabilitare un processo batch</span><span class="sxs-lookup"><span data-stu-id="327c1-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="327c1-112">Questo comando Disabilita il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="327c1-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="327c1-113">Il comando termina le attività attive per il processo.</span><span class="sxs-lookup"><span data-stu-id="327c1-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="327c1-114">Usa il cmdlet **Get-AzBatchAccountKey** per assegnare un contesto alla variabile $context.</span><span class="sxs-lookup"><span data-stu-id="327c1-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="327c1-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="327c1-115">PARAMETERS</span></span>

### <span data-ttu-id="327c1-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="327c1-116">-BatchContext</span></span>
<span data-ttu-id="327c1-117">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="327c1-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="327c1-118">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="327c1-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="327c1-119">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="327c1-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="327c1-120">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="327c1-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="327c1-121">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="327c1-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="327c1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="327c1-122">-DefaultProfile</span></span>
<span data-ttu-id="327c1-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="327c1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="327c1-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="327c1-124">-DisableJobOption</span></span>
<span data-ttu-id="327c1-125">Specifica le operazioni da eseguire con le attività attive associate al processo disabilitato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="327c1-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="327c1-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="327c1-126">Valid values are:</span></span>
- <span data-ttu-id="327c1-127">Riaccodare</span><span class="sxs-lookup"><span data-stu-id="327c1-127">Requeue</span></span>
- <span data-ttu-id="327c1-128">Terminare</span><span class="sxs-lookup"><span data-stu-id="327c1-128">Terminate</span></span>
- <span data-ttu-id="327c1-129">Attendere</span><span class="sxs-lookup"><span data-stu-id="327c1-129">Wait</span></span>

```yaml
Type: Microsoft.Azure.Batch.Common.DisableJobOption
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="327c1-130">-ID</span><span class="sxs-lookup"><span data-stu-id="327c1-130">-Id</span></span>
<span data-ttu-id="327c1-131">Specifica l'ID del processo disabilitato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="327c1-131">Specifies the ID of the job that this cmdlet disables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="327c1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="327c1-132">CommonParameters</span></span>
<span data-ttu-id="327c1-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="327c1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="327c1-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="327c1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="327c1-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="327c1-135">INPUTS</span></span>

### <span data-ttu-id="327c1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="327c1-136">System.String</span></span>

### <span data-ttu-id="327c1-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="327c1-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="327c1-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="327c1-138">OUTPUTS</span></span>

### <span data-ttu-id="327c1-139">System. void</span><span class="sxs-lookup"><span data-stu-id="327c1-139">System.Void</span></span>

## <span data-ttu-id="327c1-140">Note</span><span class="sxs-lookup"><span data-stu-id="327c1-140">NOTES</span></span>

## <span data-ttu-id="327c1-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="327c1-141">RELATED LINKS</span></span>

[<span data-ttu-id="327c1-142">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="327c1-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="327c1-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="327c1-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="327c1-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="327c1-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="327c1-145">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="327c1-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="327c1-146">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="327c1-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="327c1-147">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="327c1-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="327c1-148">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="327c1-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
