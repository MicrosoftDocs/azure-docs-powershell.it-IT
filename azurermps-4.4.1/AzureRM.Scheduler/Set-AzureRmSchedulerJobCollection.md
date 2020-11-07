---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F9CF1EEB-6EFF-4C24-AC79-1328034D22A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 141a91272e805cc30f290d544a9a33c7c81484e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687081"
---
# <span data-ttu-id="935b6-101">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="935b6-101">Set-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="935b6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="935b6-102">SYNOPSIS</span></span>
<span data-ttu-id="935b6-103">Modifica una raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="935b6-103">Modifies a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="935b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="935b6-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-Location <String>]
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="935b6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="935b6-105">DESCRIPTION</span></span>
<span data-ttu-id="935b6-106">Il cmdlet **set-AzureRmSchedulerJobCollection** modifica una raccolta processi in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="935b6-106">The **Set-AzureRmSchedulerJobCollection** cmdlet modifies a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="935b6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="935b6-107">EXAMPLES</span></span>

## <span data-ttu-id="935b6-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="935b6-108">PARAMETERS</span></span>

### <span data-ttu-id="935b6-109">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="935b6-109">-Frequency</span></span>
<span data-ttu-id="935b6-110">Specifica la frequenza massima che puoi specificare in qualsiasi processo nella raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="935b6-110">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="935b6-111">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="935b6-111">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="935b6-112">Minuto</span><span class="sxs-lookup"><span data-stu-id="935b6-112">Minute</span></span> 
- <span data-ttu-id="935b6-113">Ora</span><span class="sxs-lookup"><span data-stu-id="935b6-113">Hour</span></span> 
- <span data-ttu-id="935b6-114">Giorno</span><span class="sxs-lookup"><span data-stu-id="935b6-114">Day</span></span> 
- <span data-ttu-id="935b6-115">Settimana</span><span class="sxs-lookup"><span data-stu-id="935b6-115">Week</span></span> 
- <span data-ttu-id="935b6-116">Mese</span><span class="sxs-lookup"><span data-stu-id="935b6-116">Month</span></span>

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

### <span data-ttu-id="935b6-117">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="935b6-117">-Interval</span></span>
<span data-ttu-id="935b6-118">Specifica un intervallo di ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="935b6-118">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="935b6-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="935b6-119">-JobCollectionName</span></span>
<span data-ttu-id="935b6-120">Specifica il nome di una raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="935b6-120">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="935b6-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="935b6-121">-Location</span></span>
<span data-ttu-id="935b6-122">Specifica l'area di Azure in cui è presente la raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="935b6-122">Specifies the Azure region in which the job collection exists.</span></span>

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

### <span data-ttu-id="935b6-123">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="935b6-123">-MaxJobCount</span></span>
<span data-ttu-id="935b6-124">Specifica il numero massimo di processi che è possibile creare nella raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="935b6-124">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="935b6-125">Il valore massimo dipende dal piano specificato dal parametro *Plan* .</span><span class="sxs-lookup"><span data-stu-id="935b6-125">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="935b6-126">-Piano</span><span class="sxs-lookup"><span data-stu-id="935b6-126">-Plan</span></span>
<span data-ttu-id="935b6-127">Specifica il piano di raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="935b6-127">Specifies the job collection plan.</span></span>
<span data-ttu-id="935b6-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="935b6-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="935b6-129">Gratuito</span><span class="sxs-lookup"><span data-stu-id="935b6-129">Free</span></span> 
- <span data-ttu-id="935b6-130">Standard</span><span class="sxs-lookup"><span data-stu-id="935b6-130">Standard</span></span> 
- <span data-ttu-id="935b6-131">P10Premium</span><span class="sxs-lookup"><span data-stu-id="935b6-131">P10Premium</span></span> 
- <span data-ttu-id="935b6-132">P20Premium</span><span class="sxs-lookup"><span data-stu-id="935b6-132">P20Premium</span></span>

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

### <span data-ttu-id="935b6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="935b6-133">-ResourceGroupName</span></span>
<span data-ttu-id="935b6-134">Specifica il gruppo di risorse della raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="935b6-134">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="935b6-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="935b6-135">-Confirm</span></span>
<span data-ttu-id="935b6-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="935b6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="935b6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="935b6-137">-WhatIf</span></span>
<span data-ttu-id="935b6-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="935b6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="935b6-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="935b6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="935b6-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935b6-140">-DefaultProfile</span></span>
<span data-ttu-id="935b6-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="935b6-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="935b6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935b6-142">CommonParameters</span></span>
<span data-ttu-id="935b6-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="935b6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935b6-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="935b6-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935b6-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="935b6-145">INPUTS</span></span>

## <span data-ttu-id="935b6-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="935b6-146">OUTPUTS</span></span>

### <span data-ttu-id="935b6-147">Microsoft. Azure. Commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="935b6-147">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="935b6-148">Note</span><span class="sxs-lookup"><span data-stu-id="935b6-148">NOTES</span></span>

## <span data-ttu-id="935b6-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="935b6-149">RELATED LINKS</span></span>

[<span data-ttu-id="935b6-150">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="935b6-150">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="935b6-151">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="935b6-151">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="935b6-152">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="935b6-152">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="935b6-153">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="935b6-153">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="935b6-154">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="935b6-154">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)


