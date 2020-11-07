---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 43d7040543beb049f46fce45cab69d9128a8954e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863862"
---
# <span data-ttu-id="a93e0-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a93e0-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="a93e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a93e0-102">SYNOPSIS</span></span>
<span data-ttu-id="a93e0-103">Aggiunge una configurazione di interfaccia di rete a VMSS.</span><span class="sxs-lookup"><span data-stu-id="a93e0-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="a93e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a93e0-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-EnableIPForwarding] [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a93e0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a93e0-105">DESCRIPTION</span></span>
<span data-ttu-id="a93e0-106">Il cmdlet **Add-AzVmssNetworkInterfaceConfiguration** aggiunge una configurazione di interfaccia di rete al set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a93e0-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a93e0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a93e0-107">EXAMPLES</span></span>

### <span data-ttu-id="a93e0-108">Esempio 1: aggiungere una configurazione di interfaccia di rete a VMSS</span><span class="sxs-lookup"><span data-stu-id="a93e0-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="a93e0-109">Questo comando aggiunge una configurazione di interfaccia di rete a VMSS.</span><span class="sxs-lookup"><span data-stu-id="a93e0-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="a93e0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a93e0-110">PARAMETERS</span></span>

### <span data-ttu-id="a93e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a93e0-111">-DefaultProfile</span></span>
<span data-ttu-id="a93e0-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a93e0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93e0-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="a93e0-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="a93e0-114">Elenco di indirizzi IP del server DNS per le impostazioni DNS.</span><span class="sxs-lookup"><span data-stu-id="a93e0-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93e0-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="a93e0-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="a93e0-116">Specifica se l'interfaccia di rete è abilitata per l'accelerazione della rete.</span><span class="sxs-lookup"><span data-stu-id="a93e0-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93e0-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="a93e0-117">-EnableIPForwarding</span></span>
<span data-ttu-id="a93e0-118">Specifica se l'inoltro IP è abilitato in questa scheda di scelta.</span><span class="sxs-lookup"><span data-stu-id="a93e0-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93e0-119">-ID</span><span class="sxs-lookup"><span data-stu-id="a93e0-119">-Id</span></span>
<span data-ttu-id="a93e0-120">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a93e0-120">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93e0-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a93e0-121">-IpConfiguration</span></span>
<span data-ttu-id="a93e0-122">Specifica le configurazioni IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="a93e0-122">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93e0-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="a93e0-123">-Name</span></span>
<span data-ttu-id="a93e0-124">Specifica il nome della configurazione dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="a93e0-124">Specifies the name of the network interface configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93e0-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a93e0-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="a93e0-126">ID del gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="a93e0-126">Id of the network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93e0-127">-Primaria</span><span class="sxs-lookup"><span data-stu-id="a93e0-127">-Primary</span></span>
<span data-ttu-id="a93e0-128">Indica se le interfacce di rete create dalla configurazione dell'interfaccia di rete saranno il centro informazioni di rete principale (NIC) della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a93e0-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93e0-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a93e0-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a93e0-130">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="a93e0-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="a93e0-131">Puoi usare il cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a93e0-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a93e0-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a93e0-132">-Confirm</span></span>
<span data-ttu-id="a93e0-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a93e0-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93e0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a93e0-134">-WhatIf</span></span>
<span data-ttu-id="a93e0-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a93e0-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a93e0-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a93e0-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93e0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93e0-137">CommonParameters</span></span>
<span data-ttu-id="a93e0-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a93e0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93e0-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a93e0-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93e0-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a93e0-140">INPUTS</span></span>

### <span data-ttu-id="a93e0-141">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a93e0-141">VirtualMachineScaleSet</span></span>
<span data-ttu-id="a93e0-142">Il parametro ' VirtualMachineScaleSet ' accetta il valore di tipo ' VirtualMachineScaleSet ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a93e0-142">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="a93e0-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a93e0-143">OUTPUTS</span></span>

###  
<span data-ttu-id="a93e0-144">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a93e0-144">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a93e0-145">Note</span><span class="sxs-lookup"><span data-stu-id="a93e0-145">NOTES</span></span>

## <span data-ttu-id="a93e0-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a93e0-146">RELATED LINKS</span></span>

[<span data-ttu-id="a93e0-147">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a93e0-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
