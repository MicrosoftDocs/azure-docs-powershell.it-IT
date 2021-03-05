---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: b8a38bd16fcd08104f678752d03dbc4a6d1f054b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003485"
---
# <span data-ttu-id="1c2e7-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c2e7-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="1c2e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c2e7-102">SYNOPSIS</span></span>
<span data-ttu-id="1c2e7-103">Modifica una configurazione IP per un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="1c2e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c2e7-104">SYNTAX</span></span>

### <span data-ttu-id="1c2e7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1c2e7-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c2e7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1c2e7-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c2e7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1c2e7-107">DESCRIPTION</span></span>
<span data-ttu-id="1c2e7-108">Il cmdlet **Set-AzApplicationGatewayIPConfiguration** modifica una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="1c2e7-109">Una configurazione IP contiene la subnet in cui è distribuito un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="1c2e7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c2e7-110">EXAMPLES</span></span>

### <span data-ttu-id="1c2e7-111">Esempio 1: Aggiornare una configurazione IP per un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="1c2e7-111">Example 1: Update an IP configuration for an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="1c2e7-112">Il primo comando recupera la rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e la archivia nella $VNet variabile.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="1c2e7-113">Il secondo comando recupera la configurazione subnet denominata Subnet01 $VNet e la archivia nella variabile $Subnet locale.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="1c2e7-114">Il terzo comando ottiene un gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1c2e7-115">Il forth comando imposta la configurazione IP del gateway applicazione archiviato in $AppGw sulla configurazione subnet archiviata in $Subnet.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="1c2e7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c2e7-116">PARAMETERS</span></span>

### <span data-ttu-id="1c2e7-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1c2e7-117">-ApplicationGateway</span></span>
<span data-ttu-id="1c2e7-118">Specifica un oggetto gateway applicazione a cui questo cmdlet associa una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c2e7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c2e7-119">-DefaultProfile</span></span>
<span data-ttu-id="1c2e7-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c2e7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1c2e7-121">-Name</span></span>
<span data-ttu-id="1c2e7-122">Specifica il nome della configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-122">Specifies the name of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c2e7-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="1c2e7-123">-Subnet</span></span>
<span data-ttu-id="1c2e7-124">Specifica la subnet.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-124">Specifies the subnet.</span></span>
<span data-ttu-id="1c2e7-125">Si tratta della subnet in cui viene distribuito il gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-125">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c2e7-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1c2e7-126">-SubnetId</span></span>
<span data-ttu-id="1c2e7-127">Specifica l'ID subnet.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="1c2e7-128">Si tratta della subnet in cui viene distribuito il gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-128">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c2e7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c2e7-129">CommonParameters</span></span>
<span data-ttu-id="1c2e7-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c2e7-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c2e7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c2e7-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="1c2e7-132">INPUTS</span></span>

### <span data-ttu-id="1c2e7-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1c2e7-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1c2e7-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c2e7-134">OUTPUTS</span></span>

### <span data-ttu-id="1c2e7-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1c2e7-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1c2e7-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="1c2e7-136">NOTES</span></span>

## <span data-ttu-id="1c2e7-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c2e7-137">RELATED LINKS</span></span>

[<span data-ttu-id="1c2e7-138">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c2e7-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="1c2e7-139">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c2e7-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="1c2e7-140">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c2e7-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="1c2e7-141">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c2e7-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="1c2e7-142">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c2e7-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


