---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4F1E69B8-15FB-495F-B910-04E450D3215F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a5b53f909b840a761d40f79a311fb61b7e2337b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029550"
---
# <span data-ttu-id="44a85-101">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="44a85-101">Reset-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="44a85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44a85-102">SYNOPSIS</span></span>
<span data-ttu-id="44a85-103">Reimposta una chiave del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="44a85-103">Resets a virtual network gateway key.</span></span>

## <span data-ttu-id="44a85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44a85-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -keyLength <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="44a85-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44a85-105">DESCRIPTION</span></span>
<span data-ttu-id="44a85-106">Il cmdlet **Reset-AzureVirtualNetworkGatewayKey** Reimposta una chiave del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="44a85-106">The **Reset-AzureVirtualNetworkGatewayKey** cmdlet resets a virtual network gateway key.</span></span>

## <span data-ttu-id="44a85-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44a85-107">EXAMPLES</span></span>

## <span data-ttu-id="44a85-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44a85-108">PARAMETERS</span></span>

### <span data-ttu-id="44a85-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="44a85-109">-ConnectedEntityId</span></span>
<span data-ttu-id="44a85-110">Specifica l'ID di un'entità connessa.</span><span class="sxs-lookup"><span data-stu-id="44a85-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="44a85-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="44a85-111">-GatewayId</span></span>
<span data-ttu-id="44a85-112">Specifica l'ID di un gateway.</span><span class="sxs-lookup"><span data-stu-id="44a85-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="44a85-113">-Lunghezza</span><span class="sxs-lookup"><span data-stu-id="44a85-113">-keyLength</span></span>
<span data-ttu-id="44a85-114">Specifica la lunghezza della chiave.</span><span class="sxs-lookup"><span data-stu-id="44a85-114">Specifies the key length.</span></span>

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

### <span data-ttu-id="44a85-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="44a85-115">-Profile</span></span>
<span data-ttu-id="44a85-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44a85-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="44a85-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="44a85-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="44a85-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44a85-118">CommonParameters</span></span>
<span data-ttu-id="44a85-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44a85-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44a85-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44a85-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44a85-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44a85-121">INPUTS</span></span>

## <span data-ttu-id="44a85-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44a85-122">OUTPUTS</span></span>

## <span data-ttu-id="44a85-123">Note</span><span class="sxs-lookup"><span data-stu-id="44a85-123">NOTES</span></span>

## <span data-ttu-id="44a85-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44a85-124">RELATED LINKS</span></span>

[<span data-ttu-id="44a85-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="44a85-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="44a85-126">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="44a85-126">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)
