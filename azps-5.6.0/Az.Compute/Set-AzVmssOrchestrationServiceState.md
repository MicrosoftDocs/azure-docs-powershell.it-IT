---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: 84f208a18061d7a682fc1662c97811a19590ca65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983742"
---
# <span data-ttu-id="4ee93-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="4ee93-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="4ee93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ee93-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee93-103">Imposta lo stato del servizio di gestione per VMSS.</span><span class="sxs-lookup"><span data-stu-id="4ee93-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="4ee93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ee93-104">SYNTAX</span></span>

### <span data-ttu-id="4ee93-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="4ee93-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ee93-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="4ee93-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ee93-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="4ee93-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ee93-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4ee93-108">DESCRIPTION</span></span>
<span data-ttu-id="4ee93-109">Imposta lo stato del servizio di gestione per VMSS.</span><span class="sxs-lookup"><span data-stu-id="4ee93-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="4ee93-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ee93-110">EXAMPLES</span></span>

### <span data-ttu-id="4ee93-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4ee93-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="4ee93-112">Questo comando sospende il servizio Ripristino automatico nel sistema VMSS "vmss1" nel gruppo di risorse "rg".</span><span class="sxs-lookup"><span data-stu-id="4ee93-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="4ee93-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4ee93-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="4ee93-114">Questo comando riprende il servizio Ripristino automatico nel sistema VMSS "vmss1" nel gruppo di risorse "rg".</span><span class="sxs-lookup"><span data-stu-id="4ee93-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="4ee93-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ee93-115">PARAMETERS</span></span>

### <span data-ttu-id="4ee93-116">-Action</span><span class="sxs-lookup"><span data-stu-id="4ee93-116">-Action</span></span>
<span data-ttu-id="4ee93-117">L'azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="4ee93-117">The action to be performed.</span></span>  <span data-ttu-id="4ee93-118">I valori possibili sono Riprendi, Sospendi.</span><span class="sxs-lookup"><span data-stu-id="4ee93-118">Possible values are: Resume, Suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee93-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ee93-119">-AsJob</span></span>
<span data-ttu-id="4ee93-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4ee93-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ee93-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee93-121">-DefaultProfile</span></span>
<span data-ttu-id="4ee93-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ee93-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ee93-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ee93-123">-InputObject</span></span>
<span data-ttu-id="4ee93-124">Oggetto locale del set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4ee93-124">The local object of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="4ee93-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ee93-125">-ResourceGroupName</span></span>
<span data-ttu-id="4ee93-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4ee93-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="4ee93-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ee93-127">-ResourceId</span></span>
<span data-ttu-id="4ee93-128">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4ee93-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="4ee93-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4ee93-129">-ServiceName</span></span>
<span data-ttu-id="4ee93-130">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="4ee93-130">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee93-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4ee93-131">-VMScaleSetName</span></span>
<span data-ttu-id="4ee93-132">Nome del set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4ee93-132">The name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="4ee93-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ee93-133">-Confirm</span></span>
<span data-ttu-id="4ee93-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ee93-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ee93-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ee93-135">-WhatIf</span></span>
<span data-ttu-id="4ee93-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ee93-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ee93-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ee93-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ee93-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee93-138">CommonParameters</span></span>
<span data-ttu-id="4ee93-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ee93-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee93-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4ee93-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee93-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="4ee93-141">INPUTS</span></span>

### <span data-ttu-id="4ee93-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4ee93-142">System.String</span></span>

### <span data-ttu-id="4ee93-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4ee93-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4ee93-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ee93-144">OUTPUTS</span></span>

### <span data-ttu-id="4ee93-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="4ee93-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4ee93-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="4ee93-146">NOTES</span></span>

## <span data-ttu-id="4ee93-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ee93-147">RELATED LINKS</span></span>
