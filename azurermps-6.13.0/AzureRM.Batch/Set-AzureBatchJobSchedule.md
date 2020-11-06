---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 5e26bd47c9c53b88442505aeb66d81a96c137b1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507616"
---
# <span data-ttu-id="7fb37-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7fb37-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="7fb37-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7fb37-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb37-103">Imposta una pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="7fb37-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fb37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7fb37-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fb37-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7fb37-105">DESCRIPTION</span></span>
<span data-ttu-id="7fb37-106">Il cmdlet **set-AzureBatchJobSchedule** imposta una pianificazione dei processi nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="7fb37-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="7fb37-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7fb37-107">EXAMPLES</span></span>

## <span data-ttu-id="7fb37-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7fb37-108">PARAMETERS</span></span>

### <span data-ttu-id="7fb37-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7fb37-109">-BatchContext</span></span>
<span data-ttu-id="7fb37-110">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="7fb37-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7fb37-111">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="7fb37-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7fb37-112">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="7fb37-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7fb37-113">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7fb37-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7fb37-114">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7fb37-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7fb37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb37-115">-DefaultProfile</span></span>
<span data-ttu-id="7fb37-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7fb37-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fb37-117">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="7fb37-117">-JobSchedule</span></span>
<span data-ttu-id="7fb37-118">Specifica un oggetto **PSCloudJobSchedule** che rappresenta una pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="7fb37-118">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="7fb37-119">Per ottenere un oggetto **PSCloudJobSchedule** , usa il cmdlet Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="7fb37-119">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb37-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb37-120">CommonParameters</span></span>
<span data-ttu-id="7fb37-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fb37-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb37-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fb37-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb37-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7fb37-123">INPUTS</span></span>

### <span data-ttu-id="7fb37-124">Microsoft.Azure.Commands.Batch. Models. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7fb37-124">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>
<span data-ttu-id="7fb37-125">Parametri: JobSchedule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7fb37-125">Parameters: JobSchedule (ByValue)</span></span>

### <span data-ttu-id="7fb37-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7fb37-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="7fb37-127">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7fb37-127">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="7fb37-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7fb37-128">OUTPUTS</span></span>

### <span data-ttu-id="7fb37-129">System. void</span><span class="sxs-lookup"><span data-stu-id="7fb37-129">System.Void</span></span>

## <span data-ttu-id="7fb37-130">Note</span><span class="sxs-lookup"><span data-stu-id="7fb37-130">NOTES</span></span>

## <span data-ttu-id="7fb37-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7fb37-131">RELATED LINKS</span></span>

[<span data-ttu-id="7fb37-132">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7fb37-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="7fb37-133">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7fb37-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="7fb37-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7fb37-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="7fb37-135">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7fb37-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="7fb37-136">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7fb37-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="7fb37-137">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7fb37-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


