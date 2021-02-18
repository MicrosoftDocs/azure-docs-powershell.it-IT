---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: ceca2477d66cb6ce19564899e67a3b66d6917cfe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181542"
---
# <span data-ttu-id="8faff-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8faff-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="8faff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8faff-102">SYNOPSIS</span></span>
<span data-ttu-id="8faff-103">Rimuove un'estensione dal sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="8faff-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="8faff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8faff-104">SYNTAX</span></span>

### <span data-ttu-id="8faff-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8faff-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8faff-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8faff-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8faff-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8faff-107">DESCRIPTION</span></span>
<span data-ttu-id="8faff-108">Il cmdlet **Remove-AzVmssExtension** rimuove un'estensione dal set di scalabilità delle macchine virtuali (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8faff-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="8faff-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8faff-109">EXAMPLES</span></span>

### <span data-ttu-id="8faff-110">Esempio 1: Rimuovere un'estensione VMSS</span><span class="sxs-lookup"><span data-stu-id="8faff-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="8faff-111">Questo comando rimuove l'estensione di un sistema VMSS e aggiorna il VMSS dopo la modifica.</span><span class="sxs-lookup"><span data-stu-id="8faff-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="8faff-112">Esempio 2: Rimuovere un'istanza da un VMSS</span><span class="sxs-lookup"><span data-stu-id="8faff-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="8faff-113">Questo comando rimuove l'ID estensione specificato dal sistema VMS che appartiene al gruppo di risorse denominato Group002.</span><span class="sxs-lookup"><span data-stu-id="8faff-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="8faff-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8faff-114">PARAMETERS</span></span>

### <span data-ttu-id="8faff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8faff-115">-DefaultProfile</span></span>
<span data-ttu-id="8faff-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8faff-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8faff-117">-Id</span><span class="sxs-lookup"><span data-stu-id="8faff-117">-Id</span></span>
<span data-ttu-id="8faff-118">Specifica l'ID dell'estensione che questo cmdlet rimuove da VMSS.</span><span class="sxs-lookup"><span data-stu-id="8faff-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8faff-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8faff-119">-Name</span></span>
<span data-ttu-id="8faff-120">Specifica il nome dell'estensione che questo cmdlet rimuove dal sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="8faff-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8faff-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8faff-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8faff-122">Specifica il sistema VMSS da cui rimuovere l'estensione.</span><span class="sxs-lookup"><span data-stu-id="8faff-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="8faff-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8faff-123">-Confirm</span></span>
<span data-ttu-id="8faff-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8faff-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8faff-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8faff-125">-WhatIf</span></span>
<span data-ttu-id="8faff-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8faff-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8faff-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8faff-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8faff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8faff-128">CommonParameters</span></span>
<span data-ttu-id="8faff-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8faff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8faff-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8faff-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8faff-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="8faff-131">INPUTS</span></span>

### <span data-ttu-id="8faff-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8faff-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="8faff-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8faff-133">System.String</span></span>

## <span data-ttu-id="8faff-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8faff-134">OUTPUTS</span></span>

### <span data-ttu-id="8faff-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8faff-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8faff-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="8faff-136">NOTES</span></span>

## <span data-ttu-id="8faff-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8faff-137">RELATED LINKS</span></span>

[<span data-ttu-id="8faff-138">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8faff-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
