---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F9CF1EEB-6EFF-4C24-AC79-1328034D22A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 535455f73795d85acf05da191694f35dbeee9ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513463"
---
# <span data-ttu-id="83ef0-101">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="83ef0-101">Set-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="83ef0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="83ef0-103">Modifica una raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="83ef0-103">Modifies a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83ef0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83ef0-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-Location <String>]
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83ef0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83ef0-105">DESCRIPTION</span></span>
<span data-ttu-id="83ef0-106">Il cmdlet **set-AzureRmSchedulerJobCollection** modifica una raccolta processi in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="83ef0-106">The **Set-AzureRmSchedulerJobCollection** cmdlet modifies a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="83ef0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83ef0-107">EXAMPLES</span></span>

## <span data-ttu-id="83ef0-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83ef0-108">PARAMETERS</span></span>

### <span data-ttu-id="83ef0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83ef0-109">-DefaultProfile</span></span>
<span data-ttu-id="83ef0-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83ef0-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83ef0-111">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="83ef0-111">-Frequency</span></span>
<span data-ttu-id="83ef0-112">Specifica la frequenza massima che puoi specificare in qualsiasi processo nella raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="83ef0-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="83ef0-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="83ef0-113">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="83ef0-114">Minuto</span><span class="sxs-lookup"><span data-stu-id="83ef0-114">Minute</span></span> 
- <span data-ttu-id="83ef0-115">Ora</span><span class="sxs-lookup"><span data-stu-id="83ef0-115">Hour</span></span> 
- <span data-ttu-id="83ef0-116">Giorno</span><span class="sxs-lookup"><span data-stu-id="83ef0-116">Day</span></span> 
- <span data-ttu-id="83ef0-117">Settimana</span><span class="sxs-lookup"><span data-stu-id="83ef0-117">Week</span></span> 
- <span data-ttu-id="83ef0-118">Mese</span><span class="sxs-lookup"><span data-stu-id="83ef0-118">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ef0-119">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="83ef0-119">-Interval</span></span>
<span data-ttu-id="83ef0-120">Specifica un intervallo di ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="83ef0-120">Specifies an interval of recurrence.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ef0-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="83ef0-121">-JobCollectionName</span></span>
<span data-ttu-id="83ef0-122">Specifica il nome di una raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="83ef0-122">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="83ef0-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="83ef0-123">-Location</span></span>
<span data-ttu-id="83ef0-124">Specifica l'area di Azure in cui è presente la raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="83ef0-124">Specifies the Azure region in which the job collection exists.</span></span>

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

### <span data-ttu-id="83ef0-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="83ef0-125">-MaxJobCount</span></span>
<span data-ttu-id="83ef0-126">Specifica il numero massimo di processi che è possibile creare nella raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="83ef0-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="83ef0-127">Il valore massimo dipende dal piano specificato dal parametro *Plan* .</span><span class="sxs-lookup"><span data-stu-id="83ef0-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ef0-128">-Piano</span><span class="sxs-lookup"><span data-stu-id="83ef0-128">-Plan</span></span>
<span data-ttu-id="83ef0-129">Specifica il piano di raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="83ef0-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="83ef0-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="83ef0-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="83ef0-131">Gratuito</span><span class="sxs-lookup"><span data-stu-id="83ef0-131">Free</span></span> 
- <span data-ttu-id="83ef0-132">Standard</span><span class="sxs-lookup"><span data-stu-id="83ef0-132">Standard</span></span> 
- <span data-ttu-id="83ef0-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="83ef0-133">P10Premium</span></span> 
- <span data-ttu-id="83ef0-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="83ef0-134">P20Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Standard, P10Premium, P20Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83ef0-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83ef0-135">-ResourceGroupName</span></span>
<span data-ttu-id="83ef0-136">Specifica il gruppo di risorse della raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="83ef0-136">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="83ef0-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="83ef0-137">-Confirm</span></span>
<span data-ttu-id="83ef0-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83ef0-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ef0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83ef0-139">-WhatIf</span></span>
<span data-ttu-id="83ef0-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83ef0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83ef0-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83ef0-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ef0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ef0-142">CommonParameters</span></span>
<span data-ttu-id="83ef0-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83ef0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ef0-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83ef0-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ef0-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83ef0-145">INPUTS</span></span>

### <span data-ttu-id="83ef0-146">System. String</span><span class="sxs-lookup"><span data-stu-id="83ef0-146">System.String</span></span>

## <span data-ttu-id="83ef0-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83ef0-147">OUTPUTS</span></span>

### <span data-ttu-id="83ef0-148">Microsoft. Azure. Commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="83ef0-148">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="83ef0-149">Note</span><span class="sxs-lookup"><span data-stu-id="83ef0-149">NOTES</span></span>

## <span data-ttu-id="83ef0-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83ef0-150">RELATED LINKS</span></span>

[<span data-ttu-id="83ef0-151">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="83ef0-151">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="83ef0-152">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="83ef0-152">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="83ef0-153">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="83ef0-153">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="83ef0-154">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="83ef0-154">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="83ef0-155">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="83ef0-155">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)


