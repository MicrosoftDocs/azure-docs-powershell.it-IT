---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: e84bf86a3a784e47088ff1ed71047faac99239f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517596"
---
# <span data-ttu-id="a0796-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a0796-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="a0796-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0796-102">SYNOPSIS</span></span>
<span data-ttu-id="a0796-103">Abilita una pianificazione processo batch.</span><span class="sxs-lookup"><span data-stu-id="a0796-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0796-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0796-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0796-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0796-105">DESCRIPTION</span></span>
<span data-ttu-id="a0796-106">Il cmdlet **Enable-AzureBatchJobSchedule** Abilita una pianificazione del processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="a0796-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="a0796-107">Dopo l'abilitazione di una pianificazione processo, i processi possono essere creati in base a tale programmazione.</span><span class="sxs-lookup"><span data-stu-id="a0796-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="a0796-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0796-108">EXAMPLES</span></span>

### <span data-ttu-id="a0796-109">Esempio 1: abilitare una pianificazione del processo</span><span class="sxs-lookup"><span data-stu-id="a0796-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="a0796-110">Questo comando Abilita la pianificazione del processo con ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="a0796-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="a0796-111">Usa il cmdlet **Get-AzureRmBatchAccountKeys** per assegnare un contesto alla variabile $context.</span><span class="sxs-lookup"><span data-stu-id="a0796-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a0796-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0796-112">PARAMETERS</span></span>

### <span data-ttu-id="a0796-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a0796-113">-BatchContext</span></span>
<span data-ttu-id="a0796-114">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a0796-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a0796-115">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a0796-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a0796-116">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="a0796-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a0796-117">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a0796-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a0796-118">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a0796-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a0796-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0796-119">-DefaultProfile</span></span>
<span data-ttu-id="a0796-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0796-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0796-121">-ID</span><span class="sxs-lookup"><span data-stu-id="a0796-121">-Id</span></span>
<span data-ttu-id="a0796-122">Specifica l'ID della pianificazione del processo abilitata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0796-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="a0796-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0796-123">CommonParameters</span></span>
<span data-ttu-id="a0796-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0796-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0796-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0796-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0796-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0796-126">INPUTS</span></span>

### <span data-ttu-id="a0796-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a0796-127">System.String</span></span>

### <span data-ttu-id="a0796-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a0796-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="a0796-129">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a0796-129">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="a0796-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0796-130">OUTPUTS</span></span>

### <span data-ttu-id="a0796-131">System. void</span><span class="sxs-lookup"><span data-stu-id="a0796-131">System.Void</span></span>

## <span data-ttu-id="a0796-132">Note</span><span class="sxs-lookup"><span data-stu-id="a0796-132">NOTES</span></span>

## <span data-ttu-id="a0796-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0796-133">RELATED LINKS</span></span>

[<span data-ttu-id="a0796-134">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a0796-134">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="a0796-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a0796-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a0796-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a0796-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="a0796-137">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a0796-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="a0796-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a0796-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="a0796-139">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a0796-139">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="a0796-140">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="a0796-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


