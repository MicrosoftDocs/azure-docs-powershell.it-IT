---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 4b157dfd7e7ac47a8161c9f36f9b52bbaaa61869
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511136"
---
# <span data-ttu-id="862e9-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="862e9-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="862e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="862e9-102">SYNOPSIS</span></span>
<span data-ttu-id="862e9-103">Aggiunge una configurazione IP a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="862e9-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="862e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="862e9-104">SYNTAX</span></span>

### <span data-ttu-id="862e9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="862e9-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862e9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="862e9-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="862e9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="862e9-107">DESCRIPTION</span></span>
<span data-ttu-id="862e9-108">Il cmdlet **Add-AzureRmVirtualNetworkGatewayIpConfig** aggiunge una configurazione IP a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="862e9-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="862e9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="862e9-109">EXAMPLES</span></span>

## <span data-ttu-id="862e9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="862e9-110">PARAMETERS</span></span>

### <span data-ttu-id="862e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="862e9-111">-DefaultProfile</span></span>
<span data-ttu-id="862e9-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="862e9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="862e9-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="862e9-113">-Name</span></span>
<span data-ttu-id="862e9-114">Specifica il nome della configurazione IP del gateway da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="862e9-114">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="862e9-115">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="862e9-115">-PrivateIpAddress</span></span>
<span data-ttu-id="862e9-116">Specifica l'indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="862e9-116">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="862e9-117">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="862e9-117">-PublicIpAddress</span></span>
<span data-ttu-id="862e9-118">Specifica l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="862e9-118">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="862e9-119">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="862e9-119">-PublicIpAddressId</span></span>
<span data-ttu-id="862e9-120">Specifica l'ID dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="862e9-120">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="862e9-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="862e9-121">-Subnet</span></span>
<span data-ttu-id="862e9-122">Specifica un oggetto **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="862e9-122">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="862e9-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="862e9-123">-SubnetId</span></span>
<span data-ttu-id="862e9-124">Specifica l'ID della subnet.</span><span class="sxs-lookup"><span data-stu-id="862e9-124">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="862e9-125">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="862e9-125">-VirtualNetworkGateway</span></span>
<span data-ttu-id="862e9-126">Specifica un oggetto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="862e9-126">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="862e9-127">Questo cmdlet modifica l'oggetto **PSVirtualNetworkGateway** specificato.</span><span class="sxs-lookup"><span data-stu-id="862e9-127">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="862e9-128">Puoi usare il cmdlet Get-AzureRmVirtualNetworkGateway per recuperare un oggetto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="862e9-128">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="862e9-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="862e9-129">-Confirm</span></span>
<span data-ttu-id="862e9-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="862e9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="862e9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="862e9-131">-WhatIf</span></span>
<span data-ttu-id="862e9-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="862e9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="862e9-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="862e9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="862e9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="862e9-134">CommonParameters</span></span>
<span data-ttu-id="862e9-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="862e9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="862e9-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="862e9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="862e9-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="862e9-137">INPUTS</span></span>

### <span data-ttu-id="862e9-138">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="862e9-138">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="862e9-139">Il parametro ' VirtualNetworkGateway ' accetta il valore di tipo ' PSVirtualNetworkGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="862e9-139">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="862e9-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="862e9-140">OUTPUTS</span></span>

### <span data-ttu-id="862e9-141">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="862e9-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="862e9-142">Note</span><span class="sxs-lookup"><span data-stu-id="862e9-142">NOTES</span></span>

## <span data-ttu-id="862e9-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="862e9-143">RELATED LINKS</span></span>

[<span data-ttu-id="862e9-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="862e9-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="862e9-145">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="862e9-145">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="862e9-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="862e9-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


