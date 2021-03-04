---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: e0edd9ad095f6f7887e0e3f4951828844d2521c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955982"
---
# <span data-ttu-id="d6a37-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="d6a37-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="d6a37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6a37-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a37-103">Guida manuale all'aggiornamento dei domini della piattaforma per aggiornare le macchine virtuali in un set di scala delle macchine virtuali di un tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="d6a37-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="d6a37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6a37-104">SYNTAX</span></span>

### <span data-ttu-id="d6a37-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="d6a37-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6a37-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d6a37-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6a37-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="d6a37-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6a37-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d6a37-108">DESCRIPTION</span></span>
<span data-ttu-id="d6a37-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span><span class="sxs-lookup"><span data-stu-id="d6a37-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="d6a37-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6a37-110">EXAMPLES</span></span>

### <span data-ttu-id="d6a37-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d6a37-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="d6a37-112">Questo comando forza il percorso di aggiornamento dei tessuto di servizio nel servizio UD 0 per il set di scalabilità della macchina virtuale specificato dal nome del gruppo di risorse e dal nome del set di scale.</span><span class="sxs-lookup"><span data-stu-id="d6a37-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="d6a37-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d6a37-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="d6a37-114">Questo comando impone la walk-on-UD 1 dell'aggiornamento dei tessuto di servizio per il set di scalabilità delle macchine virtuali specificato dall'oggetto set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d6a37-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="d6a37-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d6a37-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="d6a37-116">Questo comando forza la procedura di aggiornamento dei tessuto di servizio nel servizio UD 2 per il set di scala delle macchine virtuali specificato dall'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="d6a37-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="d6a37-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6a37-117">PARAMETERS</span></span>

### <span data-ttu-id="d6a37-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6a37-118">-AsJob</span></span>
<span data-ttu-id="d6a37-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d6a37-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a37-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6a37-120">-DefaultProfile</span></span>
<span data-ttu-id="d6a37-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6a37-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a37-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="d6a37-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="d6a37-123">Dominio di aggiornamento della piattaforma per cui è richiesta una procedura di ripristino manuale.</span><span class="sxs-lookup"><span data-stu-id="d6a37-123">The platform update domain for which a manual recovery walk is requested.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a37-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6a37-124">-ResourceGroupName</span></span>
<span data-ttu-id="d6a37-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d6a37-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6a37-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6a37-126">-ResourceId</span></span>
<span data-ttu-id="d6a37-127">ID risorsa per il set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d6a37-127">The resource id for the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6a37-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d6a37-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d6a37-129">Oggetto set di scalabilità della macchina virtuale locale</span><span class="sxs-lookup"><span data-stu-id="d6a37-129">Local virtual machine scale set object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6a37-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d6a37-130">-VMScaleSetName</span></span>
<span data-ttu-id="d6a37-131">Nome del set di scalabilità della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="d6a37-131">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6a37-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6a37-132">-Confirm</span></span>
<span data-ttu-id="d6a37-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6a37-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6a37-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6a37-134">-WhatIf</span></span>
<span data-ttu-id="d6a37-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6a37-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6a37-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6a37-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6a37-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a37-137">CommonParameters</span></span>
<span data-ttu-id="d6a37-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6a37-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a37-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d6a37-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a37-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="d6a37-140">INPUTS</span></span>

### <span data-ttu-id="d6a37-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d6a37-141">System.String</span></span>

### <span data-ttu-id="d6a37-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d6a37-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d6a37-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6a37-143">OUTPUTS</span></span>

### <span data-ttu-id="d6a37-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryResponse</span><span class="sxs-lookup"><span data-stu-id="d6a37-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="d6a37-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="d6a37-145">NOTES</span></span>

## <span data-ttu-id="d6a37-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6a37-146">RELATED LINKS</span></span>
