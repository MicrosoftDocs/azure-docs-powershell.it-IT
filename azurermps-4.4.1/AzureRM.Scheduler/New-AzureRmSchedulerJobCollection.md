---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: d3577b906134a940a9339441f305d98c32b8fe74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519974"
---
# <span data-ttu-id="982e5-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="982e5-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="982e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="982e5-102">SYNOPSIS</span></span>
<span data-ttu-id="982e5-103">Crea una raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="982e5-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="982e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="982e5-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="982e5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="982e5-105">DESCRIPTION</span></span>
<span data-ttu-id="982e5-106">Il cmdlet **New-AzureRmSchedulerJobCollection** crea una raccolta di processi in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="982e5-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="982e5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="982e5-107">EXAMPLES</span></span>

## <span data-ttu-id="982e5-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="982e5-108">PARAMETERS</span></span>

### <span data-ttu-id="982e5-109">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="982e5-109">-Frequency</span></span>
<span data-ttu-id="982e5-110">Specifica la frequenza massima che puoi specificare in qualsiasi processo nella raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="982e5-110">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="982e5-111">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="982e5-111">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="982e5-112">Minuto</span><span class="sxs-lookup"><span data-stu-id="982e5-112">Minute</span></span> 
- <span data-ttu-id="982e5-113">Ora</span><span class="sxs-lookup"><span data-stu-id="982e5-113">Hour</span></span> 
- <span data-ttu-id="982e5-114">Giorno</span><span class="sxs-lookup"><span data-stu-id="982e5-114">Day</span></span> 
- <span data-ttu-id="982e5-115">Settimana</span><span class="sxs-lookup"><span data-stu-id="982e5-115">Week</span></span> 
- <span data-ttu-id="982e5-116">Mese</span><span class="sxs-lookup"><span data-stu-id="982e5-116">Month</span></span>

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

### <span data-ttu-id="982e5-117">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="982e5-117">-Interval</span></span>
<span data-ttu-id="982e5-118">Specifica un intervallo di ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="982e5-118">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="982e5-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="982e5-119">-JobCollectionName</span></span>
<span data-ttu-id="982e5-120">Specifica un nome per la raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="982e5-120">Specifies a name for the job collection.</span></span>

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

### <span data-ttu-id="982e5-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="982e5-121">-Location</span></span>
<span data-ttu-id="982e5-122">Specifica l'area di Azure in cui questo cmdlet crea la raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="982e5-122">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

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

### <span data-ttu-id="982e5-123">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="982e5-123">-MaxJobCount</span></span>
<span data-ttu-id="982e5-124">Specifica il numero massimo di processi che è possibile creare nella raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="982e5-124">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="982e5-125">Il valore massimo dipende dal piano specificato dal parametro *Plan* .</span><span class="sxs-lookup"><span data-stu-id="982e5-125">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="982e5-126">-Piano</span><span class="sxs-lookup"><span data-stu-id="982e5-126">-Plan</span></span>
<span data-ttu-id="982e5-127">Specifica il piano di raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="982e5-127">Specifies the job collection plan.</span></span>
<span data-ttu-id="982e5-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="982e5-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="982e5-129">Gratuito</span><span class="sxs-lookup"><span data-stu-id="982e5-129">Free</span></span> 
- <span data-ttu-id="982e5-130">Standard</span><span class="sxs-lookup"><span data-stu-id="982e5-130">Standard</span></span> 
- <span data-ttu-id="982e5-131">P10Premium</span><span class="sxs-lookup"><span data-stu-id="982e5-131">P10Premium</span></span> 
- <span data-ttu-id="982e5-132">P20Premium</span><span class="sxs-lookup"><span data-stu-id="982e5-132">P20Premium</span></span>

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

### <span data-ttu-id="982e5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="982e5-133">-ResourceGroupName</span></span>
<span data-ttu-id="982e5-134">Specifica il gruppo di risorse per la raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="982e5-134">Specifies the resource group for the job collection.</span></span>

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

### <span data-ttu-id="982e5-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="982e5-135">-Confirm</span></span>
<span data-ttu-id="982e5-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="982e5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="982e5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="982e5-137">-WhatIf</span></span>
<span data-ttu-id="982e5-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="982e5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="982e5-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="982e5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="982e5-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="982e5-140">-DefaultProfile</span></span>
<span data-ttu-id="982e5-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="982e5-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="982e5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="982e5-142">CommonParameters</span></span>
<span data-ttu-id="982e5-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="982e5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="982e5-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="982e5-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="982e5-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="982e5-145">INPUTS</span></span>

## <span data-ttu-id="982e5-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="982e5-146">OUTPUTS</span></span>

### <span data-ttu-id="982e5-147">Microsoft. Azure. Commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="982e5-147">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="982e5-148">Note</span><span class="sxs-lookup"><span data-stu-id="982e5-148">NOTES</span></span>

## <span data-ttu-id="982e5-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="982e5-149">RELATED LINKS</span></span>

[<span data-ttu-id="982e5-150">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="982e5-150">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="982e5-151">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="982e5-151">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="982e5-152">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="982e5-152">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="982e5-153">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="982e5-153">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="982e5-154">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="982e5-154">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


