---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: 9498b93d2062bc84d6af423c89eb351c6680eddd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865909"
---
# <span data-ttu-id="b3cda-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="b3cda-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="b3cda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3cda-102">SYNOPSIS</span></span>
<span data-ttu-id="b3cda-103">Ottiene le tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="b3cda-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3cda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3cda-104">SYNTAX</span></span>

### <span data-ttu-id="b3cda-105">Espandere</span><span class="sxs-lookup"><span data-stu-id="b3cda-105">Expand</span></span>
```
Get-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3cda-106">NoExpand</span><span class="sxs-lookup"><span data-stu-id="b3cda-106">NoExpand</span></span>
```
Get-AzureRmRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3cda-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3cda-107">DESCRIPTION</span></span>
<span data-ttu-id="b3cda-108">Il cmdlet **Get-AzureRmRouteTable** ottiene le tabelle di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="b3cda-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="b3cda-109">È possibile ottenere una singola tabella di route o ottenere tutte le tabelle di route in un gruppo di risorse o nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b3cda-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="b3cda-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3cda-110">EXAMPLES</span></span>

### <span data-ttu-id="b3cda-111">Esempio 1: ottenere una tabella di route</span><span class="sxs-lookup"><span data-stu-id="b3cda-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="b3cda-112">Questo comando consente di ottenere la tabella route denominata RouteTable01 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b3cda-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="b3cda-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3cda-113">PARAMETERS</span></span>

### <span data-ttu-id="b3cda-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3cda-114">-DefaultProfile</span></span>
<span data-ttu-id="b3cda-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3cda-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3cda-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="b3cda-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3cda-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3cda-117">-Name</span></span>
<span data-ttu-id="b3cda-118">Specifica il nome della tabella di route ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3cda-118">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3cda-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3cda-119">-ResourceGroupName</span></span>
<span data-ttu-id="b3cda-120">Specifica il nome del gruppo di risorse che contiene le tabelle di route ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3cda-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3cda-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3cda-121">CommonParameters</span></span>
<span data-ttu-id="b3cda-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3cda-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3cda-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3cda-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3cda-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3cda-124">INPUTS</span></span>

## <span data-ttu-id="b3cda-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3cda-125">OUTPUTS</span></span>

### <span data-ttu-id="b3cda-126">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="b3cda-126">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="b3cda-127">Note</span><span class="sxs-lookup"><span data-stu-id="b3cda-127">NOTES</span></span>

## <span data-ttu-id="b3cda-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3cda-128">RELATED LINKS</span></span>

[<span data-ttu-id="b3cda-129">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="b3cda-129">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="b3cda-130">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="b3cda-130">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="b3cda-131">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="b3cda-131">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


