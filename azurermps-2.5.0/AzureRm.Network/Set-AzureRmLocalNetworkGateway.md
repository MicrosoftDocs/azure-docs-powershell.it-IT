---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f01fd5c1c6694c8d16ab34e6aad9f6a52463c726
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866843"
---
# <span data-ttu-id="e3be1-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3be1-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="e3be1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3be1-102">SYNOPSIS</span></span>
<span data-ttu-id="e3be1-103">Modifica un gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="e3be1-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3be1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3be1-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3be1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3be1-105">DESCRIPTION</span></span>
<span data-ttu-id="e3be1-106">Il cmdlet **set-AzureRmLocalNetworkGateway** modifica un gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="e3be1-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="e3be1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3be1-107">EXAMPLES</span></span>

### <span data-ttu-id="e3be1-108">1:</span><span class="sxs-lookup"><span data-stu-id="e3be1-108">1:</span></span>
```

```

## <span data-ttu-id="e3be1-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3be1-109">PARAMETERS</span></span>

### <span data-ttu-id="e3be1-110">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e3be1-110">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3be1-111">-AsJob</span></span>
<span data-ttu-id="e3be1-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e3be1-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3be1-113">-ASN</span><span class="sxs-lookup"><span data-stu-id="e3be1-113">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be1-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="e3be1-114">-BgpPeeringAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3be1-115">-DefaultProfile</span></span>
<span data-ttu-id="e3be1-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3be1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3be1-117">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3be1-117">-LocalNetworkGateway</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be1-118">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="e3be1-118">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3be1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3be1-119">CommonParameters</span></span>
<span data-ttu-id="e3be1-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3be1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3be1-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3be1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3be1-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3be1-122">INPUTS</span></span>

### <span data-ttu-id="e3be1-123">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3be1-123">PSLocalNetworkGateway</span></span>
<span data-ttu-id="e3be1-124">Il parametro ' LocalNetworkGateway ' accetta il valore di tipo ' PSLocalNetworkGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e3be1-124">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="e3be1-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3be1-125">OUTPUTS</span></span>

### <span data-ttu-id="e3be1-126">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3be1-126">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="e3be1-127">Note</span><span class="sxs-lookup"><span data-stu-id="e3be1-127">NOTES</span></span>

## <span data-ttu-id="e3be1-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3be1-128">RELATED LINKS</span></span>

[<span data-ttu-id="e3be1-129">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3be1-129">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="e3be1-130">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3be1-130">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="e3be1-131">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3be1-131">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


