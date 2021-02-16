---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179727"
---
# <span data-ttu-id="64113-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="64113-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="64113-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64113-102">SYNOPSIS</span></span>
<span data-ttu-id="64113-103">Crea una configurazione IP per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="64113-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="64113-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64113-104">SYNTAX</span></span>

### <span data-ttu-id="64113-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="64113-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64113-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="64113-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64113-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="64113-107">DESCRIPTION</span></span>
<span data-ttu-id="64113-108">Il cmdlet **New-AzApplicationGatewayIPConfiguration crea** una configurazione IP per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="64113-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="64113-109">La configurazione IP contiene la subnet in cui è distribuito il gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="64113-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="64113-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64113-110">EXAMPLES</span></span>

### <span data-ttu-id="64113-111">Esempio 1: Creare una configurazione IP per un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="64113-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="64113-112">Il primo comando ottiene una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="64113-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="64113-113">Il secondo comando ottiene la configurazione subnet per la subnet a cui appartiene la rete virtuale nel comando precedente e la archivia nella variabile $Subnet locale.</span><span class="sxs-lookup"><span data-stu-id="64113-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="64113-114">Il terzo comando crea la configurazione IP usando $Subnet.</span><span class="sxs-lookup"><span data-stu-id="64113-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="64113-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64113-115">PARAMETERS</span></span>

### <span data-ttu-id="64113-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64113-116">-DefaultProfile</span></span>
<span data-ttu-id="64113-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64113-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64113-118">-Name</span><span class="sxs-lookup"><span data-stu-id="64113-118">-Name</span></span>
<span data-ttu-id="64113-119">Specifica il nome della configurazione IP da creare.</span><span class="sxs-lookup"><span data-stu-id="64113-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="64113-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="64113-120">-Subnet</span></span>
<span data-ttu-id="64113-121">Specifica l'oggetto subnet.</span><span class="sxs-lookup"><span data-stu-id="64113-121">Specifies the subnet object.</span></span>
<span data-ttu-id="64113-122">Si tratta della subnet in cui viene distribuito il gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="64113-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="64113-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="64113-123">-SubnetId</span></span>
<span data-ttu-id="64113-124">Specifica l'ID subnet.</span><span class="sxs-lookup"><span data-stu-id="64113-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="64113-125">Si tratta della subnet in cui verrà distribuito il gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="64113-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="64113-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64113-126">CommonParameters</span></span>
<span data-ttu-id="64113-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64113-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64113-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64113-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64113-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="64113-129">INPUTS</span></span>

### <span data-ttu-id="64113-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="64113-130">None</span></span>

## <span data-ttu-id="64113-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64113-131">OUTPUTS</span></span>

### <span data-ttu-id="64113-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="64113-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="64113-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="64113-133">NOTES</span></span>

## <span data-ttu-id="64113-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64113-134">RELATED LINKS</span></span>

[<span data-ttu-id="64113-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="64113-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="64113-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="64113-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="64113-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="64113-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="64113-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="64113-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


