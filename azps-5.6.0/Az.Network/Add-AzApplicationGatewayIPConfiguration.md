---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 17661a05a970a9661543220c35b122638ddbc524
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982621"
---
# <span data-ttu-id="10478-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="10478-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="10478-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10478-102">SYNOPSIS</span></span>
<span data-ttu-id="10478-103">Aggiunge una configurazione IP a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="10478-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="10478-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10478-104">SYNTAX</span></span>

### <span data-ttu-id="10478-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="10478-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10478-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="10478-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10478-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="10478-107">DESCRIPTION</span></span>
<span data-ttu-id="10478-108">Il cmdlet **Add-AzApplicationGatewayIPConfiguration aggiunge** una configurazione IP a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="10478-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="10478-109">Le configurazioni IP contengono la subnet in cui viene distribuito il gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="10478-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="10478-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10478-110">EXAMPLES</span></span>

### <span data-ttu-id="10478-111">Esempio 1: Aggiungere una configurazione di rete virtuale a un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="10478-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="10478-112">Il primo comando ottiene una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="10478-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="10478-113">Il secondo comando ottiene una subnet usando la rete virtuale creata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="10478-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="10478-114">Il terzo comando recupera il gateway applicazione e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="10478-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="10478-115">Il quarto comando aggiunge la configurazione IP al gateway applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="10478-115">The fourth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="10478-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10478-116">PARAMETERS</span></span>

### <span data-ttu-id="10478-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10478-117">-ApplicationGateway</span></span>
<span data-ttu-id="10478-118">Specifica il gateway applicazione a cui questo cmdlet aggiunge una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="10478-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="10478-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10478-119">-DefaultProfile</span></span>
<span data-ttu-id="10478-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="10478-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10478-121">-Name</span><span class="sxs-lookup"><span data-stu-id="10478-121">-Name</span></span>
<span data-ttu-id="10478-122">Specifica il nome della configurazione IP da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="10478-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="10478-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="10478-123">-Subnet</span></span>
<span data-ttu-id="10478-124">Specifica una subnet.</span><span class="sxs-lookup"><span data-stu-id="10478-124">Specifies a subnet.</span></span>
<span data-ttu-id="10478-125">Si tratta della subnet in cui viene distribuito il gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="10478-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="10478-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="10478-126">-SubnetId</span></span>
<span data-ttu-id="10478-127">Specifica un ID subnet.</span><span class="sxs-lookup"><span data-stu-id="10478-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="10478-128">Si tratta della subnet in cui viene distribuito il gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="10478-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="10478-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10478-129">CommonParameters</span></span>
<span data-ttu-id="10478-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10478-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10478-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10478-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10478-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="10478-132">INPUTS</span></span>

### <span data-ttu-id="10478-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10478-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="10478-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10478-134">OUTPUTS</span></span>

### <span data-ttu-id="10478-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10478-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="10478-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="10478-136">NOTES</span></span>

## <span data-ttu-id="10478-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10478-137">RELATED LINKS</span></span>

[<span data-ttu-id="10478-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="10478-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="10478-139">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="10478-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="10478-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="10478-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="10478-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="10478-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


