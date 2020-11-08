---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0E4D44EE-BF28-46FE-B2FA-D35C1651016F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3940a5e6fc69ebee02f3e0de963bc87f790f8860
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023430"
---
# <span data-ttu-id="ed81e-101">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed81e-101">Reset-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="ed81e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed81e-102">SYNOPSIS</span></span>
<span data-ttu-id="ed81e-103">Reimposta un gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="ed81e-103">Resets a local network gateway.</span></span>

## <span data-ttu-id="ed81e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed81e-104">SYNTAX</span></span>

```
Reset-AzureLocalNetworkGateway -GatewayId <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ed81e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed81e-105">DESCRIPTION</span></span>
<span data-ttu-id="ed81e-106">Il cmdlet **Reset-AzureLocalNetworkGateway** Reimposta un gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="ed81e-106">The **Reset-AzureLocalNetworkGateway** cmdlet resets a local network gateway.</span></span>

## <span data-ttu-id="ed81e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed81e-107">EXAMPLES</span></span>

## <span data-ttu-id="ed81e-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed81e-108">PARAMETERS</span></span>

### <span data-ttu-id="ed81e-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="ed81e-109">-AddressSpace</span></span>
<span data-ttu-id="ed81e-110">Specifica lo spazio degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="ed81e-110">Specifies the address space.</span></span>

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

### <span data-ttu-id="ed81e-111">-ASN</span><span class="sxs-lookup"><span data-stu-id="ed81e-111">-Asn</span></span>
<span data-ttu-id="ed81e-112">Specifica il numero di sistema autonomo (ASN).</span><span class="sxs-lookup"><span data-stu-id="ed81e-112">Specifies the autonomous system number (ASN).</span></span>

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

### <span data-ttu-id="ed81e-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="ed81e-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="ed81e-114">Specifica l'indirizzo di peering Border Gateway Protocol (BGP).</span><span class="sxs-lookup"><span data-stu-id="ed81e-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

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

### <span data-ttu-id="ed81e-115">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="ed81e-115">-GatewayId</span></span>
<span data-ttu-id="ed81e-116">Specifica l'ID del gateway.</span><span class="sxs-lookup"><span data-stu-id="ed81e-116">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="ed81e-117">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="ed81e-117">-PeerWeight</span></span>
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

### <span data-ttu-id="ed81e-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="ed81e-118">-Profile</span></span>
<span data-ttu-id="ed81e-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed81e-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ed81e-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ed81e-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ed81e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed81e-121">CommonParameters</span></span>
<span data-ttu-id="ed81e-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed81e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed81e-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed81e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed81e-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed81e-124">INPUTS</span></span>

## <span data-ttu-id="ed81e-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed81e-125">OUTPUTS</span></span>

## <span data-ttu-id="ed81e-126">Note</span><span class="sxs-lookup"><span data-stu-id="ed81e-126">NOTES</span></span>

## <span data-ttu-id="ed81e-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed81e-127">RELATED LINKS</span></span>

[<span data-ttu-id="ed81e-128">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed81e-128">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="ed81e-129">New-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed81e-129">New-AzureLocalNetworkGateway</span></span>](./New-AzureLocalNetworkGateway.md)

[<span data-ttu-id="ed81e-130">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed81e-130">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)


