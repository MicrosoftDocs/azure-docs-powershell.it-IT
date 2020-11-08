---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AEFC9094-144F-4E29-AC5A-DBFDA175A920
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8e56496c1fdf04b5227121f5ac39193938a2214e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023500"
---
# <span data-ttu-id="c68b8-101">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="c68b8-101">Get-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="c68b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c68b8-102">SYNOPSIS</span></span>
<span data-ttu-id="c68b8-103">Ottiene una tabella di route per una subnet.</span><span class="sxs-lookup"><span data-stu-id="c68b8-103">Gets a route table for a subnet.</span></span>

## <span data-ttu-id="c68b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c68b8-104">SYNTAX</span></span>

```
Get-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c68b8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c68b8-105">DESCRIPTION</span></span>
<span data-ttu-id="c68b8-106">Il cmdlet **Get-AzureSubnetRouteTable** ottiene la tabella di route associata a una subnet.</span><span class="sxs-lookup"><span data-stu-id="c68b8-106">The **Get-AzureSubnetRouteTable** cmdlet gets the route table that is associated with a subnet.</span></span>

## <span data-ttu-id="c68b8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c68b8-107">EXAMPLES</span></span>

### <span data-ttu-id="c68b8-108">Esempio 1: visualizzare le route per una subnet</span><span class="sxs-lookup"><span data-stu-id="c68b8-108">Example 1: Display routes for a subnet</span></span>
```
PS C:\> Get-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{internetroute}               PublicRT                      Central US                    Sample RT in Central US
```

<span data-ttu-id="c68b8-109">Questo comando Visualizza le route nel nome della tabella route associata alla subnet denominata ContosoSubnet.</span><span class="sxs-lookup"><span data-stu-id="c68b8-109">This command displays the routes in the route table name that is associated with subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="c68b8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c68b8-110">PARAMETERS</span></span>

### <span data-ttu-id="c68b8-111">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="c68b8-111">-Detailed</span></span>
<span data-ttu-id="c68b8-112">Indica che questo cmdlet Visualizza le route nella tabella route associata alla subnet.</span><span class="sxs-lookup"><span data-stu-id="c68b8-112">Indicates that this cmdlet displays the routes in the route table that is associated with the subnet.</span></span>

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

### <span data-ttu-id="c68b8-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="c68b8-113">-Profile</span></span>
<span data-ttu-id="c68b8-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c68b8-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c68b8-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c68b8-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c68b8-116">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="c68b8-116">-SubnetName</span></span>
<span data-ttu-id="c68b8-117">Specifica la subnet per cui questo cmdlet ottiene la tabella di route.</span><span class="sxs-lookup"><span data-stu-id="c68b8-117">Specifies the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="c68b8-118">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c68b8-118">-VirtualNetworkName</span></span>
<span data-ttu-id="c68b8-119">Specifica il nome di una rete virtuale che contiene la subnet per cui questo cmdlet ottiene la tabella di route.</span><span class="sxs-lookup"><span data-stu-id="c68b8-119">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="c68b8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c68b8-120">CommonParameters</span></span>
<span data-ttu-id="c68b8-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c68b8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c68b8-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c68b8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c68b8-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c68b8-123">INPUTS</span></span>

## <span data-ttu-id="c68b8-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c68b8-124">OUTPUTS</span></span>

## <span data-ttu-id="c68b8-125">Note</span><span class="sxs-lookup"><span data-stu-id="c68b8-125">NOTES</span></span>

## <span data-ttu-id="c68b8-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c68b8-126">RELATED LINKS</span></span>

[<span data-ttu-id="c68b8-127">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="c68b8-127">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="c68b8-128">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="c68b8-128">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


