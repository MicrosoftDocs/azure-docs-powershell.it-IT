---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190984"
---
# <span data-ttu-id="e903a-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e903a-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="e903a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e903a-102">SYNOPSIS</span></span>
<span data-ttu-id="e903a-103">Crea una configurazione IP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e903a-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="e903a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e903a-104">SYNTAX</span></span>

### <span data-ttu-id="e903a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e903a-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e903a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e903a-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e903a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e903a-107">DESCRIPTION</span></span>
<span data-ttu-id="e903a-108">Il cmdlet **New-AzApplicationGatewayIPConfiguration** crea una configurazione IP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e903a-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="e903a-109">La configurazione IP contiene la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e903a-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="e903a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e903a-110">EXAMPLES</span></span>

### <span data-ttu-id="e903a-111">Esempio 1: creare una configurazione IP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e903a-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="e903a-112">Il primo comando consente di ottenere una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="e903a-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="e903a-113">Il secondo comando ottiene la configurazione della subnet per la subnet a cui appartiene la rete virtuale nel comando precedente e la archivia nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="e903a-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="e903a-114">Il terzo comando crea la configurazione IP usando $Subnet.</span><span class="sxs-lookup"><span data-stu-id="e903a-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="e903a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e903a-115">PARAMETERS</span></span>

### <span data-ttu-id="e903a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e903a-116">-DefaultProfile</span></span>
<span data-ttu-id="e903a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e903a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e903a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e903a-118">-Name</span></span>
<span data-ttu-id="e903a-119">Specifica il nome della configurazione IP da creare.</span><span class="sxs-lookup"><span data-stu-id="e903a-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="e903a-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="e903a-120">-Subnet</span></span>
<span data-ttu-id="e903a-121">Specifica l'oggetto subnet.</span><span class="sxs-lookup"><span data-stu-id="e903a-121">Specifies the subnet object.</span></span>
<span data-ttu-id="e903a-122">Questa è la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e903a-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="e903a-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e903a-123">-SubnetId</span></span>
<span data-ttu-id="e903a-124">Specifica l'ID subnet.</span><span class="sxs-lookup"><span data-stu-id="e903a-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="e903a-125">Questa è la subnet in cui verrà distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e903a-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="e903a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e903a-126">CommonParameters</span></span>
<span data-ttu-id="e903a-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e903a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e903a-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e903a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e903a-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e903a-129">INPUTS</span></span>

### <span data-ttu-id="e903a-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e903a-130">None</span></span>

## <span data-ttu-id="e903a-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e903a-131">OUTPUTS</span></span>

### <span data-ttu-id="e903a-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e903a-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="e903a-133">Note</span><span class="sxs-lookup"><span data-stu-id="e903a-133">NOTES</span></span>

## <span data-ttu-id="e903a-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e903a-134">RELATED LINKS</span></span>

[<span data-ttu-id="e903a-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e903a-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e903a-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e903a-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e903a-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e903a-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e903a-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e903a-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


