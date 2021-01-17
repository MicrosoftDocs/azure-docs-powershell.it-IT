---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 0d941289f0798854a3647bcb5fbf4d1e6be1053d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487471"
---
# <span data-ttu-id="5a315-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="5a315-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="5a315-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a315-102">SYNOPSIS</span></span>
<span data-ttu-id="5a315-103">Ottiene le route da una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="5a315-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="5a315-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a315-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a315-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a315-105">DESCRIPTION</span></span>
<span data-ttu-id="5a315-106">Il cmdlet **Get-AzRouteConfig** ottiene le route da una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a315-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="5a315-107">È possibile specificare una route per nome.</span><span class="sxs-lookup"><span data-stu-id="5a315-107">You can specify a route by name.</span></span>

## <span data-ttu-id="5a315-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a315-108">EXAMPLES</span></span>

### <span data-ttu-id="5a315-109">Esempio 1: ottenere una tabella di route</span><span class="sxs-lookup"><span data-stu-id="5a315-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="5a315-110">Questo comando ottiene la tabella route denominata RouteTable01 usando il cmdlet **Get-AzRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="5a315-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="5a315-111">Il comando passa la tabella al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="5a315-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5a315-112">Il cmdlet corrente ottiene la route denominata Route07 nella tabella route denominata RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="5a315-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="5a315-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a315-113">PARAMETERS</span></span>

### <span data-ttu-id="5a315-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a315-114">-DefaultProfile</span></span>
<span data-ttu-id="5a315-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a315-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a315-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a315-116">-Name</span></span>
<span data-ttu-id="5a315-117">Specifica il nome della route ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a315-117">Specifies the name of the route that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a315-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="5a315-118">-RouteTable</span></span>
<span data-ttu-id="5a315-119">Specifica la tabella route da cui questo cmdlet ottiene le route.</span><span class="sxs-lookup"><span data-stu-id="5a315-119">Specifies the route table from which this cmdlet gets routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a315-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a315-120">CommonParameters</span></span>
<span data-ttu-id="5a315-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a315-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a315-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a315-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a315-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a315-123">INPUTS</span></span>

### <span data-ttu-id="5a315-124">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="5a315-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="5a315-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a315-125">OUTPUTS</span></span>

### <span data-ttu-id="5a315-126">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="5a315-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="5a315-127">Note</span><span class="sxs-lookup"><span data-stu-id="5a315-127">NOTES</span></span>

## <span data-ttu-id="5a315-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a315-128">RELATED LINKS</span></span>

[<span data-ttu-id="5a315-129">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="5a315-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="5a315-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="5a315-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="5a315-131">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="5a315-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="5a315-132">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="5a315-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="5a315-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="5a315-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


