---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: 340baa4b7a7d0afaf0e0523cb8c2f14f8270bf7c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867077"
---
# <span data-ttu-id="7e6d4-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e6d4-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="7e6d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e6d4-102">SYNOPSIS</span></span>
<span data-ttu-id="7e6d4-103">Aggiunge una configurazione IP a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e6d4-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e6d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e6d4-104">SYNTAX</span></span>

### <span data-ttu-id="7e6d4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7e6d4-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e6d4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7e6d4-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e6d4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e6d4-107">DESCRIPTION</span></span>
<span data-ttu-id="7e6d4-108">Il cmdlet **Add-AzureRmVirtualNetworkGatewayIpConfig** aggiunge una configurazione IP a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e6d4-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="7e6d4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e6d4-109">EXAMPLES</span></span>

### <span data-ttu-id="7e6d4-110">1:</span><span class="sxs-lookup"><span data-stu-id="7e6d4-110">1:</span></span>
```

```

## <span data-ttu-id="7e6d4-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e6d4-111">PARAMETERS</span></span>

### <span data-ttu-id="7e6d4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e6d4-112">-DefaultProfile</span></span>
<span data-ttu-id="7e6d4-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e6d4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e6d4-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e6d4-114">-Name</span></span>
<span data-ttu-id="7e6d4-115">Specifica il nome della configurazione IP del gateway da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="7e6d4-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="7e6d4-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7e6d4-116">-PrivateIpAddress</span></span>
<span data-ttu-id="7e6d4-117">Specifica l'indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="7e6d4-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="7e6d4-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7e6d4-118">-PublicIpAddress</span></span>
<span data-ttu-id="7e6d4-119">Specifica l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="7e6d4-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="7e6d4-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7e6d4-120">-PublicIpAddressId</span></span>
<span data-ttu-id="7e6d4-121">Specifica l'ID dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="7e6d4-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="7e6d4-122">-Subnet</span><span class="sxs-lookup"><span data-stu-id="7e6d4-122">-Subnet</span></span>
<span data-ttu-id="7e6d4-123">Specifica un oggetto **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="7e6d4-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="7e6d4-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7e6d4-124">-SubnetId</span></span>
<span data-ttu-id="7e6d4-125">Specifica l'ID della subnet.</span><span class="sxs-lookup"><span data-stu-id="7e6d4-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="7e6d4-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7e6d4-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="7e6d4-127">Specifica un oggetto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="7e6d4-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="7e6d4-128">Questo cmdlet modifica l'oggetto **PSVirtualNetworkGateway** specificato.</span><span class="sxs-lookup"><span data-stu-id="7e6d4-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="7e6d4-129">Puoi usare il cmdlet Get-AzureRmVirtualNetworkGateway per recuperare un oggetto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="7e6d4-129">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="7e6d4-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7e6d4-130">-Confirm</span></span>
<span data-ttu-id="7e6d4-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e6d4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e6d4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e6d4-132">-WhatIf</span></span>
<span data-ttu-id="7e6d4-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e6d4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e6d4-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e6d4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e6d4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e6d4-135">CommonParameters</span></span>
<span data-ttu-id="7e6d4-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e6d4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e6d4-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e6d4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e6d4-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e6d4-138">INPUTS</span></span>

### <span data-ttu-id="7e6d4-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7e6d4-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="7e6d4-140">Il parametro ' VirtualNetworkGateway ' accetta il valore di tipo ' PSVirtualNetworkGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7e6d4-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="7e6d4-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e6d4-141">OUTPUTS</span></span>

### <span data-ttu-id="7e6d4-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7e6d4-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7e6d4-143">Note</span><span class="sxs-lookup"><span data-stu-id="7e6d4-143">NOTES</span></span>

## <span data-ttu-id="7e6d4-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e6d4-144">RELATED LINKS</span></span>

[<span data-ttu-id="7e6d4-145">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7e6d4-145">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="7e6d4-146">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e6d4-146">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="7e6d4-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e6d4-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


