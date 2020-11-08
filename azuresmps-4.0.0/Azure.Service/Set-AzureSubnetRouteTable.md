---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7E40C4A2-8B9A-47E8-82AB-19208247349C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 893e03f8e59b3cd01e7d96ca2d04119ee6fb4c66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023770"
---
# <span data-ttu-id="ac95d-101">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="ac95d-101">Set-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="ac95d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac95d-102">SYNOPSIS</span></span>
<span data-ttu-id="ac95d-103">Associa una tabella di route a una subnet.</span><span class="sxs-lookup"><span data-stu-id="ac95d-103">Associates a route table to a subnet.</span></span>

## <span data-ttu-id="ac95d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac95d-104">SYNTAX</span></span>

```
Set-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> -RouteTableName <String>
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ac95d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac95d-105">DESCRIPTION</span></span>
<span data-ttu-id="ac95d-106">Il cmdlet **set-AzureSubnetRouteTable** associa una tabella di route a una subnet.</span><span class="sxs-lookup"><span data-stu-id="ac95d-106">The **Set-AzureSubnetRouteTable** cmdlet associates a route table to a subnet.</span></span>

## <span data-ttu-id="ac95d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac95d-107">EXAMPLES</span></span>

### <span data-ttu-id="ac95d-108">Esempio 1: associare una tabella di route a una subnet</span><span class="sxs-lookup"><span data-stu-id="ac95d-108">Example 1: Associate a route table to a subnet</span></span>
```
PS C:\> Set-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -RouteTableName "PublicRouteTable"
```

<span data-ttu-id="ac95d-109">Questo comando associa la tabella di route denominata PublicRouteTable alla subnet denominata ContosoSubnet.</span><span class="sxs-lookup"><span data-stu-id="ac95d-109">This command associates the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="ac95d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac95d-110">PARAMETERS</span></span>

### <span data-ttu-id="ac95d-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac95d-111">-PassThru</span></span>
<span data-ttu-id="ac95d-112">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="ac95d-112">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ac95d-113">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="ac95d-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ac95d-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="ac95d-114">-Profile</span></span>
<span data-ttu-id="ac95d-115">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac95d-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ac95d-116">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ac95d-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ac95d-117">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="ac95d-117">-RouteTableName</span></span>
<span data-ttu-id="ac95d-118">Specifica il nome della tabella di route che questo cmdlet associa a una subnet.</span><span class="sxs-lookup"><span data-stu-id="ac95d-118">Specifies the name of the route table that this cmdlet associates with a subnet.</span></span>

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

### <span data-ttu-id="ac95d-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="ac95d-119">-SubnetName</span></span>
<span data-ttu-id="ac95d-120">Specifica la subnet a cui questo cmdlet associa la tabella di route.</span><span class="sxs-lookup"><span data-stu-id="ac95d-120">Specifies the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="ac95d-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ac95d-121">-VirtualNetworkName</span></span>
<span data-ttu-id="ac95d-122">Specifica il nome di una rete virtuale che contiene la subnet a cui questo cmdlet associa la tabella di route.</span><span class="sxs-lookup"><span data-stu-id="ac95d-122">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="ac95d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac95d-123">CommonParameters</span></span>
<span data-ttu-id="ac95d-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac95d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac95d-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac95d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac95d-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac95d-126">INPUTS</span></span>

## <span data-ttu-id="ac95d-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac95d-127">OUTPUTS</span></span>

## <span data-ttu-id="ac95d-128">Note</span><span class="sxs-lookup"><span data-stu-id="ac95d-128">NOTES</span></span>

## <span data-ttu-id="ac95d-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac95d-129">RELATED LINKS</span></span>

[<span data-ttu-id="ac95d-130">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="ac95d-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="ac95d-131">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="ac95d-131">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)
