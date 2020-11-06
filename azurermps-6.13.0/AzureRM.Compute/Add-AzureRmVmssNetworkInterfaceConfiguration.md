---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 6789b2a0f3309e8011cc6e87a27dbf9f28579d05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515496"
---
# <span data-ttu-id="ee219-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee219-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="ee219-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee219-102">SYNOPSIS</span></span>
<span data-ttu-id="ee219-103">Aggiunge una configurazione di interfaccia di rete a VMSS.</span><span class="sxs-lookup"><span data-stu-id="ee219-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee219-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee219-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-EnableIPForwarding] [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee219-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee219-105">DESCRIPTION</span></span>
<span data-ttu-id="ee219-106">Il cmdlet **Add-AzureRmVmssNetworkInterfaceConfiguration** aggiunge una configurazione di interfaccia di rete al set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ee219-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ee219-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee219-107">EXAMPLES</span></span>

### <span data-ttu-id="ee219-108">Esempio 1: aggiungere una configurazione di interfaccia di rete a VMSS</span><span class="sxs-lookup"><span data-stu-id="ee219-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="ee219-109">Questo comando aggiunge una configurazione di interfaccia di rete a VMSS.</span><span class="sxs-lookup"><span data-stu-id="ee219-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="ee219-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee219-110">PARAMETERS</span></span>

### <span data-ttu-id="ee219-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee219-111">-DefaultProfile</span></span>
<span data-ttu-id="ee219-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee219-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee219-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="ee219-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="ee219-114">Elenco di indirizzi IP del server DNS per le impostazioni DNS.</span><span class="sxs-lookup"><span data-stu-id="ee219-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="ee219-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="ee219-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="ee219-116">Specifica se l'interfaccia di rete è abilitata per l'accelerazione della rete.</span><span class="sxs-lookup"><span data-stu-id="ee219-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="ee219-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="ee219-117">-EnableIPForwarding</span></span>
<span data-ttu-id="ee219-118">Specifica se l'inoltro IP è abilitato in questa scheda di scelta.</span><span class="sxs-lookup"><span data-stu-id="ee219-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="ee219-119">-ID</span><span class="sxs-lookup"><span data-stu-id="ee219-119">-Id</span></span>
<span data-ttu-id="ee219-120">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ee219-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="ee219-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee219-121">-IpConfiguration</span></span>
<span data-ttu-id="ee219-122">Specifica le configurazioni IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="ee219-122">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="ee219-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee219-123">-Name</span></span>
<span data-ttu-id="ee219-124">Specifica il nome della configurazione dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="ee219-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="ee219-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ee219-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="ee219-126">ID del gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="ee219-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="ee219-127">-Primaria</span><span class="sxs-lookup"><span data-stu-id="ee219-127">-Primary</span></span>
<span data-ttu-id="ee219-128">Indica se le interfacce di rete create dalla configurazione dell'interfaccia di rete saranno il centro informazioni di rete principale (NIC) della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ee219-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="ee219-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ee219-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ee219-130">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="ee219-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="ee219-131">Puoi usare il cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ee219-131">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="ee219-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ee219-132">-Confirm</span></span>
<span data-ttu-id="ee219-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee219-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee219-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee219-134">-WhatIf</span></span>
<span data-ttu-id="ee219-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee219-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee219-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee219-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee219-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee219-137">CommonParameters</span></span>
<span data-ttu-id="ee219-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee219-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee219-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee219-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee219-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee219-140">INPUTS</span></span>

### <span data-ttu-id="ee219-141">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ee219-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="ee219-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ee219-142">System.String</span></span>

### <span data-ttu-id="ee219-143">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ee219-143">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ee219-144">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="ee219-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="ee219-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="ee219-145">System.String[]</span></span>

## <span data-ttu-id="ee219-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee219-146">OUTPUTS</span></span>

### <span data-ttu-id="ee219-147">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ee219-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ee219-148">Note</span><span class="sxs-lookup"><span data-stu-id="ee219-148">NOTES</span></span>

## <span data-ttu-id="ee219-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee219-149">RELATED LINKS</span></span>

[<span data-ttu-id="ee219-150">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ee219-150">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
