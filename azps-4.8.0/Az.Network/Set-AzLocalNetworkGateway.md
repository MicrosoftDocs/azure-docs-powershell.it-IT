---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
ms.openlocfilehash: ac93b104a8ccc1afbeb41bcd11910b76f7d4039f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192026"
---
# <span data-ttu-id="ec6f6-101">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ec6f6-101">Set-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="ec6f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec6f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ec6f6-103">Modifica un gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="ec6f6-103">Modifies a local network gateway.</span></span>

## <span data-ttu-id="ec6f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec6f6-104">SYNTAX</span></span>

```
Set-AzLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway> [-AddressPrefix <String[]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec6f6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec6f6-105">DESCRIPTION</span></span>
<span data-ttu-id="ec6f6-106">Il cmdlet **set-AzLocalNetworkGateway** modifica un gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="ec6f6-106">The **Set-AzLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="ec6f6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec6f6-107">EXAMPLES</span></span>

### <span data-ttu-id="ec6f6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ec6f6-108">Example 1</span></span>
<span data-ttu-id="ec6f6-109">Impostare la configurazione per un gateway esistente</span><span class="sxs-lookup"><span data-stu-id="ec6f6-109">Set configuration for an existing gateway</span></span>


```
$lgw = Get-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
Set-AzLocalNetworkGateway -LocalNetworkGateway $lgw

Name                     : myLocalGW
ResourceGroupName        : TestRG1
Location                 : westus
Id                       : /subscriptions/81ab786c-56eb-4a4d-bb5f-f60329772466/resourceGroups/TestRG1/providers/Microso
                           ft.Network/localNetworkGateways/myLocalGW
Etag                     : W/"d2de6968-315e-411d-a4b8-a8c335abe61b"
ResourceGuid             : 393acf8b-dbb8-4b08-a9ea-c714570710e1
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : 1.2.3.4
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

## <span data-ttu-id="ec6f6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec6f6-110">PARAMETERS</span></span>

### <span data-ttu-id="ec6f6-111">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ec6f6-111">-AddressPrefix</span></span>
```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec6f6-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec6f6-112">-AsJob</span></span>
<span data-ttu-id="ec6f6-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ec6f6-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec6f6-114">-ASN</span><span class="sxs-lookup"><span data-stu-id="ec6f6-114">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec6f6-115">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="ec6f6-115">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec6f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec6f6-116">-DefaultProfile</span></span>
<span data-ttu-id="ec6f6-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec6f6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec6f6-118">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ec6f6-118">-LocalNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec6f6-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="ec6f6-119">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec6f6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec6f6-120">CommonParameters</span></span>
<span data-ttu-id="ec6f6-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec6f6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec6f6-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec6f6-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec6f6-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec6f6-123">INPUTS</span></span>

### <span data-ttu-id="ec6f6-124">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ec6f6-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="ec6f6-125">System. String []</span><span class="sxs-lookup"><span data-stu-id="ec6f6-125">System.String[]</span></span>

### <span data-ttu-id="ec6f6-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="ec6f6-126">System.UInt32</span></span>

### <span data-ttu-id="ec6f6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ec6f6-127">System.String</span></span>

### <span data-ttu-id="ec6f6-128">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ec6f6-128">System.Int32</span></span>

## <span data-ttu-id="ec6f6-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec6f6-129">OUTPUTS</span></span>

### <span data-ttu-id="ec6f6-130">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ec6f6-130">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="ec6f6-131">Note</span><span class="sxs-lookup"><span data-stu-id="ec6f6-131">NOTES</span></span>

## <span data-ttu-id="ec6f6-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec6f6-132">RELATED LINKS</span></span>

[<span data-ttu-id="ec6f6-133">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ec6f6-133">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="ec6f6-134">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ec6f6-134">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="ec6f6-135">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ec6f6-135">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)