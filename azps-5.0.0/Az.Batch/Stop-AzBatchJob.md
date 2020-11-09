---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: ffaac0bdd4a144cc3979da052c0c40cb824862f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302137"
---
# <span data-ttu-id="d3f70-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d3f70-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="d3f70-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3f70-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f70-103">Interrompe un processo batch.</span><span class="sxs-lookup"><span data-stu-id="d3f70-103">Stops a Batch job.</span></span>

## <span data-ttu-id="d3f70-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3f70-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3f70-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3f70-105">DESCRIPTION</span></span>
<span data-ttu-id="d3f70-106">Il cmdlet **Stop-AzBatchJob** interrompe un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3f70-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="d3f70-107">Questo comando contrassegna il processo come completato.</span><span class="sxs-lookup"><span data-stu-id="d3f70-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="d3f70-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3f70-108">EXAMPLES</span></span>

### <span data-ttu-id="d3f70-109">Esempio 1: interrompere un processo batch</span><span class="sxs-lookup"><span data-stu-id="d3f70-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="d3f70-110">Questo comando Arresta il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="d3f70-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="d3f70-111">Il comando specifica un motivo per cui si è scelto di interrompere il processo.</span><span class="sxs-lookup"><span data-stu-id="d3f70-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="d3f70-112">Usa il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="d3f70-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="d3f70-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3f70-113">PARAMETERS</span></span>

### <span data-ttu-id="d3f70-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d3f70-114">-BatchContext</span></span>
<span data-ttu-id="d3f70-115">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="d3f70-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d3f70-116">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="d3f70-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d3f70-117">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="d3f70-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d3f70-118">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d3f70-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d3f70-119">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d3f70-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d3f70-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f70-120">-DefaultProfile</span></span>
<span data-ttu-id="d3f70-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3f70-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3f70-122">-ID</span><span class="sxs-lookup"><span data-stu-id="d3f70-122">-Id</span></span>
<span data-ttu-id="d3f70-123">Specifica l'ID del processo interrotto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3f70-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d3f70-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="d3f70-124">-TerminateReason</span></span>
<span data-ttu-id="d3f70-125">Specifica il motivo per cui hai deciso di interrompere il processo.</span><span class="sxs-lookup"><span data-stu-id="d3f70-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="d3f70-126">Questo cmdlet archivia il testo come proprietà **TerminateReason** del processo.</span><span class="sxs-lookup"><span data-stu-id="d3f70-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f70-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f70-127">CommonParameters</span></span>
<span data-ttu-id="d3f70-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f70-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f70-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3f70-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f70-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3f70-130">INPUTS</span></span>

### <span data-ttu-id="d3f70-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d3f70-131">System.String</span></span>

### <span data-ttu-id="d3f70-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d3f70-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d3f70-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3f70-133">OUTPUTS</span></span>

### <span data-ttu-id="d3f70-134">System. void</span><span class="sxs-lookup"><span data-stu-id="d3f70-134">System.Void</span></span>

## <span data-ttu-id="d3f70-135">Note</span><span class="sxs-lookup"><span data-stu-id="d3f70-135">NOTES</span></span>

## <span data-ttu-id="d3f70-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3f70-136">RELATED LINKS</span></span>

[<span data-ttu-id="d3f70-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d3f70-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="d3f70-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d3f70-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="d3f70-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d3f70-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d3f70-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d3f70-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="d3f70-141">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d3f70-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="d3f70-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d3f70-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="d3f70-143">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="d3f70-143">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
