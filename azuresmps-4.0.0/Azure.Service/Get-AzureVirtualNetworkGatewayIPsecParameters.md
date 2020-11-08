---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 425008DB-9761-42F1-8D6D-F35757A3CA6C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37aa0718c4faa637b16ccde61f5e5b241bb9aa92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029977"
---
# <span data-ttu-id="522a5-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="522a5-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="522a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="522a5-102">SYNOPSIS</span></span>
<span data-ttu-id="522a5-103">Ottiene i parametri IPsec per un gateway di rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="522a5-103">Gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="522a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="522a5-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="522a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="522a5-105">DESCRIPTION</span></span>
<span data-ttu-id="522a5-106">Il cmdlet **Get-AzureVirtualNetworkGatewayIPsecParameters** ottiene i parametri IPSec per un gateway di rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="522a5-106">The **Get-AzureVirtualNetworkGatewayIPsecParameters** cmdlet gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="522a5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="522a5-107">EXAMPLES</span></span>

## <span data-ttu-id="522a5-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="522a5-108">PARAMETERS</span></span>

### <span data-ttu-id="522a5-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="522a5-109">-ConnectedEntityId</span></span>
<span data-ttu-id="522a5-110">Specifica l'ID di una connessione connessa.</span><span class="sxs-lookup"><span data-stu-id="522a5-110">Specifies the ID of a connected entitiy.</span></span>

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

### <span data-ttu-id="522a5-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="522a5-111">-GatewayId</span></span>
<span data-ttu-id="522a5-112">Specifica l'ID di un gateway.</span><span class="sxs-lookup"><span data-stu-id="522a5-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="522a5-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="522a5-113">-Profile</span></span>
<span data-ttu-id="522a5-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="522a5-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="522a5-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="522a5-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="522a5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="522a5-116">CommonParameters</span></span>
<span data-ttu-id="522a5-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="522a5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="522a5-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="522a5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="522a5-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="522a5-119">INPUTS</span></span>

## <span data-ttu-id="522a5-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="522a5-120">OUTPUTS</span></span>

## <span data-ttu-id="522a5-121">Note</span><span class="sxs-lookup"><span data-stu-id="522a5-121">NOTES</span></span>

## <span data-ttu-id="522a5-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="522a5-122">RELATED LINKS</span></span>

[<span data-ttu-id="522a5-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="522a5-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Set-AzureVirtualNetworkGatewayIPsecParameters.md)


