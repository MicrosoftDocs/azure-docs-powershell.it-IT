---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: cc84daecf4c98a48bb37ff0edd38f1136960a273
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519429"
---
# <span data-ttu-id="56fab-101">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="56fab-101">Add-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="56fab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56fab-102">SYNOPSIS</span></span>
<span data-ttu-id="56fab-103">Aggiunge una configurazione IP a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="56fab-103">Adds an IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56fab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56fab-104">SYNTAX</span></span>

### <span data-ttu-id="56fab-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="56fab-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56fab-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="56fab-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56fab-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56fab-107">DESCRIPTION</span></span>
<span data-ttu-id="56fab-108">Il cmdlet **Add-AzureRmApplicationGatewayIPConfiguration** aggiunge una configurazione IP a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="56fab-108">The **Add-AzureRmApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="56fab-109">Le configurazioni IP contengono la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="56fab-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="56fab-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56fab-110">EXAMPLES</span></span>

### <span data-ttu-id="56fab-111">Esempio 1: aggiungere una configurazione di rete virtuale a un gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="56fab-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzureRmVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="56fab-112">Il primo comando crea una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="56fab-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="56fab-113">Il secondo comando crea una subnet usando la rete virtuale creata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="56fab-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="56fab-114">Il terzo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="56fab-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="56fab-115">Il comando quarto aggiunge la configurazione IP al gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="56fab-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="56fab-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56fab-116">PARAMETERS</span></span>

### <span data-ttu-id="56fab-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="56fab-117">-ApplicationGateway</span></span>
<span data-ttu-id="56fab-118">Specifica il gateway dell'applicazione a cui questo cmdlet aggiunge una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="56fab-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="56fab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56fab-119">-DefaultProfile</span></span>
<span data-ttu-id="56fab-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56fab-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56fab-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="56fab-121">-Name</span></span>
<span data-ttu-id="56fab-122">Specifica il nome della configurazione IP da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="56fab-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="56fab-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="56fab-123">-Subnet</span></span>
<span data-ttu-id="56fab-124">Specifica una subnet.</span><span class="sxs-lookup"><span data-stu-id="56fab-124">Specifies a subnet.</span></span>
<span data-ttu-id="56fab-125">Questa è la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="56fab-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="56fab-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="56fab-126">-SubnetId</span></span>
<span data-ttu-id="56fab-127">Specifica un ID subnet.</span><span class="sxs-lookup"><span data-stu-id="56fab-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="56fab-128">Questa è la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="56fab-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="56fab-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56fab-129">CommonParameters</span></span>
<span data-ttu-id="56fab-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56fab-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56fab-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56fab-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56fab-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56fab-132">INPUTS</span></span>

### <span data-ttu-id="56fab-133">System. String</span><span class="sxs-lookup"><span data-stu-id="56fab-133">System.String</span></span>

## <span data-ttu-id="56fab-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56fab-134">OUTPUTS</span></span>

### <span data-ttu-id="56fab-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="56fab-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="56fab-136">Note</span><span class="sxs-lookup"><span data-stu-id="56fab-136">NOTES</span></span>

## <span data-ttu-id="56fab-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56fab-137">RELATED LINKS</span></span>

[<span data-ttu-id="56fab-138">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="56fab-138">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="56fab-139">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="56fab-139">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="56fab-140">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="56fab-140">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="56fab-141">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="56fab-141">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


