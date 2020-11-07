---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 31790ead292c9146aa73f41c56e79f3bdf51c715
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860950"
---
# <span data-ttu-id="293a5-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="293a5-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="293a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="293a5-102">SYNOPSIS</span></span>
<span data-ttu-id="293a5-103">Aggiunge una configurazione IP a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="293a5-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="293a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="293a5-104">SYNTAX</span></span>

### <span data-ttu-id="293a5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="293a5-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="293a5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="293a5-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="293a5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="293a5-107">DESCRIPTION</span></span>
<span data-ttu-id="293a5-108">Il cmdlet **Add-AzVirtualNetworkGatewayIpConfig** aggiunge una configurazione IP a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="293a5-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="293a5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="293a5-109">EXAMPLES</span></span>

### <span data-ttu-id="293a5-110">1:</span><span class="sxs-lookup"><span data-stu-id="293a5-110">1:</span></span>
```

```

## <span data-ttu-id="293a5-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="293a5-111">PARAMETERS</span></span>

### <span data-ttu-id="293a5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="293a5-112">-DefaultProfile</span></span>
<span data-ttu-id="293a5-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="293a5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="293a5-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="293a5-114">-Name</span></span>
<span data-ttu-id="293a5-115">Specifica il nome della configurazione IP del gateway da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="293a5-115">Specifies the name of the gateway IP configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293a5-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="293a5-116">-PrivateIpAddress</span></span>
<span data-ttu-id="293a5-117">Specifica l'indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="293a5-117">Specifies the private IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293a5-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="293a5-118">-PublicIpAddress</span></span>
<span data-ttu-id="293a5-119">Specifica l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="293a5-119">Specifies the public IP address.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293a5-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="293a5-120">-PublicIpAddressId</span></span>
<span data-ttu-id="293a5-121">Specifica l'ID dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="293a5-121">Specifies the ID of the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293a5-122">-Subnet</span><span class="sxs-lookup"><span data-stu-id="293a5-122">-Subnet</span></span>
<span data-ttu-id="293a5-123">Specifica un oggetto **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="293a5-123">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293a5-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="293a5-124">-SubnetId</span></span>
<span data-ttu-id="293a5-125">Specifica l'ID della subnet.</span><span class="sxs-lookup"><span data-stu-id="293a5-125">Specifies the ID of the subnet.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293a5-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="293a5-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="293a5-127">Specifica un oggetto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="293a5-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="293a5-128">Questo cmdlet modifica l'oggetto **PSVirtualNetworkGateway** specificato.</span><span class="sxs-lookup"><span data-stu-id="293a5-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="293a5-129">Puoi usare il cmdlet Get-AzVirtualNetworkGateway per recuperare un oggetto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="293a5-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="293a5-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="293a5-130">-Confirm</span></span>
<span data-ttu-id="293a5-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="293a5-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293a5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="293a5-132">-WhatIf</span></span>
<span data-ttu-id="293a5-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="293a5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="293a5-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="293a5-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293a5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="293a5-135">CommonParameters</span></span>
<span data-ttu-id="293a5-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="293a5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="293a5-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="293a5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="293a5-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="293a5-138">INPUTS</span></span>

### <span data-ttu-id="293a5-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="293a5-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="293a5-140">Il parametro ' VirtualNetworkGateway ' accetta il valore di tipo ' PSVirtualNetworkGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="293a5-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="293a5-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="293a5-141">OUTPUTS</span></span>

### <span data-ttu-id="293a5-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="293a5-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="293a5-143">Note</span><span class="sxs-lookup"><span data-stu-id="293a5-143">NOTES</span></span>

## <span data-ttu-id="293a5-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="293a5-144">RELATED LINKS</span></span>

[<span data-ttu-id="293a5-145">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="293a5-145">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="293a5-146">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="293a5-146">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="293a5-147">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="293a5-147">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)


