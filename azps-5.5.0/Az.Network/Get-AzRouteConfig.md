---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 0d941289f0798854a3647bcb5fbf4d1e6be1053d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203068"
---
# <span data-ttu-id="33081-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="33081-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="33081-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33081-102">SYNOPSIS</span></span>
<span data-ttu-id="33081-103">Ottiene i percorsi da una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="33081-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="33081-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33081-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33081-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="33081-105">DESCRIPTION</span></span>
<span data-ttu-id="33081-106">Il cmdlet **Get-AzRouteConfig** ottiene le route da una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="33081-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="33081-107">È possibile specificare una route in base al nome.</span><span class="sxs-lookup"><span data-stu-id="33081-107">You can specify a route by name.</span></span>

## <span data-ttu-id="33081-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33081-108">EXAMPLES</span></span>

### <span data-ttu-id="33081-109">Esempio 1: Ottenere una tabella di route</span><span class="sxs-lookup"><span data-stu-id="33081-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="33081-110">Questo comando recupera la tabella di route denominata RouteTable01 usando il cmdlet **Get-AzRouteTable.**</span><span class="sxs-lookup"><span data-stu-id="33081-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="33081-111">Il comando passa la tabella al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="33081-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="33081-112">Il cmdlet corrente ottiene la route denominata Route07 nella tabella di route denominata RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="33081-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="33081-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33081-113">PARAMETERS</span></span>

### <span data-ttu-id="33081-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33081-114">-DefaultProfile</span></span>
<span data-ttu-id="33081-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33081-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33081-116">-Name</span><span class="sxs-lookup"><span data-stu-id="33081-116">-Name</span></span>
<span data-ttu-id="33081-117">Specifica il nome della route che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33081-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="33081-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="33081-118">-RouteTable</span></span>
<span data-ttu-id="33081-119">Specifica la tabella di route da cui questo cmdlet ottiene le route.</span><span class="sxs-lookup"><span data-stu-id="33081-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="33081-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33081-120">CommonParameters</span></span>
<span data-ttu-id="33081-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33081-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33081-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="33081-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33081-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="33081-123">INPUTS</span></span>

### <span data-ttu-id="33081-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="33081-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="33081-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33081-125">OUTPUTS</span></span>

### <span data-ttu-id="33081-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span><span class="sxs-lookup"><span data-stu-id="33081-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="33081-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="33081-127">NOTES</span></span>

## <span data-ttu-id="33081-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33081-128">RELATED LINKS</span></span>

[<span data-ttu-id="33081-129">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="33081-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="33081-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="33081-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="33081-131">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="33081-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="33081-132">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="33081-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="33081-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="33081-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


