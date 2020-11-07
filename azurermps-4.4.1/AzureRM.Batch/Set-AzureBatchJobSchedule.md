---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 0f9d20cdd1d2acabbd644fda91f5f8d22ff1ccd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688362"
---
# <span data-ttu-id="56e34-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="56e34-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="56e34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56e34-102">SYNOPSIS</span></span>
<span data-ttu-id="56e34-103">Imposta una pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="56e34-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56e34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56e34-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56e34-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56e34-105">DESCRIPTION</span></span>
<span data-ttu-id="56e34-106">Il cmdlet **set-AzureBatchJobSchedule** imposta una pianificazione dei processi nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="56e34-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="56e34-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56e34-107">EXAMPLES</span></span>

## <span data-ttu-id="56e34-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56e34-108">PARAMETERS</span></span>

### <span data-ttu-id="56e34-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="56e34-109">-BatchContext</span></span>
<span data-ttu-id="56e34-110">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="56e34-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="56e34-111">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="56e34-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="56e34-112">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="56e34-112">-JobSchedule</span></span>
<span data-ttu-id="56e34-113">Specifica un oggetto **PSCloudJobSchedule** che rappresenta una pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="56e34-113">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="56e34-114">Per ottenere un oggetto **PSCloudJobSchedule** , usa il cmdlet Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="56e34-114">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="56e34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e34-115">-DefaultProfile</span></span>
<span data-ttu-id="56e34-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56e34-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56e34-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e34-117">CommonParameters</span></span>
<span data-ttu-id="56e34-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56e34-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e34-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56e34-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e34-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56e34-120">INPUTS</span></span>

### <span data-ttu-id="56e34-121">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="56e34-121">BatchAccountContext</span></span>
<span data-ttu-id="56e34-122">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="56e34-122">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="56e34-123">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="56e34-123">PSCloudJobSchedule</span></span>
<span data-ttu-id="56e34-124">Il parametro ' JobSchedule ' accetta il valore di tipo ' PSCloudJobSchedule ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="56e34-124">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="56e34-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56e34-125">OUTPUTS</span></span>

## <span data-ttu-id="56e34-126">Note</span><span class="sxs-lookup"><span data-stu-id="56e34-126">NOTES</span></span>

## <span data-ttu-id="56e34-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56e34-127">RELATED LINKS</span></span>

[<span data-ttu-id="56e34-128">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="56e34-128">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="56e34-129">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="56e34-129">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="56e34-130">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="56e34-130">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="56e34-131">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="56e34-131">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="56e34-132">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="56e34-132">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="56e34-133">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="56e34-133">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


