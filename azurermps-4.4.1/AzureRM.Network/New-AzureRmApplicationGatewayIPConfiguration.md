---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 076965d0f63a8c28742cf9853068b9e020403a66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520497"
---
# <span data-ttu-id="7ad52-101">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad52-101">New-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="7ad52-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ad52-102">SYNOPSIS</span></span>
<span data-ttu-id="7ad52-103">Crea una configurazione IP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ad52-103">Creates an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ad52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ad52-104">SYNTAX</span></span>

### <span data-ttu-id="7ad52-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7ad52-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ad52-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7ad52-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ad52-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ad52-107">DESCRIPTION</span></span>
<span data-ttu-id="7ad52-108">Il cmdlet **New-AzureRmApplicationGatewayIPConfiguration** crea una configurazione IP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ad52-108">The **New-AzureRmApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="7ad52-109">La configurazione IP contiene la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ad52-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="7ad52-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ad52-110">EXAMPLES</span></span>

### <span data-ttu-id="7ad52-111">Esempio 1: creare una configurazione IP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ad52-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzureRmApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="7ad52-112">Il primo comando consente di ottenere una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="7ad52-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>

<span data-ttu-id="7ad52-113">Il secondo comando ottiene la configurazione della subnet per la subnet a cui appartiene la rete virtuale nel comando precedente e la archivia nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="7ad52-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="7ad52-114">Il terzo comando crea la configurazione IP usando $Subnet.</span><span class="sxs-lookup"><span data-stu-id="7ad52-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="7ad52-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ad52-115">PARAMETERS</span></span>

### <span data-ttu-id="7ad52-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ad52-116">-Name</span></span>
<span data-ttu-id="7ad52-117">Specifica il nome della configurazione IP da creare.</span><span class="sxs-lookup"><span data-stu-id="7ad52-117">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="7ad52-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="7ad52-118">-Subnet</span></span>
<span data-ttu-id="7ad52-119">Specifica l'oggetto subnet.</span><span class="sxs-lookup"><span data-stu-id="7ad52-119">Specifies the subnet object.</span></span>
<span data-ttu-id="7ad52-120">Questa è la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ad52-120">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="7ad52-121">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7ad52-121">-SubnetId</span></span>
<span data-ttu-id="7ad52-122">Specifica l'ID subnet.</span><span class="sxs-lookup"><span data-stu-id="7ad52-122">Specifies the subnet ID.</span></span>
<span data-ttu-id="7ad52-123">Questa è la subnet in cui verrà distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ad52-123">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="7ad52-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ad52-124">-DefaultProfile</span></span>
<span data-ttu-id="7ad52-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ad52-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ad52-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ad52-126">CommonParameters</span></span>
<span data-ttu-id="7ad52-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ad52-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ad52-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ad52-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ad52-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ad52-129">INPUTS</span></span>

### <span data-ttu-id="7ad52-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7ad52-130">System.String</span></span>

## <span data-ttu-id="7ad52-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ad52-131">OUTPUTS</span></span>

### <span data-ttu-id="7ad52-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad52-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="7ad52-133">Note</span><span class="sxs-lookup"><span data-stu-id="7ad52-133">NOTES</span></span>

## <span data-ttu-id="7ad52-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ad52-134">RELATED LINKS</span></span>

[<span data-ttu-id="7ad52-135">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad52-135">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="7ad52-136">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad52-136">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="7ad52-137">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad52-137">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="7ad52-138">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad52-138">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


