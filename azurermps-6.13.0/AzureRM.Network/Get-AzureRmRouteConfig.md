---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
ms.openlocfilehash: dd23891bc56ac2eb8fce30708d9a72055a567bf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513752"
---
# <span data-ttu-id="efdb3-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="efdb3-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="efdb3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="efdb3-102">SYNOPSIS</span></span>
<span data-ttu-id="efdb3-103">Ottiene le route da una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="efdb3-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efdb3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="efdb3-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="efdb3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efdb3-105">DESCRIPTION</span></span>
<span data-ttu-id="efdb3-106">Il cmdlet **Get-AzureRmRouteConfig** ottiene le route da una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="efdb3-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="efdb3-107">È possibile specificare una route per nome.</span><span class="sxs-lookup"><span data-stu-id="efdb3-107">You can specify a route by name.</span></span>

## <span data-ttu-id="efdb3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="efdb3-108">EXAMPLES</span></span>

### <span data-ttu-id="efdb3-109">Esempio 1: ottenere una tabella di route</span><span class="sxs-lookup"><span data-stu-id="efdb3-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="efdb3-110">Questo comando ottiene la tabella route denominata RouteTable01 usando il cmdlet **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="efdb3-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="efdb3-111">Il comando passa la tabella al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="efdb3-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="efdb3-112">Il cmdlet corrente ottiene la route denominata Route07 nella tabella route denominata RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="efdb3-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="efdb3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="efdb3-113">PARAMETERS</span></span>

### <span data-ttu-id="efdb3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efdb3-114">-DefaultProfile</span></span>
<span data-ttu-id="efdb3-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="efdb3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efdb3-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="efdb3-116">-Name</span></span>
<span data-ttu-id="efdb3-117">Specifica il nome della route ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efdb3-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="efdb3-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="efdb3-118">-RouteTable</span></span>
<span data-ttu-id="efdb3-119">Specifica la tabella route da cui questo cmdlet ottiene le route.</span><span class="sxs-lookup"><span data-stu-id="efdb3-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="efdb3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efdb3-120">CommonParameters</span></span>
<span data-ttu-id="efdb3-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efdb3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efdb3-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efdb3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efdb3-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="efdb3-123">INPUTS</span></span>

### <span data-ttu-id="efdb3-124">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="efdb3-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="efdb3-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="efdb3-125">OUTPUTS</span></span>

### <span data-ttu-id="efdb3-126">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="efdb3-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="efdb3-127">Note</span><span class="sxs-lookup"><span data-stu-id="efdb3-127">NOTES</span></span>

## <span data-ttu-id="efdb3-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="efdb3-128">RELATED LINKS</span></span>

[<span data-ttu-id="efdb3-129">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="efdb3-129">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="efdb3-130">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="efdb3-130">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="efdb3-131">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="efdb3-131">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="efdb3-132">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="efdb3-132">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="efdb3-133">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="efdb3-133">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


