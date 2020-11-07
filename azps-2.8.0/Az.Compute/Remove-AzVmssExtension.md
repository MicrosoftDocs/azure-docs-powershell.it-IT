---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: 676584e1e6814a05ba1ab49bb7c751218a16d361
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675233"
---
# <span data-ttu-id="a7f44-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a7f44-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="a7f44-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7f44-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f44-103">Rimuove un'estensione da VMSS.</span><span class="sxs-lookup"><span data-stu-id="a7f44-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="a7f44-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7f44-104">SYNTAX</span></span>

### <span data-ttu-id="a7f44-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7f44-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7f44-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7f44-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7f44-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7f44-107">DESCRIPTION</span></span>
<span data-ttu-id="a7f44-108">Il cmdlet **Remove-AzVmssExtension** consente di rimuovere un'estensione dal set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a7f44-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a7f44-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7f44-109">EXAMPLES</span></span>

### <span data-ttu-id="a7f44-110">Esempio 1: rimuovere un'estensione VMSS</span><span class="sxs-lookup"><span data-stu-id="a7f44-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="a7f44-111">Questo comando rimuove l'estensione di un VMSS e aggiorna VMSS dopo la modifica.</span><span class="sxs-lookup"><span data-stu-id="a7f44-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="a7f44-112">Esempio 2: rimuovere un'istanza dall'interno di un VMSS</span><span class="sxs-lookup"><span data-stu-id="a7f44-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="a7f44-113">Questo comando rimuove specifica l'ID di estensione da VMSS che appartiene al gruppo di risorse denominato Group002.</span><span class="sxs-lookup"><span data-stu-id="a7f44-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="a7f44-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7f44-114">PARAMETERS</span></span>

### <span data-ttu-id="a7f44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f44-115">-DefaultProfile</span></span>
<span data-ttu-id="a7f44-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7f44-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7f44-117">-ID</span><span class="sxs-lookup"><span data-stu-id="a7f44-117">-Id</span></span>
<span data-ttu-id="a7f44-118">Specifica l'ID dell'estensione rimossa da questo cmdlet da VMSS.</span><span class="sxs-lookup"><span data-stu-id="a7f44-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="a7f44-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7f44-119">-Name</span></span>
<span data-ttu-id="a7f44-120">Specifica il nome dell'estensione rimossa da questo cmdlet da VMSS.</span><span class="sxs-lookup"><span data-stu-id="a7f44-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="a7f44-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a7f44-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a7f44-122">Specifica il VMSS da cui rimuovere l'estensione.</span><span class="sxs-lookup"><span data-stu-id="a7f44-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="a7f44-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a7f44-123">-Confirm</span></span>
<span data-ttu-id="a7f44-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7f44-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7f44-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7f44-125">-WhatIf</span></span>
<span data-ttu-id="a7f44-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7f44-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7f44-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7f44-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7f44-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f44-128">CommonParameters</span></span>
<span data-ttu-id="a7f44-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7f44-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f44-130">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7f44-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f44-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7f44-131">INPUTS</span></span>

### <span data-ttu-id="a7f44-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a7f44-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a7f44-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a7f44-133">System.String</span></span>

## <span data-ttu-id="a7f44-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7f44-134">OUTPUTS</span></span>

### <span data-ttu-id="a7f44-135">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a7f44-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a7f44-136">Note</span><span class="sxs-lookup"><span data-stu-id="a7f44-136">NOTES</span></span>

## <span data-ttu-id="a7f44-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7f44-137">RELATED LINKS</span></span>

[<span data-ttu-id="a7f44-138">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a7f44-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
