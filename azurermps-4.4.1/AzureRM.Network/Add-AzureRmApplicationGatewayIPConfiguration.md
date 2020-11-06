---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 98e2249c3577d49a140d31b4287507e0e46185f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520047"
---
# <span data-ttu-id="0c5ce-101">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c5ce-101">Add-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="0c5ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c5ce-102">SYNOPSIS</span></span>
<span data-ttu-id="0c5ce-103">Aggiunge una configurazione IP a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0c5ce-103">Adds an IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c5ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c5ce-104">SYNTAX</span></span>

### <span data-ttu-id="0c5ce-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0c5ce-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c5ce-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0c5ce-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c5ce-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c5ce-107">DESCRIPTION</span></span>
<span data-ttu-id="0c5ce-108">Il cmdlet **Add-AzureRmApplicationGatewayIPConfiguration** aggiunge una configurazione IP a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0c5ce-108">The **Add-AzureRmApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="0c5ce-109">Le configurazioni IP contengono la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0c5ce-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="0c5ce-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c5ce-110">EXAMPLES</span></span>

### <span data-ttu-id="0c5ce-111">Esempio 1: aggiungere una configurazione di rete virtuale a un gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="0c5ce-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzureRmVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="0c5ce-112">Il primo comando crea una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0c5ce-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="0c5ce-113">Il secondo comando crea una subnet usando la rete virtuale creata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="0c5ce-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="0c5ce-114">Il terzo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0c5ce-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0c5ce-115">Il comando quarto aggiunge la configurazione IP al gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0c5ce-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="0c5ce-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c5ce-116">PARAMETERS</span></span>

### <span data-ttu-id="0c5ce-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c5ce-117">-ApplicationGateway</span></span>
<span data-ttu-id="0c5ce-118">Specifica il gateway dell'applicazione a cui questo cmdlet aggiunge una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="0c5ce-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="0c5ce-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c5ce-119">-Name</span></span>
<span data-ttu-id="0c5ce-120">Specifica il nome della configurazione IP da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="0c5ce-120">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="0c5ce-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="0c5ce-121">-Subnet</span></span>
<span data-ttu-id="0c5ce-122">Specifica una subnet.</span><span class="sxs-lookup"><span data-stu-id="0c5ce-122">Specifies a subnet.</span></span>
<span data-ttu-id="0c5ce-123">Questa è la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0c5ce-123">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="0c5ce-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0c5ce-124">-SubnetId</span></span>
<span data-ttu-id="0c5ce-125">Specifica un ID subnet.</span><span class="sxs-lookup"><span data-stu-id="0c5ce-125">Specifies a subnet ID.</span></span>
<span data-ttu-id="0c5ce-126">Questa è la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0c5ce-126">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="0c5ce-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c5ce-127">-DefaultProfile</span></span>
<span data-ttu-id="0c5ce-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c5ce-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c5ce-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c5ce-129">CommonParameters</span></span>
<span data-ttu-id="0c5ce-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c5ce-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c5ce-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c5ce-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c5ce-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c5ce-132">INPUTS</span></span>

### <span data-ttu-id="0c5ce-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0c5ce-133">System.String</span></span>

## <span data-ttu-id="0c5ce-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c5ce-134">OUTPUTS</span></span>

### <span data-ttu-id="0c5ce-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c5ce-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0c5ce-136">Note</span><span class="sxs-lookup"><span data-stu-id="0c5ce-136">NOTES</span></span>

## <span data-ttu-id="0c5ce-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c5ce-137">RELATED LINKS</span></span>

[<span data-ttu-id="0c5ce-138">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c5ce-138">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="0c5ce-139">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c5ce-139">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="0c5ce-140">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c5ce-140">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="0c5ce-141">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c5ce-141">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


