---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayipconfiguration
schema: 2.0.0
ms.openlocfilehash: d3a309d99dff493e2440618d87c20b1a543e2ed9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866034"
---
# <span data-ttu-id="4d06f-101">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d06f-101">Set-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="4d06f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d06f-102">SYNOPSIS</span></span>
<span data-ttu-id="4d06f-103">Modifica una configurazione IP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4d06f-103">Modifies an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d06f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d06f-104">SYNTAX</span></span>

### <span data-ttu-id="4d06f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4d06f-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d06f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4d06f-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d06f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d06f-107">DESCRIPTION</span></span>
<span data-ttu-id="4d06f-108">Il cmdlet **set-AzureRmApplicationGatewayIPConfiguration** modifica una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="4d06f-108">The **Set-AzureRmApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="4d06f-109">Una configurazione IP contiene la subnet in cui è distribuito un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4d06f-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="4d06f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d06f-110">EXAMPLES</span></span>

### <span data-ttu-id="4d06f-111">Esempio 1: impostare lo stato obiettivo di una configurazione IP</span><span class="sxs-lookup"><span data-stu-id="4d06f-111">Example 1: Set the goal state of an IP configuration</span></span>
```
PS C:\>$VNet = Get-AzureRmVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="4d06f-112">Il primo comando consente di ottenere la rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $VNet.</span><span class="sxs-lookup"><span data-stu-id="4d06f-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>

<span data-ttu-id="4d06f-113">Il secondo comando ottiene la configurazione della subnet denominata Subnet01 usando $VNet e la archivia nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="4d06f-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="4d06f-114">Il terzo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4d06f-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="4d06f-115">Il comando Forth imposta la configurazione IP del gateway dell'applicazione archiviato in $AppGw alla configurazione della subnet archiviata in $Subnet.</span><span class="sxs-lookup"><span data-stu-id="4d06f-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="4d06f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d06f-116">PARAMETERS</span></span>

### <span data-ttu-id="4d06f-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d06f-117">-ApplicationGateway</span></span>
<span data-ttu-id="4d06f-118">Specifica un oggetto gateway dell'applicazione con cui questo cmdlet associa una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="4d06f-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d06f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d06f-119">-DefaultProfile</span></span>
<span data-ttu-id="4d06f-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d06f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d06f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d06f-121">-Name</span></span>
<span data-ttu-id="4d06f-122">Specifica il nome della configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="4d06f-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="4d06f-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="4d06f-123">-Subnet</span></span>
<span data-ttu-id="4d06f-124">Specifica la subnet.</span><span class="sxs-lookup"><span data-stu-id="4d06f-124">Specifies the subnet.</span></span>
<span data-ttu-id="4d06f-125">Questa è la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4d06f-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="4d06f-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4d06f-126">-SubnetId</span></span>
<span data-ttu-id="4d06f-127">Specifica l'ID subnet.</span><span class="sxs-lookup"><span data-stu-id="4d06f-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="4d06f-128">Questa è la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4d06f-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="4d06f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d06f-129">CommonParameters</span></span>
<span data-ttu-id="4d06f-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d06f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d06f-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d06f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d06f-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d06f-132">INPUTS</span></span>

### <span data-ttu-id="4d06f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4d06f-133">System.String</span></span>

## <span data-ttu-id="4d06f-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d06f-134">OUTPUTS</span></span>

### <span data-ttu-id="4d06f-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d06f-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4d06f-136">Note</span><span class="sxs-lookup"><span data-stu-id="4d06f-136">NOTES</span></span>

## <span data-ttu-id="4d06f-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d06f-137">RELATED LINKS</span></span>

[<span data-ttu-id="4d06f-138">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d06f-138">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4d06f-139">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d06f-139">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4d06f-140">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d06f-140">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4d06f-141">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d06f-141">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4d06f-142">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d06f-142">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)


