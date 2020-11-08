---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F3D44471-50F0-4737-9AF5-3DE7222EAF9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9aa386b47c02ed945cad63c00425534d68e66f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023443"
---
# <span data-ttu-id="a24a7-101">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a24a7-101">Remove-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="a24a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a24a7-102">SYNOPSIS</span></span>
<span data-ttu-id="a24a7-103">Rimuove una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a24a7-103">Removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="a24a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a24a7-104">SYNTAX</span></span>

```
Remove-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a24a7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a24a7-105">DESCRIPTION</span></span>
<span data-ttu-id="a24a7-106">Il cmdlet **Remove-AzureVirtualNetworkGatewayConnection** rimuove una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a24a7-106">The **Remove-AzureVirtualNetworkGatewayConnection** cmdlet removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="a24a7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a24a7-107">EXAMPLES</span></span>

## <span data-ttu-id="a24a7-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a24a7-108">PARAMETERS</span></span>

### <span data-ttu-id="a24a7-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="a24a7-109">-ConnectedEntityId</span></span>
<span data-ttu-id="a24a7-110">Specifica l'ID di un'entità connessa.</span><span class="sxs-lookup"><span data-stu-id="a24a7-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="a24a7-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="a24a7-111">-GatewayId</span></span>
<span data-ttu-id="a24a7-112">Specifica l'ID di un gateway.</span><span class="sxs-lookup"><span data-stu-id="a24a7-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="a24a7-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="a24a7-113">-Profile</span></span>
<span data-ttu-id="a24a7-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a24a7-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a24a7-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a24a7-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a24a7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a24a7-116">CommonParameters</span></span>
<span data-ttu-id="a24a7-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a24a7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a24a7-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a24a7-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a24a7-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a24a7-119">INPUTS</span></span>

## <span data-ttu-id="a24a7-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a24a7-120">OUTPUTS</span></span>

## <span data-ttu-id="a24a7-121">Note</span><span class="sxs-lookup"><span data-stu-id="a24a7-121">NOTES</span></span>

## <span data-ttu-id="a24a7-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a24a7-122">RELATED LINKS</span></span>

[<span data-ttu-id="a24a7-123">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a24a7-123">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="a24a7-124">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a24a7-124">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="a24a7-125">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a24a7-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)


