---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5F016D72-80EB-462D-9646-25EC4E33293E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 485b29130fd4b54c378f3ec19389b6c24ba86c63
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029975"
---
# <span data-ttu-id="c4398-101">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c4398-101">Get-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="c4398-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4398-102">SYNOPSIS</span></span>
<span data-ttu-id="c4398-103">Ottiene la chiave per un gateway di rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="c4398-103">Gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="c4398-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4398-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4398-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4398-105">DESCRIPTION</span></span>
<span data-ttu-id="c4398-106">Il cmdlet **Get-AzureVirtualNetworkGatewayKey** ottiene la chiave per un gateway di rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="c4398-106">The **Get-AzureVirtualNetworkGatewayKey** cmdlet gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="c4398-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4398-107">EXAMPLES</span></span>

## <span data-ttu-id="c4398-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4398-108">PARAMETERS</span></span>

### <span data-ttu-id="c4398-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="c4398-109">-ConnectedEntityId</span></span>
<span data-ttu-id="c4398-110">Specifica l'ID di un'entità connessa.</span><span class="sxs-lookup"><span data-stu-id="c4398-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="c4398-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="c4398-111">-GatewayId</span></span>
<span data-ttu-id="c4398-112">Specifica l'ID di un gateway.</span><span class="sxs-lookup"><span data-stu-id="c4398-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="c4398-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="c4398-113">-Profile</span></span>
<span data-ttu-id="c4398-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4398-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c4398-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c4398-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c4398-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4398-116">CommonParameters</span></span>
<span data-ttu-id="c4398-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4398-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4398-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4398-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4398-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4398-119">INPUTS</span></span>

## <span data-ttu-id="c4398-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4398-120">OUTPUTS</span></span>

## <span data-ttu-id="c4398-121">Note</span><span class="sxs-lookup"><span data-stu-id="c4398-121">NOTES</span></span>

## <span data-ttu-id="c4398-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4398-122">RELATED LINKS</span></span>

[<span data-ttu-id="c4398-123">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c4398-123">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="c4398-124">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c4398-124">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)


