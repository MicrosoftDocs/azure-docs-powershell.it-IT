---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: 791562b4cfa7f2ee5cb446e70cad59074389c25c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93685285"
---
# <span data-ttu-id="4f2b9-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4f2b9-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="4f2b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4f2b9-102">SYNOPSIS</span></span>
<span data-ttu-id="4f2b9-103">Interrompe un processo batch.</span><span class="sxs-lookup"><span data-stu-id="4f2b9-103">Stops a Batch job.</span></span>

## <span data-ttu-id="4f2b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f2b9-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f2b9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f2b9-105">DESCRIPTION</span></span>
<span data-ttu-id="4f2b9-106">Il cmdlet **Stop-AzBatchJob** interrompe un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="4f2b9-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="4f2b9-107">Questo comando contrassegna il processo come completato.</span><span class="sxs-lookup"><span data-stu-id="4f2b9-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="4f2b9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f2b9-108">EXAMPLES</span></span>

### <span data-ttu-id="4f2b9-109">Esempio 1: interrompere un processo batch</span><span class="sxs-lookup"><span data-stu-id="4f2b9-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="4f2b9-110">Questo comando Arresta il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="4f2b9-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="4f2b9-111">Il comando specifica un motivo per cui si è scelto di interrompere il processo.</span><span class="sxs-lookup"><span data-stu-id="4f2b9-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="4f2b9-112">Usa il cmdlet Get-AzBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="4f2b9-112">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="4f2b9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4f2b9-113">PARAMETERS</span></span>

### <span data-ttu-id="4f2b9-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4f2b9-114">-BatchContext</span></span>
<span data-ttu-id="4f2b9-115">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4f2b9-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4f2b9-116">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4f2b9-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4f2b9-117">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="4f2b9-117">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4f2b9-118">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4f2b9-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4f2b9-119">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4f2b9-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4f2b9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f2b9-120">-DefaultProfile</span></span>
<span data-ttu-id="4f2b9-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f2b9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f2b9-122">-ID</span><span class="sxs-lookup"><span data-stu-id="4f2b9-122">-Id</span></span>
<span data-ttu-id="4f2b9-123">Specifica l'ID del processo interrotto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f2b9-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="4f2b9-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="4f2b9-124">-TerminateReason</span></span>
<span data-ttu-id="4f2b9-125">Specifica il motivo per cui hai deciso di interrompere il processo.</span><span class="sxs-lookup"><span data-stu-id="4f2b9-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="4f2b9-126">Questo cmdlet archivia il testo come proprietà **TerminateReason** del processo.</span><span class="sxs-lookup"><span data-stu-id="4f2b9-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="4f2b9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f2b9-127">CommonParameters</span></span>
<span data-ttu-id="4f2b9-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f2b9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f2b9-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f2b9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f2b9-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4f2b9-130">INPUTS</span></span>

### <span data-ttu-id="4f2b9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4f2b9-131">System.String</span></span>

### <span data-ttu-id="4f2b9-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4f2b9-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4f2b9-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f2b9-133">OUTPUTS</span></span>

### <span data-ttu-id="4f2b9-134">System. void</span><span class="sxs-lookup"><span data-stu-id="4f2b9-134">System.Void</span></span>

## <span data-ttu-id="4f2b9-135">Note</span><span class="sxs-lookup"><span data-stu-id="4f2b9-135">NOTES</span></span>

## <span data-ttu-id="4f2b9-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f2b9-136">RELATED LINKS</span></span>

[<span data-ttu-id="4f2b9-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4f2b9-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="4f2b9-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4f2b9-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="4f2b9-139">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="4f2b9-139">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4f2b9-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4f2b9-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="4f2b9-141">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4f2b9-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="4f2b9-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4f2b9-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="4f2b9-143">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="4f2b9-143">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


