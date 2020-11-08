---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AD5F4D69-45AF-46FB-ADF0-59CEF9908EF7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d63ac418d2dcee97afef9ae5f351fb2c1eebece0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029548"
---
# <span data-ttu-id="f7ca8-101">Resize-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7ca8-101">Resize-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="f7ca8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ca8-103">Ridimensiona un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f7ca8-103">Resizes a virtual network gateway.</span></span>

## <span data-ttu-id="f7ca8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7ca8-104">SYNTAX</span></span>

```
Resize-AzureVirtualNetworkGateway -GatewayId <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7ca8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7ca8-105">DESCRIPTION</span></span>
<span data-ttu-id="f7ca8-106">Il cmdlet Resize-AzureVirtualNetworkGateway ridimensiona un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f7ca8-106">The Resize-AzureVirtualNetworkGateway cmdlet resizes a virtual network gateway.</span></span>

## <span data-ttu-id="f7ca8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7ca8-107">EXAMPLES</span></span>

## <span data-ttu-id="f7ca8-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7ca8-108">PARAMETERS</span></span>

### <span data-ttu-id="f7ca8-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="f7ca8-109">-GatewayId</span></span>
<span data-ttu-id="f7ca8-110">Specifica l'ID di un gateway.</span><span class="sxs-lookup"><span data-stu-id="f7ca8-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="f7ca8-111">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="f7ca8-111">-GatewaySKU</span></span>
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

### <span data-ttu-id="f7ca8-112">-Profile</span><span class="sxs-lookup"><span data-stu-id="f7ca8-112">-Profile</span></span>
<span data-ttu-id="f7ca8-113">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7ca8-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f7ca8-114">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="f7ca8-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f7ca8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ca8-115">CommonParameters</span></span>
<span data-ttu-id="f7ca8-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7ca8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ca8-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7ca8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ca8-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7ca8-118">INPUTS</span></span>

## <span data-ttu-id="f7ca8-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7ca8-119">OUTPUTS</span></span>

## <span data-ttu-id="f7ca8-120">Note</span><span class="sxs-lookup"><span data-stu-id="f7ca8-120">NOTES</span></span>

## <span data-ttu-id="f7ca8-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7ca8-121">RELATED LINKS</span></span>

[<span data-ttu-id="f7ca8-122">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7ca8-122">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="f7ca8-123">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7ca8-123">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="f7ca8-124">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7ca8-124">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="f7ca8-125">Reset-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7ca8-125">Reset-AzureVirtualNetworkGateway</span></span>](./Reset-AzureVirtualNetworkGateway.md)


