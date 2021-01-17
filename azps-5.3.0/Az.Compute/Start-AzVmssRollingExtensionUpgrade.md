---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingextensionupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
ms.openlocfilehash: a98818a855ef7bc75fb27c466dd0ba555d53a10f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477635"
---
# <span data-ttu-id="3f4f6-101">Start-AzVmssRollingExtensionUpgrade</span><span class="sxs-lookup"><span data-stu-id="3f4f6-101">Start-AzVmssRollingExtensionUpgrade</span></span>

## <span data-ttu-id="3f4f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3f4f6-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4f6-103">Questo cmdlet avvia un aggiornamento a rotazione per tutte le estensioni nella scala della macchina virtuale specificata impostata sulla versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="3f4f6-103">This cmdlet starts a rolling upgrade for all extensions on the given Virtual Machine Scale Set to the latest available version.</span></span> 

## <span data-ttu-id="3f4f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f4f6-104">SYNTAX</span></span>

### <span data-ttu-id="3f4f6-105">DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="3f4f6-105">DefaultParameter</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceGroupName <String> -VMScaleSetName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f4f6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3f4f6-106">ByInputObject</span></span>
```
Start-AzVmssRollingExtensionUpgrade -VirtualMachineScaleSet <PSVirtualMachineScaleSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f4f6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f4f6-107">ByResourceId</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f4f6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f4f6-108">DESCRIPTION</span></span>
<span data-ttu-id="3f4f6-109">Avvia un aggiornamento a rotazione per trasferire tutte le estensioni in questa scala della macchina virtuale impostata sulla versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="3f4f6-109">Starts a rolling upgrade to move all extensions on this virtual machine scale set to the latest available version.</span></span>
<span data-ttu-id="3f4f6-110">Le estensioni già in esecuzione dell'ultima versione disponibile non sono interessate.</span><span class="sxs-lookup"><span data-stu-id="3f4f6-110">Extensions which are already running the latest available version are not affected.</span></span>

## <span data-ttu-id="3f4f6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f4f6-111">EXAMPLES</span></span>

### <span data-ttu-id="3f4f6-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3f4f6-112">Example 1</span></span>
```powershell
PS C:\> $vmss = Get-AzVM -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name "testExtension" -Publisher Microsoft.CPlat.Core -Type "NullWindows" -TypeHandlerVersion "3.0" -AutoUpgradeMinorVersion $True  -Setting "";
PS C:\> Start-AzVmssRollingExtensionUpgrade -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
```

<span data-ttu-id="3f4f6-113">Questo esempio ottiene l'impostazione della scala VM esistente "MyVmssName" e aggiunge un'estensione.</span><span class="sxs-lookup"><span data-stu-id="3f4f6-113">This example gets the existing VM scale set "MyVmssName", and adds an extension to it.</span></span> <span data-ttu-id="3f4f6-114">Il comando finale esegue il processo di aggiornamento a rotazione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="3f4f6-114">The final command runs the extension rolling upgrade process.</span></span> 

## <span data-ttu-id="3f4f6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3f4f6-115">PARAMETERS</span></span>

### <span data-ttu-id="3f4f6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f4f6-116">-AsJob</span></span>
<span data-ttu-id="3f4f6-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3f4f6-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f4f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4f6-118">-DefaultProfile</span></span>
<span data-ttu-id="3f4f6-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f4f6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f4f6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f4f6-120">-ResourceGroupName</span></span>
<span data-ttu-id="3f4f6-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3f4f6-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="3f4f6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f4f6-122">-ResourceId</span></span>
<span data-ttu-id="3f4f6-123">ID risorsa dell'oggetto set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="3f4f6-123">The resource Id of the VM scale set object.</span></span> 

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

### <span data-ttu-id="3f4f6-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3f4f6-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3f4f6-125">Oggetto set della scala VM.</span><span class="sxs-lookup"><span data-stu-id="3f4f6-125">The VM scale set object.</span></span>

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

### <span data-ttu-id="3f4f6-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3f4f6-126">-VMScaleSetName</span></span>
<span data-ttu-id="3f4f6-127">Nome del set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="3f4f6-127">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="3f4f6-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3f4f6-128">-Confirm</span></span>
<span data-ttu-id="3f4f6-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f4f6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f4f6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f4f6-130">-WhatIf</span></span>
<span data-ttu-id="3f4f6-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f4f6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f4f6-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f4f6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f4f6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4f6-133">CommonParameters</span></span>
<span data-ttu-id="3f4f6-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f4f6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4f6-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f4f6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4f6-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3f4f6-136">INPUTS</span></span>

### <span data-ttu-id="3f4f6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3f4f6-137">System.String</span></span>

### <span data-ttu-id="3f4f6-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3f4f6-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="3f4f6-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f4f6-139">OUTPUTS</span></span>

### <span data-ttu-id="3f4f6-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3f4f6-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3f4f6-141">Note</span><span class="sxs-lookup"><span data-stu-id="3f4f6-141">NOTES</span></span>

## <span data-ttu-id="3f4f6-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f4f6-142">RELATED LINKS</span></span>
