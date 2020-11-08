---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: 06fc7496a4e25dce8638b887a7f04afdda705261
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "94030652"
---
# <span data-ttu-id="7bb13-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7bb13-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="7bb13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7bb13-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb13-103">Disabilita la pianificazione di un processo batch.</span><span class="sxs-lookup"><span data-stu-id="7bb13-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="7bb13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7bb13-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bb13-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bb13-105">DESCRIPTION</span></span>
<span data-ttu-id="7bb13-106">Il cmdlet **Disable-AzBatchJobSchedule Disabilita** una pianificazione dei processi batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="7bb13-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="7bb13-107">Se si disattiva una programmazione, i processi non vengono creati in base a tale programmazione.</span><span class="sxs-lookup"><span data-stu-id="7bb13-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="7bb13-108">È possibile abilitare una pianificazione disabilitata in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="7bb13-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="7bb13-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7bb13-109">EXAMPLES</span></span>

### <span data-ttu-id="7bb13-110">Esempio 1: disabilitare una pianificazione del processo</span><span class="sxs-lookup"><span data-stu-id="7bb13-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="7bb13-111">Questo comando Disabilita la pianificazione del processo con ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="7bb13-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="7bb13-112">Usa il cmdlet **Get-AzBatchAccountKey** per assegnare un contesto alla variabile $context.</span><span class="sxs-lookup"><span data-stu-id="7bb13-112">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="7bb13-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7bb13-113">PARAMETERS</span></span>

### <span data-ttu-id="7bb13-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7bb13-114">-BatchContext</span></span>
<span data-ttu-id="7bb13-115">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="7bb13-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7bb13-116">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="7bb13-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7bb13-117">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="7bb13-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7bb13-118">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7bb13-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7bb13-119">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7bb13-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7bb13-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb13-120">-DefaultProfile</span></span>
<span data-ttu-id="7bb13-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7bb13-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bb13-122">-ID</span><span class="sxs-lookup"><span data-stu-id="7bb13-122">-Id</span></span>
<span data-ttu-id="7bb13-123">Specifica l'ID della pianificazione del processo disabilitata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bb13-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="7bb13-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb13-124">CommonParameters</span></span>
<span data-ttu-id="7bb13-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bb13-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb13-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bb13-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb13-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7bb13-127">INPUTS</span></span>

### <span data-ttu-id="7bb13-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7bb13-128">System.String</span></span>

### <span data-ttu-id="7bb13-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7bb13-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7bb13-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7bb13-130">OUTPUTS</span></span>

### <span data-ttu-id="7bb13-131">System. void</span><span class="sxs-lookup"><span data-stu-id="7bb13-131">System.Void</span></span>

## <span data-ttu-id="7bb13-132">Note</span><span class="sxs-lookup"><span data-stu-id="7bb13-132">NOTES</span></span>

## <span data-ttu-id="7bb13-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7bb13-133">RELATED LINKS</span></span>

[<span data-ttu-id="7bb13-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7bb13-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="7bb13-135">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7bb13-135">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7bb13-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7bb13-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="7bb13-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7bb13-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="7bb13-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7bb13-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="7bb13-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7bb13-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="7bb13-140">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="7bb13-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


