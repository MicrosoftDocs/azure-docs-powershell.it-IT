---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: 89c4a6bd9d009456c97aa246f608c1920c27c823
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520850"
---
# <span data-ttu-id="ec0c3-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="ec0c3-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="ec0c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec0c3-102">SYNOPSIS</span></span>
<span data-ttu-id="ec0c3-103">Ottiene i processi dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec0c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec0c3-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec0c3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec0c3-105">DESCRIPTION</span></span>
<span data-ttu-id="ec0c3-106">Il cmdlet **Get-AzureRmSchedulerJob** ottiene i processi di pianificazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="ec0c3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec0c3-107">EXAMPLES</span></span>

## <span data-ttu-id="ec0c3-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec0c3-108">PARAMETERS</span></span>

### <span data-ttu-id="ec0c3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec0c3-109">-DefaultProfile</span></span>
<span data-ttu-id="ec0c3-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec0c3-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="ec0c3-111">-JobCollectionName</span></span>
<span data-ttu-id="ec0c3-112">Specifica il nome di una raccolta processo che contiene i processi da ottenere.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-112">Specifies the name of a job collection that contains jobs to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec0c3-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="ec0c3-113">-JobName</span></span>
<span data-ttu-id="ec0c3-114">Specifica il nome di un processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-114">Specifies the name of a job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec0c3-115">-JobState</span><span class="sxs-lookup"><span data-stu-id="ec0c3-115">-JobState</span></span>
<span data-ttu-id="ec0c3-116">Specifica uno stato di lavoro per ottenere i processi.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-116">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="ec0c3-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ec0c3-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ec0c3-118">Abilitato</span><span class="sxs-lookup"><span data-stu-id="ec0c3-118">Enabled</span></span> 
- <span data-ttu-id="ec0c3-119">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="ec0c3-119">Disabled</span></span> 
- <span data-ttu-id="ec0c3-120">Faulted</span><span class="sxs-lookup"><span data-stu-id="ec0c3-120">Faulted</span></span> 
- <span data-ttu-id="ec0c3-121">Completato</span><span class="sxs-lookup"><span data-stu-id="ec0c3-121">Completed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec0c3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec0c3-122">-ResourceGroupName</span></span>
<span data-ttu-id="ec0c3-123">Specifica il gruppo di risorse dei processi da ottenere.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-123">Specifies the resource group of the jobs to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec0c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec0c3-124">CommonParameters</span></span>
<span data-ttu-id="ec0c3-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec0c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec0c3-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec0c3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec0c3-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec0c3-127">INPUTS</span></span>

### <span data-ttu-id="ec0c3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ec0c3-128">System.String</span></span>

## <span data-ttu-id="ec0c3-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec0c3-129">OUTPUTS</span></span>

### <span data-ttu-id="ec0c3-130">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ec0c3-130">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="ec0c3-131">Note</span><span class="sxs-lookup"><span data-stu-id="ec0c3-131">NOTES</span></span>

## <span data-ttu-id="ec0c3-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec0c3-132">RELATED LINKS</span></span>

[<span data-ttu-id="ec0c3-133">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ec0c3-133">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="ec0c3-134">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ec0c3-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ec0c3-135">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ec0c3-135">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="ec0c3-136">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ec0c3-136">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="ec0c3-137">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ec0c3-137">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="ec0c3-138">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="ec0c3-138">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="ec0c3-139">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ec0c3-139">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="ec0c3-140">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ec0c3-140">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="ec0c3-141">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ec0c3-141">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="ec0c3-142">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ec0c3-142">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


