---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: 3081721db5cb113d48417ddf28d8a96512d27f99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520475"
---
# <span data-ttu-id="30bfa-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="30bfa-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="30bfa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="30bfa-103">Abilita una pianificazione processo batch.</span><span class="sxs-lookup"><span data-stu-id="30bfa-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30bfa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30bfa-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30bfa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30bfa-105">DESCRIPTION</span></span>
<span data-ttu-id="30bfa-106">Il cmdlet **Enable-AzureBatchJobSchedule** Abilita una pianificazione del processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="30bfa-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="30bfa-107">Dopo l'abilitazione di una pianificazione processo, i processi possono essere creati in base a tale programmazione.</span><span class="sxs-lookup"><span data-stu-id="30bfa-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="30bfa-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30bfa-108">EXAMPLES</span></span>

### <span data-ttu-id="30bfa-109">Esempio 1: abilitare una pianificazione del processo</span><span class="sxs-lookup"><span data-stu-id="30bfa-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="30bfa-110">Questo comando Abilita la pianificazione del processo con ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="30bfa-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="30bfa-111">Usa il cmdlet **Get-AzureRmBatchAccountKeys** per assegnare un contesto alla variabile $context.</span><span class="sxs-lookup"><span data-stu-id="30bfa-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="30bfa-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30bfa-112">PARAMETERS</span></span>

### <span data-ttu-id="30bfa-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="30bfa-113">-BatchContext</span></span>
<span data-ttu-id="30bfa-114">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="30bfa-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="30bfa-115">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="30bfa-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="30bfa-116">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="30bfa-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="30bfa-117">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="30bfa-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="30bfa-118">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="30bfa-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30bfa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30bfa-119">-DefaultProfile</span></span>
<span data-ttu-id="30bfa-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30bfa-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bfa-121">-ID</span><span class="sxs-lookup"><span data-stu-id="30bfa-121">-Id</span></span>
<span data-ttu-id="30bfa-122">Specifica l'ID della pianificazione del processo abilitata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30bfa-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30bfa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30bfa-123">CommonParameters</span></span>
<span data-ttu-id="30bfa-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30bfa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30bfa-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30bfa-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30bfa-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30bfa-126">INPUTS</span></span>

### <span data-ttu-id="30bfa-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="30bfa-127">BatchAccountContext</span></span>
<span data-ttu-id="30bfa-128">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="30bfa-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="30bfa-129">Stringa</span><span class="sxs-lookup"><span data-stu-id="30bfa-129">String</span></span>
<span data-ttu-id="30bfa-130">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="30bfa-130">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="30bfa-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30bfa-131">OUTPUTS</span></span>

## <span data-ttu-id="30bfa-132">Note</span><span class="sxs-lookup"><span data-stu-id="30bfa-132">NOTES</span></span>

## <span data-ttu-id="30bfa-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30bfa-133">RELATED LINKS</span></span>

[<span data-ttu-id="30bfa-134">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="30bfa-134">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="30bfa-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="30bfa-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="30bfa-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="30bfa-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="30bfa-137">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="30bfa-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="30bfa-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="30bfa-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="30bfa-139">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="30bfa-139">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="30bfa-140">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="30bfa-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


