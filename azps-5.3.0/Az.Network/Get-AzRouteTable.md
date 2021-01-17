---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: 613519f6d9d3d2d8ce1c83ff0ad5a2d9421859b8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487464"
---
# <span data-ttu-id="2b5cc-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="2b5cc-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="2b5cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b5cc-102">SYNOPSIS</span></span>
<span data-ttu-id="2b5cc-103">Ottiene le tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="2b5cc-103">Gets route tables.</span></span>

## <span data-ttu-id="2b5cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b5cc-104">SYNTAX</span></span>

### <span data-ttu-id="2b5cc-105">NOEXPAND (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2b5cc-105">NoExpand (Default)</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b5cc-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="2b5cc-106">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b5cc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b5cc-107">DESCRIPTION</span></span>
<span data-ttu-id="2b5cc-108">Il cmdlet **Get-AzRouteTable** ottiene le tabelle di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b5cc-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="2b5cc-109">È possibile ottenere una singola tabella di route o ottenere tutte le tabelle di route in un gruppo di risorse o nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2b5cc-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="2b5cc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b5cc-110">EXAMPLES</span></span>

### <span data-ttu-id="2b5cc-111">Esempio 1: ottenere una tabella di route</span><span class="sxs-lookup"><span data-stu-id="2b5cc-111">Example 1: Get a route table</span></span>
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

<span data-ttu-id="2b5cc-112">Questo comando consente di ottenere la tabella route denominata RouteTable01 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2b5cc-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="2b5cc-113">Esempio 2: elencare le tabelle di routing tramite filtri</span><span class="sxs-lookup"><span data-stu-id="2b5cc-113">Example 2: List route tables using filtering</span></span>
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

<span data-ttu-id="2b5cc-114">Questo comando consente di ottenere tutte le tabelle di route il cui nome inizia con "RouteTable"</span><span class="sxs-lookup"><span data-stu-id="2b5cc-114">This command gets all route tables whose name starts with "RouteTable"</span></span>

## <span data-ttu-id="2b5cc-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b5cc-115">PARAMETERS</span></span>

### <span data-ttu-id="2b5cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b5cc-116">-DefaultProfile</span></span>
<span data-ttu-id="2b5cc-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b5cc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b5cc-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="2b5cc-118">-ExpandResource</span></span>
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

### <span data-ttu-id="2b5cc-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b5cc-119">-Name</span></span>
<span data-ttu-id="2b5cc-120">Specifica il nome della tabella di route ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b5cc-120">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2b5cc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b5cc-121">-ResourceGroupName</span></span>
<span data-ttu-id="2b5cc-122">Specifica il nome del gruppo di risorse che contiene le tabelle di route ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b5cc-122">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2b5cc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b5cc-123">CommonParameters</span></span>
<span data-ttu-id="2b5cc-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b5cc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b5cc-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b5cc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b5cc-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b5cc-126">INPUTS</span></span>

### <span data-ttu-id="2b5cc-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2b5cc-127">System.String</span></span>

## <span data-ttu-id="2b5cc-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b5cc-128">OUTPUTS</span></span>

### <span data-ttu-id="2b5cc-129">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2b5cc-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="2b5cc-130">Note</span><span class="sxs-lookup"><span data-stu-id="2b5cc-130">NOTES</span></span>

## <span data-ttu-id="2b5cc-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b5cc-131">RELATED LINKS</span></span>

[<span data-ttu-id="2b5cc-132">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="2b5cc-132">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="2b5cc-133">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="2b5cc-133">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="2b5cc-134">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="2b5cc-134">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


