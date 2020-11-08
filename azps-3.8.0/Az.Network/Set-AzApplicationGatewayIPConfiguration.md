---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4b3a3303e8ade93b5c6945dae7650f7a9d16bbff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019307"
---
# <span data-ttu-id="f34d2-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f34d2-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="f34d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f34d2-102">SYNOPSIS</span></span>
<span data-ttu-id="f34d2-103">Modifica una configurazione IP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f34d2-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="f34d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f34d2-104">SYNTAX</span></span>

### <span data-ttu-id="f34d2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f34d2-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f34d2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f34d2-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f34d2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f34d2-107">DESCRIPTION</span></span>
<span data-ttu-id="f34d2-108">Il cmdlet **set-AzApplicationGatewayIPConfiguration** modifica una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="f34d2-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="f34d2-109">Una configurazione IP contiene la subnet in cui è distribuito un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f34d2-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="f34d2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f34d2-110">EXAMPLES</span></span>

### <span data-ttu-id="f34d2-111">Esempio 1: aggiornare una configurazione IP per un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="f34d2-111">Example 1: Update an IP configuration for an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="f34d2-112">Il primo comando consente di ottenere la rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $VNet.</span><span class="sxs-lookup"><span data-stu-id="f34d2-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="f34d2-113">Il secondo comando ottiene la configurazione della subnet denominata Subnet01 usando $VNet e la archivia nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="f34d2-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="f34d2-114">Il terzo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f34d2-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f34d2-115">Il comando Forth imposta la configurazione IP del gateway dell'applicazione archiviato in $AppGw alla configurazione della subnet archiviata in $Subnet.</span><span class="sxs-lookup"><span data-stu-id="f34d2-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="f34d2-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f34d2-116">PARAMETERS</span></span>

### <span data-ttu-id="f34d2-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f34d2-117">-ApplicationGateway</span></span>
<span data-ttu-id="f34d2-118">Specifica un oggetto gateway dell'applicazione con cui questo cmdlet associa una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="f34d2-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="f34d2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f34d2-119">-DefaultProfile</span></span>
<span data-ttu-id="f34d2-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f34d2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f34d2-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f34d2-121">-Name</span></span>
<span data-ttu-id="f34d2-122">Specifica il nome della configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="f34d2-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="f34d2-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="f34d2-123">-Subnet</span></span>
<span data-ttu-id="f34d2-124">Specifica la subnet.</span><span class="sxs-lookup"><span data-stu-id="f34d2-124">Specifies the subnet.</span></span>
<span data-ttu-id="f34d2-125">Questa è la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f34d2-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="f34d2-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f34d2-126">-SubnetId</span></span>
<span data-ttu-id="f34d2-127">Specifica l'ID subnet.</span><span class="sxs-lookup"><span data-stu-id="f34d2-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="f34d2-128">Questa è la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f34d2-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="f34d2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f34d2-129">CommonParameters</span></span>
<span data-ttu-id="f34d2-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f34d2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f34d2-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f34d2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f34d2-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f34d2-132">INPUTS</span></span>

### <span data-ttu-id="f34d2-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f34d2-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f34d2-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f34d2-134">OUTPUTS</span></span>

### <span data-ttu-id="f34d2-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f34d2-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f34d2-136">Note</span><span class="sxs-lookup"><span data-stu-id="f34d2-136">NOTES</span></span>

## <span data-ttu-id="f34d2-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f34d2-137">RELATED LINKS</span></span>

[<span data-ttu-id="f34d2-138">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f34d2-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f34d2-139">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f34d2-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f34d2-140">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f34d2-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f34d2-141">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f34d2-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f34d2-142">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f34d2-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


