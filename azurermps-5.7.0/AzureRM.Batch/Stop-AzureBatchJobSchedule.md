---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 719c743281102f83c08f55093d221856be4194bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685636"
---
# <span data-ttu-id="579c1-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="579c1-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="579c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="579c1-102">SYNOPSIS</span></span>
<span data-ttu-id="579c1-103">Interrompe la pianificazione di un processo batch.</span><span class="sxs-lookup"><span data-stu-id="579c1-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="579c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="579c1-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="579c1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="579c1-105">DESCRIPTION</span></span>
<span data-ttu-id="579c1-106">Il cmdlet **Stop-AzureBatchJobSchedule** interrompe la pianificazione di un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="579c1-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="579c1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="579c1-107">EXAMPLES</span></span>

### <span data-ttu-id="579c1-108">Esempio 1: interrompere la pianificazione di un processo</span><span class="sxs-lookup"><span data-stu-id="579c1-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="579c1-109">Questo comando interrompe la pianificazione del processo che contiene l'ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="579c1-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="579c1-110">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="579c1-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="579c1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="579c1-111">PARAMETERS</span></span>

### <span data-ttu-id="579c1-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="579c1-112">-BatchContext</span></span>
<span data-ttu-id="579c1-113">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="579c1-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="579c1-114">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="579c1-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="579c1-115">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="579c1-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="579c1-116">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="579c1-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="579c1-117">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="579c1-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="579c1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="579c1-118">-DefaultProfile</span></span>
<span data-ttu-id="579c1-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="579c1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="579c1-120">-ID</span><span class="sxs-lookup"><span data-stu-id="579c1-120">-Id</span></span>
<span data-ttu-id="579c1-121">Specifica l'ID della pianificazione del processo arrestata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="579c1-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="579c1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="579c1-122">CommonParameters</span></span>
<span data-ttu-id="579c1-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="579c1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="579c1-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="579c1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="579c1-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="579c1-125">INPUTS</span></span>

### <span data-ttu-id="579c1-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="579c1-126">BatchAccountContext</span></span>
<span data-ttu-id="579c1-127">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="579c1-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="579c1-128">Stringa</span><span class="sxs-lookup"><span data-stu-id="579c1-128">String</span></span>
<span data-ttu-id="579c1-129">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="579c1-129">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="579c1-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="579c1-130">OUTPUTS</span></span>

## <span data-ttu-id="579c1-131">Note</span><span class="sxs-lookup"><span data-stu-id="579c1-131">NOTES</span></span>

## <span data-ttu-id="579c1-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="579c1-132">RELATED LINKS</span></span>

[<span data-ttu-id="579c1-133">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="579c1-133">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="579c1-134">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="579c1-134">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="579c1-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="579c1-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="579c1-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="579c1-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="579c1-137">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="579c1-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="579c1-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="579c1-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="579c1-139">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="579c1-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


