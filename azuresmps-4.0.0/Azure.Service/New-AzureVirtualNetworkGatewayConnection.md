---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: E3C0C3AA-3941-469E-A6CC-A92ADD7377B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bf6824219879af52549d7815d65dcb502a2a752
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029647"
---
# <span data-ttu-id="e2cb1-101">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e2cb1-101">New-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="e2cb1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="e2cb1-103">Crea una connessione di rete Virtual gateway Azure.</span><span class="sxs-lookup"><span data-stu-id="e2cb1-103">Creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="e2cb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2cb1-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGatewayConnection -ConnectedEntityId <String> -GatewayConnectionName <String>
 -GatewayConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>]
 -VirtualNetworkGatewayId <String> [-EnableBgp <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e2cb1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2cb1-105">DESCRIPTION</span></span>
<span data-ttu-id="e2cb1-106">Il cmdlet **New-AzureVirtualNetworkGatewayConnection** crea una connessione di rete Virtual gateway Azure.</span><span class="sxs-lookup"><span data-stu-id="e2cb1-106">The **New-AzureVirtualNetworkGatewayConnection** cmdlet creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="e2cb1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2cb1-107">EXAMPLES</span></span>

## <span data-ttu-id="e2cb1-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2cb1-108">PARAMETERS</span></span>

### <span data-ttu-id="e2cb1-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="e2cb1-109">-ConnectedEntityId</span></span>
<span data-ttu-id="e2cb1-110">Specifica l'ID di un'entità connessa.</span><span class="sxs-lookup"><span data-stu-id="e2cb1-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="e2cb1-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="e2cb1-111">-EnableBgp</span></span>
<span data-ttu-id="e2cb1-112">Abilita il protocollo BGP (Border Gateway Protocol).</span><span class="sxs-lookup"><span data-stu-id="e2cb1-112">Enables Border Gateway Protocol (BGP).</span></span>

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

### <span data-ttu-id="e2cb1-113">-GatewayConnectionName</span><span class="sxs-lookup"><span data-stu-id="e2cb1-113">-GatewayConnectionName</span></span>
<span data-ttu-id="e2cb1-114">Specifica un nome per la connessione al gateway.</span><span class="sxs-lookup"><span data-stu-id="e2cb1-114">Specifies a name for the gateway connection.</span></span>

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

### <span data-ttu-id="e2cb1-115">-GatewayConnectionType</span><span class="sxs-lookup"><span data-stu-id="e2cb1-115">-GatewayConnectionType</span></span>
<span data-ttu-id="e2cb1-116">Specifica il tipo di connessione del gateway.</span><span class="sxs-lookup"><span data-stu-id="e2cb1-116">Specifies the type of gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2cb1-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="e2cb1-117">-Profile</span></span>
<span data-ttu-id="e2cb1-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2cb1-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e2cb1-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e2cb1-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2cb1-120">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="e2cb1-120">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2cb1-121">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="e2cb1-121">-SharedKey</span></span>
<span data-ttu-id="e2cb1-122">Specifica una chiave condivisa.</span><span class="sxs-lookup"><span data-stu-id="e2cb1-122">Specifies a shared key.</span></span>

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

### <span data-ttu-id="e2cb1-123">-VirtualNetworkGatewayId</span><span class="sxs-lookup"><span data-stu-id="e2cb1-123">-VirtualNetworkGatewayId</span></span>
<span data-ttu-id="e2cb1-124">Specifica l'ID di un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2cb1-124">Specifies the ID of a virtual network gateway.</span></span>

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

### <span data-ttu-id="e2cb1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2cb1-125">CommonParameters</span></span>
<span data-ttu-id="e2cb1-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2cb1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2cb1-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2cb1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2cb1-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2cb1-128">INPUTS</span></span>

## <span data-ttu-id="e2cb1-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2cb1-129">OUTPUTS</span></span>

## <span data-ttu-id="e2cb1-130">Note</span><span class="sxs-lookup"><span data-stu-id="e2cb1-130">NOTES</span></span>

## <span data-ttu-id="e2cb1-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2cb1-131">RELATED LINKS</span></span>

[<span data-ttu-id="e2cb1-132">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e2cb1-132">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="e2cb1-133">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e2cb1-133">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="e2cb1-134">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e2cb1-134">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)


