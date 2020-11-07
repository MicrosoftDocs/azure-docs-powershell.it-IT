---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 0b21b5fa3b5b605ee3092a61eaf67a2c63c4346b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685499"
---
# <span data-ttu-id="cd50a-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd50a-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="cd50a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd50a-102">SYNOPSIS</span></span>
<span data-ttu-id="cd50a-103">Aggiunge una configurazione di interfaccia di rete a VMSS.</span><span class="sxs-lookup"><span data-stu-id="cd50a-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd50a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd50a-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd50a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd50a-105">DESCRIPTION</span></span>
<span data-ttu-id="cd50a-106">Il cmdlet **Add-AzureRmVmssNetworkInterfaceConfiguration** aggiunge una configurazione di interfaccia di rete al set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="cd50a-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="cd50a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd50a-107">EXAMPLES</span></span>

### <span data-ttu-id="cd50a-108">Esempio 1: aggiungere una configurazione di interfaccia di rete a VMSS</span><span class="sxs-lookup"><span data-stu-id="cd50a-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="cd50a-109">Questo comando aggiunge una configurazione di interfaccia di rete a VMSS.</span><span class="sxs-lookup"><span data-stu-id="cd50a-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="cd50a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd50a-110">PARAMETERS</span></span>

### <span data-ttu-id="cd50a-111">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="cd50a-111">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="cd50a-112">Elenco di indirizzi IP del server DNS per le impostazioni DNS.</span><span class="sxs-lookup"><span data-stu-id="cd50a-112">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd50a-113">-ID</span><span class="sxs-lookup"><span data-stu-id="cd50a-113">-Id</span></span>
<span data-ttu-id="cd50a-114">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cd50a-114">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="cd50a-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd50a-115">-IpConfiguration</span></span>
<span data-ttu-id="cd50a-116">Specifica le configurazioni IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="cd50a-116">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="cd50a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd50a-117">-Name</span></span>
<span data-ttu-id="cd50a-118">Specifica il nome della configurazione dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="cd50a-118">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="cd50a-119">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="cd50a-119">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="cd50a-120">ID del gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="cd50a-120">Id of the network security group.</span></span>

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

### <span data-ttu-id="cd50a-121">-Primaria</span><span class="sxs-lookup"><span data-stu-id="cd50a-121">-Primary</span></span>
<span data-ttu-id="cd50a-122">Indica se le interfacce di rete create dalla configurazione dell'interfaccia di rete saranno il centro informazioni di rete principale (NIC) della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cd50a-122">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="cd50a-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cd50a-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="cd50a-124">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="cd50a-124">Specifies the VMSS object.</span></span>
<span data-ttu-id="cd50a-125">Puoi usare il cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd50a-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd50a-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd50a-126">-Confirm</span></span>
<span data-ttu-id="cd50a-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd50a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd50a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd50a-128">-WhatIf</span></span>
<span data-ttu-id="cd50a-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd50a-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd50a-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd50a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd50a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd50a-131">CommonParameters</span></span>
<span data-ttu-id="cd50a-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd50a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd50a-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd50a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd50a-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd50a-134">INPUTS</span></span>

### <span data-ttu-id="cd50a-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cd50a-135">None</span></span>
<span data-ttu-id="cd50a-136">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="cd50a-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cd50a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd50a-137">OUTPUTS</span></span>

###  
<span data-ttu-id="cd50a-138">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="cd50a-138">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="cd50a-139">Note</span><span class="sxs-lookup"><span data-stu-id="cd50a-139">NOTES</span></span>

## <span data-ttu-id="cd50a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd50a-140">RELATED LINKS</span></span>

[<span data-ttu-id="cd50a-141">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cd50a-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
