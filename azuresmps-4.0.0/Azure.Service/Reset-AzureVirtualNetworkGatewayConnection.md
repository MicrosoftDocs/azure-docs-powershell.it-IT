---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 09642B94-E888-4A22-9E8E-62109DB9394E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f42a788f29f8546e6f402f1685f4c91aa3d7e5cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029551"
---
# <span data-ttu-id="7558f-101">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7558f-101">Reset-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7558f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7558f-102">SYNOPSIS</span></span>
<span data-ttu-id="7558f-103">Reimposta una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7558f-103">Resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="7558f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7558f-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 -RoutingWeight <Int32> [-SharedKey <String>] [-EnableBgp <Boolean>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7558f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7558f-105">DESCRIPTION</span></span>
<span data-ttu-id="7558f-106">Il cmdlet **Reset-AzureVirtualNetworkGatewayConnection** Reimposta una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7558f-106">The **Reset-AzureVirtualNetworkGatewayConnection** cmdlet resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="7558f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7558f-107">EXAMPLES</span></span>

## <span data-ttu-id="7558f-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7558f-108">PARAMETERS</span></span>

### <span data-ttu-id="7558f-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="7558f-109">-ConnectedEntityId</span></span>
<span data-ttu-id="7558f-110">Specifica l'ID di un'entità connessa.</span><span class="sxs-lookup"><span data-stu-id="7558f-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="7558f-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7558f-111">-EnableBgp</span></span>
<span data-ttu-id="7558f-112">Abilita il protocollo BGP (Border Gateway Protocol).</span><span class="sxs-lookup"><span data-stu-id="7558f-112">Enables Border Gateway Protocol (BGP).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7558f-113">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="7558f-113">-GatewayId</span></span>
<span data-ttu-id="7558f-114">Specifica l'ID di un gateway.</span><span class="sxs-lookup"><span data-stu-id="7558f-114">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="7558f-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="7558f-115">-Profile</span></span>
<span data-ttu-id="7558f-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7558f-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7558f-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="7558f-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7558f-118">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="7558f-118">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7558f-119">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7558f-119">-SharedKey</span></span>
<span data-ttu-id="7558f-120">Specifica una chiave condivisa.</span><span class="sxs-lookup"><span data-stu-id="7558f-120">Specifies a shared key.</span></span>

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

### <span data-ttu-id="7558f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7558f-121">CommonParameters</span></span>
<span data-ttu-id="7558f-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7558f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7558f-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7558f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7558f-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7558f-124">INPUTS</span></span>

## <span data-ttu-id="7558f-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7558f-125">OUTPUTS</span></span>

## <span data-ttu-id="7558f-126">Note</span><span class="sxs-lookup"><span data-stu-id="7558f-126">NOTES</span></span>

## <span data-ttu-id="7558f-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7558f-127">RELATED LINKS</span></span>

[<span data-ttu-id="7558f-128">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7558f-128">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7558f-129">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7558f-129">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7558f-130">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7558f-130">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)


