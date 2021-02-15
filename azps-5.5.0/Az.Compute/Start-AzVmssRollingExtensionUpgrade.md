---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingextensionupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
ms.openlocfilehash: a98818a855ef7bc75fb27c466dd0ba555d53a10f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200622"
---
# <span data-ttu-id="04b2e-101">Start-AzVmssRollingExtensionUpgrade</span><span class="sxs-lookup"><span data-stu-id="04b2e-101">Start-AzVmssRollingExtensionUpgrade</span></span>

## <span data-ttu-id="04b2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04b2e-102">SYNOPSIS</span></span>
<span data-ttu-id="04b2e-103">Questo cmdlet avvia un aggiornamento in sequenza per tutte le estensioni del set di scalabilità delle macchine virtuali specificato alla versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="04b2e-103">This cmdlet starts a rolling upgrade for all extensions on the given Virtual Machine Scale Set to the latest available version.</span></span> 

## <span data-ttu-id="04b2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04b2e-104">SYNTAX</span></span>

### <span data-ttu-id="04b2e-105">DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="04b2e-105">DefaultParameter</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceGroupName <String> -VMScaleSetName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04b2e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="04b2e-106">ByInputObject</span></span>
```
Start-AzVmssRollingExtensionUpgrade -VirtualMachineScaleSet <PSVirtualMachineScaleSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04b2e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="04b2e-107">ByResourceId</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04b2e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="04b2e-108">DESCRIPTION</span></span>
<span data-ttu-id="04b2e-109">Avvia un aggiornamento in sequenza per spostare tutte le estensioni di questo set di scalabilità delle macchine virtuali alla versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="04b2e-109">Starts a rolling upgrade to move all extensions on this virtual machine scale set to the latest available version.</span></span>
<span data-ttu-id="04b2e-110">Le estensioni che eseguono già l'ultima versione disponibile non sono interessate.</span><span class="sxs-lookup"><span data-stu-id="04b2e-110">Extensions which are already running the latest available version are not affected.</span></span>

## <span data-ttu-id="04b2e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04b2e-111">EXAMPLES</span></span>

### <span data-ttu-id="04b2e-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="04b2e-112">Example 1</span></span>
```powershell
PS C:\> $vmss = Get-AzVM -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name "testExtension" -Publisher Microsoft.CPlat.Core -Type "NullWindows" -TypeHandlerVersion "3.0" -AutoUpgradeMinorVersion $True  -Setting "";
PS C:\> Start-AzVmssRollingExtensionUpgrade -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
```

<span data-ttu-id="04b2e-113">Questo esempio ottiene il set di scala della macchina virtuale esistente "MyVmssName" e aggiunge un'estensione.</span><span class="sxs-lookup"><span data-stu-id="04b2e-113">This example gets the existing VM scale set "MyVmssName", and adds an extension to it.</span></span> <span data-ttu-id="04b2e-114">Il comando finale esegue il processo di aggiornamento dell'estensione in fase di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="04b2e-114">The final command runs the extension rolling upgrade process.</span></span> 

## <span data-ttu-id="04b2e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04b2e-115">PARAMETERS</span></span>

### <span data-ttu-id="04b2e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04b2e-116">-AsJob</span></span>
<span data-ttu-id="04b2e-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="04b2e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04b2e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04b2e-118">-DefaultProfile</span></span>
<span data-ttu-id="04b2e-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="04b2e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04b2e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04b2e-120">-ResourceGroupName</span></span>
<span data-ttu-id="04b2e-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="04b2e-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04b2e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04b2e-122">-ResourceId</span></span>
<span data-ttu-id="04b2e-123">ID risorsa dell'oggetto set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="04b2e-123">The resource Id of the VM scale set object.</span></span> 

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04b2e-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="04b2e-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="04b2e-125">Oggetto set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="04b2e-125">The VM scale set object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04b2e-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="04b2e-126">-VMScaleSetName</span></span>
<span data-ttu-id="04b2e-127">Nome del set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="04b2e-127">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04b2e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04b2e-128">-Confirm</span></span>
<span data-ttu-id="04b2e-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04b2e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04b2e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04b2e-130">-WhatIf</span></span>
<span data-ttu-id="04b2e-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04b2e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04b2e-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04b2e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04b2e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b2e-133">CommonParameters</span></span>
<span data-ttu-id="04b2e-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04b2e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b2e-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="04b2e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b2e-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="04b2e-136">INPUTS</span></span>

### <span data-ttu-id="04b2e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="04b2e-137">System.String</span></span>

### <span data-ttu-id="04b2e-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="04b2e-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="04b2e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04b2e-139">OUTPUTS</span></span>

### <span data-ttu-id="04b2e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="04b2e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="04b2e-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="04b2e-141">NOTES</span></span>

## <span data-ttu-id="04b2e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04b2e-142">RELATED LINKS</span></span>
