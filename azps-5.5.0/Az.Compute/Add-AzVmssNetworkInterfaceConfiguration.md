---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 9e52131bd5f53d48b4c958c26a0ef37b5ebd23ec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181743"
---
# <span data-ttu-id="becf1-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="becf1-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="becf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="becf1-102">SYNOPSIS</span></span>
<span data-ttu-id="becf1-103">Aggiunge una configurazione dell'interfaccia di rete al sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="becf1-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="becf1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="becf1-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Primary] <Boolean>] [[-Id] <String>] [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>]
 [-EnableAcceleratedNetworking] [-EnableIPForwarding] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="becf1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="becf1-105">DESCRIPTION</span></span>
<span data-ttu-id="becf1-106">Il cmdlet **Add-AzVmssNetworkInterfaceConfiguration** aggiunge una configurazione dell'interfaccia di rete al set di scalabilità delle macchine virtuali (VMSS).</span><span class="sxs-lookup"><span data-stu-id="becf1-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="becf1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="becf1-107">EXAMPLES</span></span>

### <span data-ttu-id="becf1-108">Esempio 1: Aggiungere una configurazione dell'interfaccia di rete al sistema VMSS</span><span class="sxs-lookup"><span data-stu-id="becf1-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="becf1-109">Questo comando aggiunge una configurazione dell'interfaccia di rete al sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="becf1-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="becf1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="becf1-110">PARAMETERS</span></span>

### <span data-ttu-id="becf1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="becf1-111">-DefaultProfile</span></span>
<span data-ttu-id="becf1-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="becf1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="becf1-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="becf1-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="becf1-114">Elenco di indirizzi IP del server DNS per le impostazioni DNS.</span><span class="sxs-lookup"><span data-stu-id="becf1-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="becf1-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="becf1-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="becf1-116">Specifica se l'interfaccia di rete è accelerata e abilitata per la rete.</span><span class="sxs-lookup"><span data-stu-id="becf1-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="becf1-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="becf1-117">-EnableIPForwarding</span></span>
<span data-ttu-id="becf1-118">Specifica se l'inoltro IP è abilitato su questa scheda NIC.</span><span class="sxs-lookup"><span data-stu-id="becf1-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="becf1-119">-Id</span><span class="sxs-lookup"><span data-stu-id="becf1-119">-Id</span></span>
<span data-ttu-id="becf1-120">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="becf1-120">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="becf1-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="becf1-121">-IpConfiguration</span></span>
<span data-ttu-id="becf1-122">Specifica le configurazioni IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="becf1-122">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="becf1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="becf1-123">-Name</span></span>
<span data-ttu-id="becf1-124">Specifica il nome della configurazione dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="becf1-124">Specifies the name of the network interface configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="becf1-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="becf1-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="becf1-126">ID del gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="becf1-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="becf1-127">-Principale</span><span class="sxs-lookup"><span data-stu-id="becf1-127">-Primary</span></span>
<span data-ttu-id="becf1-128">Indica se le interfacce di rete create dalla configurazione dell'interfaccia di rete saranno il network information center (NIC) principale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="becf1-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="becf1-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="becf1-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="becf1-130">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="becf1-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="becf1-131">È possibile usare il cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="becf1-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="becf1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="becf1-132">-Confirm</span></span>
<span data-ttu-id="becf1-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="becf1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="becf1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="becf1-134">-WhatIf</span></span>
<span data-ttu-id="becf1-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="becf1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="becf1-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="becf1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="becf1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="becf1-137">CommonParameters</span></span>
<span data-ttu-id="becf1-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="becf1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="becf1-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="becf1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="becf1-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="becf1-140">INPUTS</span></span>

### <span data-ttu-id="becf1-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="becf1-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="becf1-142">System.String</span><span class="sxs-lookup"><span data-stu-id="becf1-142">System.String</span></span>

### <span data-ttu-id="becf1-143">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="becf1-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="becf1-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="becf1-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="becf1-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="becf1-145">System.String[]</span></span>

## <span data-ttu-id="becf1-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="becf1-146">OUTPUTS</span></span>

### <span data-ttu-id="becf1-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="becf1-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="becf1-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="becf1-148">NOTES</span></span>

## <span data-ttu-id="becf1-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="becf1-149">RELATED LINKS</span></span>

[<span data-ttu-id="becf1-150">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="becf1-150">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
