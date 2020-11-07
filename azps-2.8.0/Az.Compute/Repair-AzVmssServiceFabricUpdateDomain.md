---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: d593f7444d6a14c6dbff72ac3922265938d7816a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675228"
---
# <span data-ttu-id="922a1-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="922a1-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="922a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="922a1-102">SYNOPSIS</span></span>
<span data-ttu-id="922a1-103">Manuale della piattaforma di aggiornamento del dominio per aggiornare le macchine virtuali in un set di scale della macchina virtuale in tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="922a1-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="922a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="922a1-104">SYNTAX</span></span>

### <span data-ttu-id="922a1-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="922a1-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="922a1-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="922a1-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="922a1-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="922a1-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="922a1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="922a1-108">DESCRIPTION</span></span>
<span data-ttu-id="922a1-109">Force Manual Platform Update Domain Walk per aggiornare le macchine virtuali in un set di scale della macchina virtuale in tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="922a1-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="922a1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="922a1-110">EXAMPLES</span></span>

### <span data-ttu-id="922a1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="922a1-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="922a1-112">Questo comando forza il percorso di aggiornamento di Service Fabric su UD 0 per il set di scale della macchina virtuale specificato dal nome del gruppo di risorse e dal nome del set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="922a1-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="922a1-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="922a1-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="922a1-114">Questo comando forza il percorso di aggiornamento del tessuto di servizio su UD 1 per il set di scale della macchina virtuale specificato dall'oggetto set scala VM.</span><span class="sxs-lookup"><span data-stu-id="922a1-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="922a1-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="922a1-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="922a1-116">Questo comando forza il percorso di aggiornamento del tessuto di servizio su UD 2 per il set di scale della macchina virtuale specificato dall'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="922a1-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="922a1-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="922a1-117">PARAMETERS</span></span>

### <span data-ttu-id="922a1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="922a1-118">-AsJob</span></span>
<span data-ttu-id="922a1-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="922a1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="922a1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="922a1-120">-DefaultProfile</span></span>
<span data-ttu-id="922a1-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="922a1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="922a1-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="922a1-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="922a1-123">Il dominio di aggiornamento della piattaforma per cui è richiesto un percorso di ripristino manuale.</span><span class="sxs-lookup"><span data-stu-id="922a1-123">The platform update domain for which a manual recovery walk is requested.</span></span>

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

### <span data-ttu-id="922a1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="922a1-124">-ResourceGroupName</span></span>
<span data-ttu-id="922a1-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="922a1-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="922a1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="922a1-126">-ResourceId</span></span>
<span data-ttu-id="922a1-127">ID risorsa per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="922a1-127">The resource id for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="922a1-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="922a1-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="922a1-129">Oggetto set scala della macchina virtuale locale</span><span class="sxs-lookup"><span data-stu-id="922a1-129">Local virtual machine scale set object</span></span>

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

### <span data-ttu-id="922a1-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="922a1-130">-VMScaleSetName</span></span>
<span data-ttu-id="922a1-131">Nome del set di scale della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="922a1-131">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="922a1-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="922a1-132">-Confirm</span></span>
<span data-ttu-id="922a1-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="922a1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="922a1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="922a1-134">-WhatIf</span></span>
<span data-ttu-id="922a1-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="922a1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="922a1-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="922a1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="922a1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="922a1-137">CommonParameters</span></span>
<span data-ttu-id="922a1-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="922a1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="922a1-139">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="922a1-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="922a1-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="922a1-140">INPUTS</span></span>

### <span data-ttu-id="922a1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="922a1-141">System.String</span></span>

### <span data-ttu-id="922a1-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="922a1-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="922a1-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="922a1-143">OUTPUTS</span></span>

### <span data-ttu-id="922a1-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSRecoveryWalkResponse</span><span class="sxs-lookup"><span data-stu-id="922a1-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="922a1-145">Note</span><span class="sxs-lookup"><span data-stu-id="922a1-145">NOTES</span></span>

## <span data-ttu-id="922a1-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="922a1-146">RELATED LINKS</span></span>
