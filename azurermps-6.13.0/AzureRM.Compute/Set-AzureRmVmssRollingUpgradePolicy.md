---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssRollingUpgradePolicy.md
ms.openlocfilehash: 872012c6d00f5251c53b289e99ee4a4436f4b8aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520254"
---
# <span data-ttu-id="aa5ca-101">Set-AzureRmVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="aa5ca-101">Set-AzureRmVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="aa5ca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa5ca-102">SYNOPSIS</span></span>
<span data-ttu-id="aa5ca-103">Imposta le proprietà dei criteri di aggiornamento a rotazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-103">Sets the VMSS rolling upgrade policy properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa5ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa5ca-104">SYNTAX</span></span>

```
Set-AzureRmVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa5ca-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa5ca-105">DESCRIPTION</span></span>
<span data-ttu-id="aa5ca-106">Imposta le proprietà dei criteri di aggiornamento a rotazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="aa5ca-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa5ca-107">EXAMPLES</span></span>

### <span data-ttu-id="aa5ca-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aa5ca-108">Example 1</span></span>
```
PS C:\> Set-AzureRmVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="aa5ca-109">Questo comando imposta 40% per MaxBatchInstance, 35% per MaxUnhealthyInstance, 30% per MaxUnhealthyUpgradedInstance e 30 secondi di pausa tra i batch per VMSS oggetto local $vmss.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="aa5ca-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa5ca-110">PARAMETERS</span></span>

### <span data-ttu-id="aa5ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa5ca-111">-DefaultProfile</span></span>
<span data-ttu-id="aa5ca-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa5ca-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="aa5ca-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="aa5ca-114">Percentuale massima delle istanze totali della macchina virtuale che verranno aggiornate simultaneamente dall'aggiornamento a rotazione in un unico batch.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="aa5ca-115">Poiché si tratta di un massimo, le istanze non sane nei batch precedenti o futuri possono causare una diminuzione della percentuale di istanze in un batch per garantire maggiore affidabilità.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="aa5ca-116">Se il valore non è specificato, viene impostato su 20.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-116">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa5ca-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="aa5ca-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="aa5ca-118">La percentuale massima delle istanze totali della macchina virtuale nel set di proporzioni che possono essere non sane contemporaneamente, come risultato dell'aggiornamento o per essere stati trovati in uno stato non sano dai controlli di integrità della macchina virtuale prima dell'interruzione dell'aggiornamento a rotazione.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="aa5ca-119">Questo vincolo verrà controllato prima di iniziare qualsiasi batch.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="aa5ca-120">Se il valore non è specificato, viene impostato su 20.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-120">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa5ca-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="aa5ca-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="aa5ca-122">La percentuale massima delle istanze di macchine virtuali aggiornate che possono essere trovate in uno stato non sano.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="aa5ca-123">Questo controllo avverrà dopo l'aggiornamento di ogni batch.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="aa5ca-124">Se questa percentuale viene mai superata, l'aggiornamento a rotazione viene interrotto.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="aa5ca-125">Se il valore non è specificato, viene impostato su 20.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-125">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa5ca-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="aa5ca-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="aa5ca-127">Il tempo di attesa tra il completamento dell'aggiornamento per tutte le macchine virtuali in un unico batch e l'avvio del batch successivo.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="aa5ca-128">La durata dell'ora deve essere specificata nel formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="aa5ca-129">Il valore predefinito è 0 secondi (PT0S).</span><span class="sxs-lookup"><span data-stu-id="aa5ca-129">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="aa5ca-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="aa5ca-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="aa5ca-131">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="aa5ca-132">Puoi usare il cmdlet New-AzureRmVmssConfig per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-132">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa5ca-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aa5ca-133">-Confirm</span></span>
<span data-ttu-id="aa5ca-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa5ca-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa5ca-135">-WhatIf</span></span>
<span data-ttu-id="aa5ca-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa5ca-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa5ca-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa5ca-138">CommonParameters</span></span>
<span data-ttu-id="aa5ca-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa5ca-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa5ca-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa5ca-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa5ca-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa5ca-141">INPUTS</span></span>

### <span data-ttu-id="aa5ca-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="aa5ca-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="aa5ca-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="aa5ca-143">System.Int32</span></span>

### <span data-ttu-id="aa5ca-144">System. String</span><span class="sxs-lookup"><span data-stu-id="aa5ca-144">System.String</span></span>

## <span data-ttu-id="aa5ca-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa5ca-145">OUTPUTS</span></span>

### <span data-ttu-id="aa5ca-146">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="aa5ca-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="aa5ca-147">Note</span><span class="sxs-lookup"><span data-stu-id="aa5ca-147">NOTES</span></span>

## <span data-ttu-id="aa5ca-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa5ca-148">RELATED LINKS</span></span>