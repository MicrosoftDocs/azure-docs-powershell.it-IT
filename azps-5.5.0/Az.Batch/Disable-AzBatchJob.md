---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: a25c31c0b73a42e0d64b567b6bc2529bf4ebf258
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205410"
---
# <span data-ttu-id="03d65-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="03d65-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="03d65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03d65-102">SYNOPSIS</span></span>
<span data-ttu-id="03d65-103">Disabilita un processo batch.</span><span class="sxs-lookup"><span data-stu-id="03d65-103">Disables a Batch job.</span></span>

## <span data-ttu-id="03d65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03d65-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03d65-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="03d65-105">DESCRIPTION</span></span>
<span data-ttu-id="03d65-106">Il cmdlet **Disable-AzBatchJob** disabilita un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="03d65-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="03d65-107">Dopo aver abilitato un processo, è possibile eseguire nuove attività.</span><span class="sxs-lookup"><span data-stu-id="03d65-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="03d65-108">I processi disabilitati non eseguono nuove attività.</span><span class="sxs-lookup"><span data-stu-id="03d65-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="03d65-109">È possibile abilitare un processo disabilitato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="03d65-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="03d65-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03d65-110">EXAMPLES</span></span>

### <span data-ttu-id="03d65-111">Esempio 1: Disabilitare un processo batch</span><span class="sxs-lookup"><span data-stu-id="03d65-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="03d65-112">Questo comando disabilita il processo con ID Processo-000001.</span><span class="sxs-lookup"><span data-stu-id="03d65-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="03d65-113">Il comando termina le attività attive per il processo.</span><span class="sxs-lookup"><span data-stu-id="03d65-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="03d65-114">Usare il cmdlet **Get-AzBatchAccountKey** per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="03d65-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="03d65-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03d65-115">PARAMETERS</span></span>

### <span data-ttu-id="03d65-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="03d65-116">-BatchContext</span></span>
<span data-ttu-id="03d65-117">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="03d65-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="03d65-118">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="03d65-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="03d65-119">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="03d65-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="03d65-120">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="03d65-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="03d65-121">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="03d65-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="03d65-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03d65-122">-DefaultProfile</span></span>
<span data-ttu-id="03d65-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03d65-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03d65-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="03d65-124">-DisableJobOption</span></span>
<span data-ttu-id="03d65-125">Specifica cosa fare con le attività attive associate al processo che questo cmdlet disabilita.</span><span class="sxs-lookup"><span data-stu-id="03d65-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="03d65-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="03d65-126">Valid values are:</span></span>
- <span data-ttu-id="03d65-127">Rita in coda</span><span class="sxs-lookup"><span data-stu-id="03d65-127">Requeue</span></span>
- <span data-ttu-id="03d65-128">Termina</span><span class="sxs-lookup"><span data-stu-id="03d65-128">Terminate</span></span>
- <span data-ttu-id="03d65-129">Attendi</span><span class="sxs-lookup"><span data-stu-id="03d65-129">Wait</span></span>

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

### <span data-ttu-id="03d65-130">-Id</span><span class="sxs-lookup"><span data-stu-id="03d65-130">-Id</span></span>
<span data-ttu-id="03d65-131">Specifica l'ID del processo disabilitato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03d65-131">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="03d65-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03d65-132">CommonParameters</span></span>
<span data-ttu-id="03d65-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03d65-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03d65-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="03d65-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03d65-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="03d65-135">INPUTS</span></span>

### <span data-ttu-id="03d65-136">System.String</span><span class="sxs-lookup"><span data-stu-id="03d65-136">System.String</span></span>

### <span data-ttu-id="03d65-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="03d65-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="03d65-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03d65-138">OUTPUTS</span></span>

### <span data-ttu-id="03d65-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="03d65-139">System.Void</span></span>

## <span data-ttu-id="03d65-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="03d65-140">NOTES</span></span>

## <span data-ttu-id="03d65-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03d65-141">RELATED LINKS</span></span>

[<span data-ttu-id="03d65-142">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="03d65-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="03d65-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="03d65-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="03d65-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="03d65-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="03d65-145">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="03d65-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="03d65-146">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="03d65-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="03d65-147">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="03d65-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="03d65-148">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="03d65-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
