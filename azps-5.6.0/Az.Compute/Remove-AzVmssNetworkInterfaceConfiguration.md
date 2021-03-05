---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 3c9e19c30d89d73a52be4defd18166f88b700889
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986942"
---
# <span data-ttu-id="c8811-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8811-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="c8811-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8811-102">SYNOPSIS</span></span>
<span data-ttu-id="c8811-103">Rimuove una configurazione dell'interfaccia di rete da un sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="c8811-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="c8811-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8811-104">SYNTAX</span></span>

### <span data-ttu-id="c8811-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8811-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8811-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8811-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8811-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c8811-107">DESCRIPTION</span></span>
<span data-ttu-id="c8811-108">Il cmdlet **Remove-AzVmssNetworkInterfaceConfiguration** rimuove una configurazione dell'interfaccia di rete da un set di scalabilità delle macchine virtuali (VMSS).</span><span class="sxs-lookup"><span data-stu-id="c8811-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="c8811-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8811-109">EXAMPLES</span></span>

### <span data-ttu-id="c8811-110">Esempio 1: Rimuovere una configurazione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="c8811-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="c8811-111">Il primo comando ottiene un VMSS usando il cmdlet Get-AzVmss, quindi lo archivia nella $VMSS variabile.</span><span class="sxs-lookup"><span data-stu-id="c8811-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="c8811-112">Il secondo comando rimuove la configurazione dell'interfaccia di rete denominata ContosoVmssInterface02 dal set in $VMSS.</span><span class="sxs-lookup"><span data-stu-id="c8811-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="c8811-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8811-113">PARAMETERS</span></span>

### <span data-ttu-id="c8811-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8811-114">-DefaultProfile</span></span>
<span data-ttu-id="c8811-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8811-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8811-116">-Id</span><span class="sxs-lookup"><span data-stu-id="c8811-116">-Id</span></span>
<span data-ttu-id="c8811-117">Specifica l'ID della configurazione dell'interfaccia di rete rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8811-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c8811-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c8811-118">-Name</span></span>
<span data-ttu-id="c8811-119">Specifica il nome della configurazione dell'interfaccia di rete rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8811-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c8811-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c8811-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c8811-121">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="c8811-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="c8811-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8811-122">-Confirm</span></span>
<span data-ttu-id="c8811-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8811-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8811-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8811-124">-WhatIf</span></span>
<span data-ttu-id="c8811-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8811-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8811-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8811-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8811-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8811-127">CommonParameters</span></span>
<span data-ttu-id="c8811-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8811-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8811-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c8811-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8811-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="c8811-130">INPUTS</span></span>

### <span data-ttu-id="c8811-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c8811-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="c8811-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c8811-132">System.String</span></span>

## <span data-ttu-id="c8811-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8811-133">OUTPUTS</span></span>

### <span data-ttu-id="c8811-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c8811-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c8811-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="c8811-135">NOTES</span></span>

## <span data-ttu-id="c8811-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8811-136">RELATED LINKS</span></span>

[<span data-ttu-id="c8811-137">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8811-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="c8811-138">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c8811-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


