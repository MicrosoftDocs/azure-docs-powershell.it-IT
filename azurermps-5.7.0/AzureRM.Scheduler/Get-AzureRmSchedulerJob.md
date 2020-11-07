---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: d22f1acf8f99f15df83be95aafdc8ff0aefd2a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687458"
---
# <span data-ttu-id="46408-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="46408-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="46408-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="46408-102">SYNOPSIS</span></span>
<span data-ttu-id="46408-103">Ottiene i processi dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="46408-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46408-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46408-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46408-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46408-105">DESCRIPTION</span></span>
<span data-ttu-id="46408-106">Il cmdlet **Get-AzureRmSchedulerJob** ottiene i processi di pianificazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="46408-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="46408-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46408-107">EXAMPLES</span></span>

## <span data-ttu-id="46408-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="46408-108">PARAMETERS</span></span>

### <span data-ttu-id="46408-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46408-109">-DefaultProfile</span></span>
<span data-ttu-id="46408-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46408-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46408-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="46408-111">-JobCollectionName</span></span>
<span data-ttu-id="46408-112">Specifica il nome di una raccolta processo che contiene i processi da ottenere.</span><span class="sxs-lookup"><span data-stu-id="46408-112">Specifies the name of a job collection that contains jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46408-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="46408-113">-JobName</span></span>
<span data-ttu-id="46408-114">Specifica il nome di un processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="46408-114">Specifies the name of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46408-115">-JobState</span><span class="sxs-lookup"><span data-stu-id="46408-115">-JobState</span></span>
<span data-ttu-id="46408-116">Specifica uno stato di lavoro per ottenere i processi.</span><span class="sxs-lookup"><span data-stu-id="46408-116">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="46408-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="46408-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="46408-118">Abilitato</span><span class="sxs-lookup"><span data-stu-id="46408-118">Enabled</span></span> 
- <span data-ttu-id="46408-119">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="46408-119">Disabled</span></span> 
- <span data-ttu-id="46408-120">Faulted</span><span class="sxs-lookup"><span data-stu-id="46408-120">Faulted</span></span> 
- <span data-ttu-id="46408-121">Completato</span><span class="sxs-lookup"><span data-stu-id="46408-121">Completed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46408-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46408-122">-ResourceGroupName</span></span>
<span data-ttu-id="46408-123">Specifica il gruppo di risorse dei processi da ottenere.</span><span class="sxs-lookup"><span data-stu-id="46408-123">Specifies the resource group of the jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46408-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46408-124">CommonParameters</span></span>
<span data-ttu-id="46408-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46408-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46408-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46408-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46408-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="46408-127">INPUTS</span></span>

### <span data-ttu-id="46408-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="46408-128">None</span></span>
<span data-ttu-id="46408-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="46408-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="46408-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46408-130">OUTPUTS</span></span>

### <span data-ttu-id="46408-131">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="46408-131">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="46408-132">Note</span><span class="sxs-lookup"><span data-stu-id="46408-132">NOTES</span></span>

## <span data-ttu-id="46408-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46408-133">RELATED LINKS</span></span>

[<span data-ttu-id="46408-134">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="46408-134">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="46408-135">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="46408-135">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="46408-136">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="46408-136">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="46408-137">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="46408-137">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="46408-138">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="46408-138">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="46408-139">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="46408-139">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="46408-140">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="46408-140">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="46408-141">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="46408-141">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="46408-142">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="46408-142">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="46408-143">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="46408-143">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


