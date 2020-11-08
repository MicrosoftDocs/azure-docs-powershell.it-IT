---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 88AB3621-7C80-41BA-BE49-4F8F9C46BCF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fb0fa13cb5ea155b945505fd3f99c28494c5dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029985"
---
# <span data-ttu-id="362e5-101">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="362e5-101">Get-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="362e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="362e5-102">SYNOPSIS</span></span>
<span data-ttu-id="362e5-103">Ottiene una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="362e5-103">Gets a virtual network gateway connection.</span></span>

## <span data-ttu-id="362e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="362e5-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayConnection [-GatewayId <String>] [-ConnectedEntityId <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="362e5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="362e5-105">DESCRIPTION</span></span>
<span data-ttu-id="362e5-106">Il cmdlet **Get-AzureVirtualNetworkGatewayConnection** ottiene una connessione di gateway di rete virtuale Azure.</span><span class="sxs-lookup"><span data-stu-id="362e5-106">The **Get-AzureVirtualNetworkGatewayConnection** cmdlet gets an Azure virtual network gateway connection.</span></span>

## <span data-ttu-id="362e5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="362e5-107">EXAMPLES</span></span>

## <span data-ttu-id="362e5-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="362e5-108">PARAMETERS</span></span>

### <span data-ttu-id="362e5-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="362e5-109">-ConnectedEntityId</span></span>
<span data-ttu-id="362e5-110">Specifica l'ID di un'entità connessa.</span><span class="sxs-lookup"><span data-stu-id="362e5-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="362e5-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="362e5-111">-GatewayId</span></span>
<span data-ttu-id="362e5-112">Specifica l'ID del gateway.</span><span class="sxs-lookup"><span data-stu-id="362e5-112">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="362e5-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="362e5-113">-Profile</span></span>
<span data-ttu-id="362e5-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="362e5-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="362e5-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="362e5-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="362e5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="362e5-116">CommonParameters</span></span>
<span data-ttu-id="362e5-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="362e5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="362e5-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="362e5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="362e5-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="362e5-119">INPUTS</span></span>

## <span data-ttu-id="362e5-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="362e5-120">OUTPUTS</span></span>

## <span data-ttu-id="362e5-121">Note</span><span class="sxs-lookup"><span data-stu-id="362e5-121">NOTES</span></span>

## <span data-ttu-id="362e5-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="362e5-122">RELATED LINKS</span></span>

[<span data-ttu-id="362e5-123">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="362e5-123">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="362e5-124">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="362e5-124">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="362e5-125">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="362e5-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)
