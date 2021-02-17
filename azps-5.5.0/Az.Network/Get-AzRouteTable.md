---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: 613519f6d9d3d2d8ce1c83ff0ad5a2d9421859b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184662"
---
# <span data-ttu-id="5880b-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="5880b-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="5880b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5880b-102">SYNOPSIS</span></span>
<span data-ttu-id="5880b-103">Ottiene le tabelle delle route.</span><span class="sxs-lookup"><span data-stu-id="5880b-103">Gets route tables.</span></span>

## <span data-ttu-id="5880b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5880b-104">SYNTAX</span></span>

### <span data-ttu-id="5880b-105">NoExpand (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5880b-105">NoExpand (Default)</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5880b-106">Espandi</span><span class="sxs-lookup"><span data-stu-id="5880b-106">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5880b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5880b-107">DESCRIPTION</span></span>
<span data-ttu-id="5880b-108">Il cmdlet **Get-AzRouteTable** ottiene le tabelle delle route di Azure.</span><span class="sxs-lookup"><span data-stu-id="5880b-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="5880b-109">È possibile ottenere una singola tabella di route oppure tutte le tabelle di route in un gruppo di risorse o nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="5880b-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="5880b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5880b-110">EXAMPLES</span></span>

### <span data-ttu-id="5880b-111">Esempio 1: Ottenere una tabella di route</span><span class="sxs-lookup"><span data-stu-id="5880b-111">Example 1: Get a route table</span></span>
```
PS C:\> Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"

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

<span data-ttu-id="5880b-112">Questo comando recupera la tabella di route denominata RouteTable01 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5880b-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="5880b-113">Esempio 2: Elencare le tabelle delle route usando i filtri</span><span class="sxs-lookup"><span data-stu-id="5880b-113">Example 2: List route tables using filtering</span></span>
```
PS C:\> Get-AzRouteTable -Name RouteTable*

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

Name              : routetable02
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable02
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable02/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="5880b-114">Questo comando recupera tutte le tabelle di route il cui nome inizia con "Tabella Route"</span><span class="sxs-lookup"><span data-stu-id="5880b-114">This command gets all route tables whose name starts with "RouteTable"</span></span>

## <span data-ttu-id="5880b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5880b-115">PARAMETERS</span></span>

### <span data-ttu-id="5880b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5880b-116">-DefaultProfile</span></span>
<span data-ttu-id="5880b-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5880b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5880b-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="5880b-118">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5880b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5880b-119">-Name</span></span>
<span data-ttu-id="5880b-120">Specifica il nome della tabella di route che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5880b-120">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="5880b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5880b-121">-ResourceGroupName</span></span>
<span data-ttu-id="5880b-122">Specifica il nome del gruppo di risorse che contiene le tabelle di route recuperate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5880b-122">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="5880b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5880b-123">CommonParameters</span></span>
<span data-ttu-id="5880b-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5880b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5880b-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5880b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5880b-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="5880b-126">INPUTS</span></span>

### <span data-ttu-id="5880b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5880b-127">System.String</span></span>

## <span data-ttu-id="5880b-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5880b-128">OUTPUTS</span></span>

### <span data-ttu-id="5880b-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="5880b-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="5880b-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="5880b-130">NOTES</span></span>

## <span data-ttu-id="5880b-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5880b-131">RELATED LINKS</span></span>

[<span data-ttu-id="5880b-132">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="5880b-132">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="5880b-133">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="5880b-133">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="5880b-134">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="5880b-134">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


