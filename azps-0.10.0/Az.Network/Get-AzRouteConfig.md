---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: a5b80a15711314d5acc4f0288c1fd0304da772fc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860686"
---
# <span data-ttu-id="3dd55-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="3dd55-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="3dd55-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3dd55-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd55-103">Ottiene le route da una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="3dd55-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="3dd55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dd55-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3dd55-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dd55-105">DESCRIPTION</span></span>
<span data-ttu-id="3dd55-106">Il cmdlet **Get-AzRouteConfig** ottiene le route da una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="3dd55-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="3dd55-107">È possibile specificare una route per nome.</span><span class="sxs-lookup"><span data-stu-id="3dd55-107">You can specify a route by name.</span></span>

## <span data-ttu-id="3dd55-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dd55-108">EXAMPLES</span></span>

### <span data-ttu-id="3dd55-109">Esempio 1: ottenere una tabella di route</span><span class="sxs-lookup"><span data-stu-id="3dd55-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="3dd55-110">Questo comando ottiene la tabella route denominata RouteTable01 usando il cmdlet **Get-AzRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="3dd55-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="3dd55-111">Il comando passa la tabella al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="3dd55-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3dd55-112">Il cmdlet corrente ottiene la route denominata Route07 nella tabella route denominata RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="3dd55-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="3dd55-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3dd55-113">PARAMETERS</span></span>

### <span data-ttu-id="3dd55-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd55-114">-DefaultProfile</span></span>
<span data-ttu-id="3dd55-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3dd55-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dd55-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3dd55-116">-Name</span></span>
<span data-ttu-id="3dd55-117">Specifica il nome della route ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dd55-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3dd55-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="3dd55-118">-RouteTable</span></span>
<span data-ttu-id="3dd55-119">Specifica la tabella route da cui questo cmdlet ottiene le route.</span><span class="sxs-lookup"><span data-stu-id="3dd55-119">Specifies the route table from which this cmdlet gets routes.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd55-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd55-120">CommonParameters</span></span>
<span data-ttu-id="3dd55-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dd55-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd55-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dd55-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd55-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3dd55-123">INPUTS</span></span>

### <span data-ttu-id="3dd55-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="3dd55-124">PSRouteTable</span></span>
<span data-ttu-id="3dd55-125">Il parametro ' RouteTable ' accetta il valore di tipo ' PSRouteTable ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3dd55-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="3dd55-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dd55-126">OUTPUTS</span></span>

### <span data-ttu-id="3dd55-127">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="3dd55-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="3dd55-128">Note</span><span class="sxs-lookup"><span data-stu-id="3dd55-128">NOTES</span></span>

## <span data-ttu-id="3dd55-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dd55-129">RELATED LINKS</span></span>

[<span data-ttu-id="3dd55-130">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="3dd55-130">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="3dd55-131">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="3dd55-131">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="3dd55-132">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="3dd55-132">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="3dd55-133">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="3dd55-133">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="3dd55-134">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="3dd55-134">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


