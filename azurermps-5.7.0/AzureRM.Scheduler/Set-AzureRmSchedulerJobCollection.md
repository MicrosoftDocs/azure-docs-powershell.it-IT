---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F9CF1EEB-6EFF-4C24-AC79-1328034D22A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: fc2375e66dbc47ccadf11d0f7dd9dd66e42470de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687005"
---
# <span data-ttu-id="d0568-101">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d0568-101">Set-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="d0568-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0568-102">SYNOPSIS</span></span>
<span data-ttu-id="d0568-103">Modifica una raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="d0568-103">Modifies a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0568-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0568-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-Location <String>]
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0568-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0568-105">DESCRIPTION</span></span>
<span data-ttu-id="d0568-106">Il cmdlet **set-AzureRmSchedulerJobCollection** modifica una raccolta processi in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="d0568-106">The **Set-AzureRmSchedulerJobCollection** cmdlet modifies a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="d0568-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0568-107">EXAMPLES</span></span>

## <span data-ttu-id="d0568-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0568-108">PARAMETERS</span></span>

### <span data-ttu-id="d0568-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0568-109">-DefaultProfile</span></span>
<span data-ttu-id="d0568-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0568-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0568-111">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="d0568-111">-Frequency</span></span>
<span data-ttu-id="d0568-112">Specifica la frequenza massima che puoi specificare in qualsiasi processo nella raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="d0568-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="d0568-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d0568-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d0568-114">Minuto</span><span class="sxs-lookup"><span data-stu-id="d0568-114">Minute</span></span> 
- <span data-ttu-id="d0568-115">Ora</span><span class="sxs-lookup"><span data-stu-id="d0568-115">Hour</span></span> 
- <span data-ttu-id="d0568-116">Giorno</span><span class="sxs-lookup"><span data-stu-id="d0568-116">Day</span></span> 
- <span data-ttu-id="d0568-117">Settimana</span><span class="sxs-lookup"><span data-stu-id="d0568-117">Week</span></span> 
- <span data-ttu-id="d0568-118">Mese</span><span class="sxs-lookup"><span data-stu-id="d0568-118">Month</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0568-119">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="d0568-119">-Interval</span></span>
<span data-ttu-id="d0568-120">Specifica un intervallo di ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="d0568-120">Specifies an interval of recurrence.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0568-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d0568-121">-JobCollectionName</span></span>
<span data-ttu-id="d0568-122">Specifica il nome di una raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="d0568-122">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="d0568-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d0568-123">-Location</span></span>
<span data-ttu-id="d0568-124">Specifica l'area di Azure in cui è presente la raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="d0568-124">Specifies the Azure region in which the job collection exists.</span></span>

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

### <span data-ttu-id="d0568-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="d0568-125">-MaxJobCount</span></span>
<span data-ttu-id="d0568-126">Specifica il numero massimo di processi che è possibile creare nella raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="d0568-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="d0568-127">Il valore massimo dipende dal piano specificato dal parametro *Plan* .</span><span class="sxs-lookup"><span data-stu-id="d0568-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0568-128">-Piano</span><span class="sxs-lookup"><span data-stu-id="d0568-128">-Plan</span></span>
<span data-ttu-id="d0568-129">Specifica il piano di raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="d0568-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="d0568-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d0568-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d0568-131">Gratuito</span><span class="sxs-lookup"><span data-stu-id="d0568-131">Free</span></span> 
- <span data-ttu-id="d0568-132">Standard</span><span class="sxs-lookup"><span data-stu-id="d0568-132">Standard</span></span> 
- <span data-ttu-id="d0568-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="d0568-133">P10Premium</span></span> 
- <span data-ttu-id="d0568-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="d0568-134">P20Premium</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Standard, P10Premium, P20Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0568-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0568-135">-ResourceGroupName</span></span>
<span data-ttu-id="d0568-136">Specifica il gruppo di risorse della raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="d0568-136">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="d0568-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d0568-137">-Confirm</span></span>
<span data-ttu-id="d0568-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0568-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0568-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0568-139">-WhatIf</span></span>
<span data-ttu-id="d0568-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0568-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0568-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0568-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0568-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0568-142">CommonParameters</span></span>
<span data-ttu-id="d0568-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0568-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0568-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0568-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0568-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0568-145">INPUTS</span></span>

### <span data-ttu-id="d0568-146">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d0568-146">None</span></span>
<span data-ttu-id="d0568-147">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d0568-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d0568-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0568-148">OUTPUTS</span></span>

### <span data-ttu-id="d0568-149">Microsoft. Azure. Commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="d0568-149">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="d0568-150">Note</span><span class="sxs-lookup"><span data-stu-id="d0568-150">NOTES</span></span>

## <span data-ttu-id="d0568-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0568-151">RELATED LINKS</span></span>

[<span data-ttu-id="d0568-152">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d0568-152">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d0568-153">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d0568-153">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d0568-154">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d0568-154">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d0568-155">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d0568-155">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d0568-156">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d0568-156">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)


