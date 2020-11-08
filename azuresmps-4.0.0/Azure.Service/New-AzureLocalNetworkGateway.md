---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9F9E4639-A557-4BD8-88C2-894F6C848C4A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa54a7bd236bb561b3de4b9c2a3c0a2710deb61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029469"
---
# <span data-ttu-id="06557-101">New-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06557-101">New-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="06557-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06557-102">SYNOPSIS</span></span>
<span data-ttu-id="06557-103">Crea un gateway di rete locale di Azure.</span><span class="sxs-lookup"><span data-stu-id="06557-103">creates an Azure local network gateway.</span></span>

## <span data-ttu-id="06557-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06557-104">SYNTAX</span></span>

```
New-AzureLocalNetworkGateway -GatewayName <String> -IpAddress <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="06557-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06557-105">DESCRIPTION</span></span>
<span data-ttu-id="06557-106">Il cmdlet **New-AzureLocalNetworkGateway** crea un gateway di rete locale di Azure.</span><span class="sxs-lookup"><span data-stu-id="06557-106">The **New-AzureLocalNetworkGateway** cmdlet creates an Azure local network gateway.</span></span>

## <span data-ttu-id="06557-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06557-107">EXAMPLES</span></span>

## <span data-ttu-id="06557-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06557-108">PARAMETERS</span></span>

### <span data-ttu-id="06557-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="06557-109">-AddressSpace</span></span>
<span data-ttu-id="06557-110">Specifica lo spazio degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="06557-110">Specifies the address space.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06557-111">-ASN</span><span class="sxs-lookup"><span data-stu-id="06557-111">-Asn</span></span>
<span data-ttu-id="06557-112">Specifica il numero di sistema autonomo (ASN).</span><span class="sxs-lookup"><span data-stu-id="06557-112">Specifies the autonomous system number (ASN).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06557-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="06557-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="06557-114">Specifica l'indirizzo di peering Border Gateway Protocol (BGP).</span><span class="sxs-lookup"><span data-stu-id="06557-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06557-115">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="06557-115">-GatewayName</span></span>
<span data-ttu-id="06557-116">Specifica il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="06557-116">Specifies the name of the gateway.</span></span>

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

### <span data-ttu-id="06557-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="06557-117">-IpAddress</span></span>
<span data-ttu-id="06557-118">Specifica l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="06557-118">Specifies the IP address.</span></span>

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

### <span data-ttu-id="06557-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="06557-119">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06557-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="06557-120">-Profile</span></span>
<span data-ttu-id="06557-121">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06557-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="06557-122">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="06557-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06557-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06557-123">CommonParameters</span></span>
<span data-ttu-id="06557-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06557-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06557-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06557-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06557-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06557-126">INPUTS</span></span>

## <span data-ttu-id="06557-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06557-127">OUTPUTS</span></span>

## <span data-ttu-id="06557-128">Note</span><span class="sxs-lookup"><span data-stu-id="06557-128">NOTES</span></span>

## <span data-ttu-id="06557-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06557-129">RELATED LINKS</span></span>

[<span data-ttu-id="06557-130">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06557-130">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="06557-131">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06557-131">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)

[<span data-ttu-id="06557-132">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06557-132">Reset-AzureLocalNetworkGateway</span></span>](./Reset-AzureLocalNetworkGateway.md)


