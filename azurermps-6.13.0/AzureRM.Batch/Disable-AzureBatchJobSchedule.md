---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: e1eb586ff23f5f56cd9fc117f5039d3ccc841367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517619"
---
# <span data-ttu-id="f8875-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f8875-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="f8875-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8875-102">SYNOPSIS</span></span>
<span data-ttu-id="f8875-103">Disabilita la pianificazione di un processo batch.</span><span class="sxs-lookup"><span data-stu-id="f8875-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8875-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8875-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8875-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8875-105">DESCRIPTION</span></span>
<span data-ttu-id="f8875-106">Il cmdlet **Disable-AzureBatchJobSchedule Disabilita** una pianificazione dei processi batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="f8875-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="f8875-107">Se si disattiva una programmazione, i processi non vengono creati in base a tale programmazione.</span><span class="sxs-lookup"><span data-stu-id="f8875-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="f8875-108">È possibile abilitare una pianificazione disabilitata in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="f8875-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="f8875-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8875-109">EXAMPLES</span></span>

### <span data-ttu-id="f8875-110">Esempio 1: disabilitare una pianificazione del processo</span><span class="sxs-lookup"><span data-stu-id="f8875-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="f8875-111">Questo comando Disabilita la pianificazione del processo con ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="f8875-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="f8875-112">Usa il cmdlet **Get-AzureRmBatchAccountKeys** per assegnare un contesto alla variabile $context.</span><span class="sxs-lookup"><span data-stu-id="f8875-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="f8875-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8875-113">PARAMETERS</span></span>

### <span data-ttu-id="f8875-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f8875-114">-BatchContext</span></span>
<span data-ttu-id="f8875-115">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f8875-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f8875-116">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f8875-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f8875-117">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="f8875-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f8875-118">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f8875-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f8875-119">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f8875-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f8875-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8875-120">-DefaultProfile</span></span>
<span data-ttu-id="f8875-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8875-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8875-122">-ID</span><span class="sxs-lookup"><span data-stu-id="f8875-122">-Id</span></span>
<span data-ttu-id="f8875-123">Specifica l'ID della pianificazione del processo disabilitata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8875-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="f8875-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8875-124">CommonParameters</span></span>
<span data-ttu-id="f8875-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8875-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8875-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8875-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8875-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8875-127">INPUTS</span></span>

### <span data-ttu-id="f8875-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f8875-128">System.String</span></span>

### <span data-ttu-id="f8875-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f8875-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="f8875-130">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f8875-130">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="f8875-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8875-131">OUTPUTS</span></span>

### <span data-ttu-id="f8875-132">System. void</span><span class="sxs-lookup"><span data-stu-id="f8875-132">System.Void</span></span>

## <span data-ttu-id="f8875-133">Note</span><span class="sxs-lookup"><span data-stu-id="f8875-133">NOTES</span></span>

## <span data-ttu-id="f8875-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8875-134">RELATED LINKS</span></span>

[<span data-ttu-id="f8875-135">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f8875-135">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="f8875-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f8875-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f8875-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f8875-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="f8875-138">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f8875-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="f8875-139">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f8875-139">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="f8875-140">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f8875-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="f8875-141">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="f8875-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


