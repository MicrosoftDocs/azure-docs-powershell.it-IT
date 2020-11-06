---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 33ae727ea31d533652943240cd9cd25014635533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519298"
---
# <span data-ttu-id="4fb63-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4fb63-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="4fb63-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4fb63-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb63-103">Interrompe la pianificazione di un processo batch.</span><span class="sxs-lookup"><span data-stu-id="4fb63-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fb63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4fb63-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fb63-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fb63-105">DESCRIPTION</span></span>
<span data-ttu-id="4fb63-106">Il cmdlet **Stop-AzureBatchJobSchedule** interrompe la pianificazione di un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb63-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="4fb63-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4fb63-107">EXAMPLES</span></span>

### <span data-ttu-id="4fb63-108">Esempio 1: interrompere la pianificazione di un processo</span><span class="sxs-lookup"><span data-stu-id="4fb63-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="4fb63-109">Questo comando interrompe la pianificazione del processo che contiene l'ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="4fb63-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="4fb63-110">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="4fb63-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="4fb63-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4fb63-111">PARAMETERS</span></span>

### <span data-ttu-id="4fb63-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4fb63-112">-BatchContext</span></span>
<span data-ttu-id="4fb63-113">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4fb63-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4fb63-114">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4fb63-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4fb63-115">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="4fb63-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4fb63-116">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4fb63-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4fb63-117">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4fb63-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4fb63-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb63-118">-DefaultProfile</span></span>
<span data-ttu-id="4fb63-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb63-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fb63-120">-ID</span><span class="sxs-lookup"><span data-stu-id="4fb63-120">-Id</span></span>
<span data-ttu-id="4fb63-121">Specifica l'ID della pianificazione del processo arrestata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fb63-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="4fb63-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb63-122">CommonParameters</span></span>
<span data-ttu-id="4fb63-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fb63-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb63-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb63-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb63-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4fb63-125">INPUTS</span></span>

### <span data-ttu-id="4fb63-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4fb63-126">System.String</span></span>

### <span data-ttu-id="4fb63-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4fb63-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="4fb63-128">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4fb63-128">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="4fb63-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4fb63-129">OUTPUTS</span></span>

### <span data-ttu-id="4fb63-130">System. void</span><span class="sxs-lookup"><span data-stu-id="4fb63-130">System.Void</span></span>

## <span data-ttu-id="4fb63-131">Note</span><span class="sxs-lookup"><span data-stu-id="4fb63-131">NOTES</span></span>

## <span data-ttu-id="4fb63-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4fb63-132">RELATED LINKS</span></span>

[<span data-ttu-id="4fb63-133">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4fb63-133">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="4fb63-134">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4fb63-134">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="4fb63-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="4fb63-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="4fb63-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4fb63-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="4fb63-137">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4fb63-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="4fb63-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4fb63-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="4fb63-139">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="4fb63-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


