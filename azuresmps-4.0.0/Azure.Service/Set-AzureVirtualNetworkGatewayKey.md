---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8099942A-B6EB-4C01-9F57-378B0EB7B3C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c933b716095392a215543cfc61d334cd347835
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023395"
---
# <span data-ttu-id="df1a2-101">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="df1a2-101">Set-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="df1a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df1a2-102">SYNOPSIS</span></span>
<span data-ttu-id="df1a2-103">Imposta la chiave per un gateway di rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="df1a2-103">Sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="df1a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df1a2-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="df1a2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df1a2-105">DESCRIPTION</span></span>
<span data-ttu-id="df1a2-106">Il cmdlet **set-AzureVirtualNetworkGatewayKey** imposta la chiave per un gateway di rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="df1a2-106">The **Set-AzureVirtualNetworkGatewayKey** cmdlet sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="df1a2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df1a2-107">EXAMPLES</span></span>

## <span data-ttu-id="df1a2-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df1a2-108">PARAMETERS</span></span>

### <span data-ttu-id="df1a2-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="df1a2-109">-ConnectedEntityId</span></span>
<span data-ttu-id="df1a2-110">Specifica l'ID di un'entità connessa.</span><span class="sxs-lookup"><span data-stu-id="df1a2-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="df1a2-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="df1a2-111">-GatewayId</span></span>
<span data-ttu-id="df1a2-112">Specifica l'ID di un gateway.</span><span class="sxs-lookup"><span data-stu-id="df1a2-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="df1a2-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="df1a2-113">-Profile</span></span>
<span data-ttu-id="df1a2-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df1a2-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="df1a2-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="df1a2-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="df1a2-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="df1a2-116">-SharedKey</span></span>
<span data-ttu-id="df1a2-117">Specifica una chiave condivisa.</span><span class="sxs-lookup"><span data-stu-id="df1a2-117">Specifies a shared key.</span></span>

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

### <span data-ttu-id="df1a2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1a2-118">CommonParameters</span></span>
<span data-ttu-id="df1a2-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df1a2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1a2-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df1a2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1a2-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df1a2-121">INPUTS</span></span>

## <span data-ttu-id="df1a2-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df1a2-122">OUTPUTS</span></span>

## <span data-ttu-id="df1a2-123">Note</span><span class="sxs-lookup"><span data-stu-id="df1a2-123">NOTES</span></span>

## <span data-ttu-id="df1a2-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df1a2-124">RELATED LINKS</span></span>

[<span data-ttu-id="df1a2-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="df1a2-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="df1a2-126">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="df1a2-126">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)


