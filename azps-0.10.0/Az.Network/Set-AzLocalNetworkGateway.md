---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLocalNetworkGateway.md
ms.openlocfilehash: 61e2fd8a4f6c073bbb900586b0d73dec97c3b662
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862774"
---
# <span data-ttu-id="c24f4-101">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c24f4-101">Set-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="c24f4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c24f4-102">SYNOPSIS</span></span>
<span data-ttu-id="c24f4-103">Modifica un gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="c24f4-103">Modifies a local network gateway.</span></span>

## <span data-ttu-id="c24f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c24f4-104">SYNTAX</span></span>

```
Set-AzLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c24f4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c24f4-105">DESCRIPTION</span></span>
<span data-ttu-id="c24f4-106">Il cmdlet **set-AzLocalNetworkGateway** modifica un gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="c24f4-106">The **Set-AzLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="c24f4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c24f4-107">EXAMPLES</span></span>

### <span data-ttu-id="c24f4-108">1:</span><span class="sxs-lookup"><span data-stu-id="c24f4-108">1:</span></span>
```

```

## <span data-ttu-id="c24f4-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c24f4-109">PARAMETERS</span></span>

### <span data-ttu-id="c24f4-110">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c24f4-110">-AddressPrefix</span></span>
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

### <span data-ttu-id="c24f4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c24f4-111">-AsJob</span></span>
<span data-ttu-id="c24f4-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c24f4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c24f4-113">-ASN</span><span class="sxs-lookup"><span data-stu-id="c24f4-113">-Asn</span></span>
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

### <span data-ttu-id="c24f4-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="c24f4-114">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="c24f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c24f4-115">-DefaultProfile</span></span>
<span data-ttu-id="c24f4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c24f4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c24f4-117">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c24f4-117">-LocalNetworkGateway</span></span>
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

### <span data-ttu-id="c24f4-118">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="c24f4-118">-PeerWeight</span></span>
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

### <span data-ttu-id="c24f4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c24f4-119">CommonParameters</span></span>
<span data-ttu-id="c24f4-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c24f4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c24f4-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c24f4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c24f4-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c24f4-122">INPUTS</span></span>

### <span data-ttu-id="c24f4-123">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c24f4-123">PSLocalNetworkGateway</span></span>
<span data-ttu-id="c24f4-124">Il parametro ' LocalNetworkGateway ' accetta il valore di tipo ' PSLocalNetworkGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c24f4-124">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="c24f4-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c24f4-125">OUTPUTS</span></span>

### <span data-ttu-id="c24f4-126">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c24f4-126">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="c24f4-127">Note</span><span class="sxs-lookup"><span data-stu-id="c24f4-127">NOTES</span></span>

## <span data-ttu-id="c24f4-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c24f4-128">RELATED LINKS</span></span>

[<span data-ttu-id="c24f4-129">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c24f4-129">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="c24f4-130">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c24f4-130">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="c24f4-131">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c24f4-131">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)


