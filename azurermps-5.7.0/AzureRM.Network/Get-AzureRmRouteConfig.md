---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
ms.openlocfilehash: f00a1d0c67d7bb395a328e01915f5bb0334d3d83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511115"
---
# <span data-ttu-id="3245b-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="3245b-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="3245b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3245b-102">SYNOPSIS</span></span>
<span data-ttu-id="3245b-103">Ottiene le route da una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="3245b-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3245b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3245b-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3245b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3245b-105">DESCRIPTION</span></span>
<span data-ttu-id="3245b-106">Il cmdlet **Get-AzureRmRouteConfig** ottiene le route da una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="3245b-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="3245b-107">È possibile specificare una route per nome.</span><span class="sxs-lookup"><span data-stu-id="3245b-107">You can specify a route by name.</span></span>

## <span data-ttu-id="3245b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3245b-108">EXAMPLES</span></span>

### <span data-ttu-id="3245b-109">Esempio 1: ottenere una tabella di route</span><span class="sxs-lookup"><span data-stu-id="3245b-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzureRmRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="3245b-110">Questo comando ottiene la tabella route denominata RouteTable01 usando il cmdlet **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="3245b-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="3245b-111">Il comando passa la tabella al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="3245b-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3245b-112">Il cmdlet corrente ottiene la route denominata Route07 nella tabella route denominata RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="3245b-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="3245b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3245b-113">PARAMETERS</span></span>

### <span data-ttu-id="3245b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3245b-114">-DefaultProfile</span></span>
<span data-ttu-id="3245b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3245b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3245b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3245b-116">-Name</span></span>
<span data-ttu-id="3245b-117">Specifica il nome della route ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3245b-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3245b-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="3245b-118">-RouteTable</span></span>
<span data-ttu-id="3245b-119">Specifica la tabella route da cui questo cmdlet ottiene le route.</span><span class="sxs-lookup"><span data-stu-id="3245b-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="3245b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3245b-120">CommonParameters</span></span>
<span data-ttu-id="3245b-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3245b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3245b-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3245b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3245b-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3245b-123">INPUTS</span></span>

### <span data-ttu-id="3245b-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="3245b-124">PSRouteTable</span></span>
<span data-ttu-id="3245b-125">Il parametro ' RouteTable ' accetta il valore di tipo ' PSRouteTable ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3245b-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="3245b-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3245b-126">OUTPUTS</span></span>

### <span data-ttu-id="3245b-127">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="3245b-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="3245b-128">Note</span><span class="sxs-lookup"><span data-stu-id="3245b-128">NOTES</span></span>

## <span data-ttu-id="3245b-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3245b-129">RELATED LINKS</span></span>

[<span data-ttu-id="3245b-130">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="3245b-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="3245b-131">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="3245b-131">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="3245b-132">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="3245b-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="3245b-133">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="3245b-133">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="3245b-134">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="3245b-134">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


