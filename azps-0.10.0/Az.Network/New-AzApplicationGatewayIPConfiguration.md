---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 67cf5adb8d8cc0bef914f0623f66ee0e871302d8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860566"
---
# <span data-ttu-id="0a8fc-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a8fc-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="0a8fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a8fc-102">SYNOPSIS</span></span>
<span data-ttu-id="0a8fc-103">Crea una configurazione IP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="0a8fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a8fc-104">SYNTAX</span></span>

### <span data-ttu-id="0a8fc-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0a8fc-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a8fc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0a8fc-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a8fc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a8fc-107">DESCRIPTION</span></span>
<span data-ttu-id="0a8fc-108">Il cmdlet **New-AzApplicationGatewayIPConfiguration** crea una configurazione IP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="0a8fc-109">La configurazione IP contiene la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="0a8fc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a8fc-110">EXAMPLES</span></span>

### <span data-ttu-id="0a8fc-111">Esempio 1: creare una configurazione IP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="0a8fc-112">Il primo comando consente di ottenere una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>

<span data-ttu-id="0a8fc-113">Il secondo comando ottiene la configurazione della subnet per la subnet a cui appartiene la rete virtuale nel comando precedente e la archivia nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="0a8fc-114">Il terzo comando crea la configurazione IP usando $Subnet.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="0a8fc-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a8fc-115">PARAMETERS</span></span>

### <span data-ttu-id="0a8fc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a8fc-116">-DefaultProfile</span></span>
<span data-ttu-id="0a8fc-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a8fc-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a8fc-118">-Name</span></span>
<span data-ttu-id="0a8fc-119">Specifica il nome della configurazione IP da creare.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="0a8fc-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="0a8fc-120">-Subnet</span></span>
<span data-ttu-id="0a8fc-121">Specifica l'oggetto subnet.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-121">Specifies the subnet object.</span></span>
<span data-ttu-id="0a8fc-122">Questa è la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="0a8fc-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0a8fc-123">-SubnetId</span></span>
<span data-ttu-id="0a8fc-124">Specifica l'ID subnet.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="0a8fc-125">Questa è la subnet in cui verrà distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="0a8fc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a8fc-126">CommonParameters</span></span>
<span data-ttu-id="0a8fc-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a8fc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a8fc-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a8fc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a8fc-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a8fc-129">INPUTS</span></span>

### <span data-ttu-id="0a8fc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0a8fc-130">System.String</span></span>

## <span data-ttu-id="0a8fc-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a8fc-131">OUTPUTS</span></span>

### <span data-ttu-id="0a8fc-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a8fc-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="0a8fc-133">Note</span><span class="sxs-lookup"><span data-stu-id="0a8fc-133">NOTES</span></span>

## <span data-ttu-id="0a8fc-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a8fc-134">RELATED LINKS</span></span>

[<span data-ttu-id="0a8fc-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a8fc-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="0a8fc-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a8fc-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="0a8fc-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a8fc-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="0a8fc-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a8fc-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


