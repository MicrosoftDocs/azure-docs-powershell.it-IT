---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
ms.openlocfilehash: b64fe52b95fb116b08aade300f622b8ea612dcc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521181"
---
# <span data-ttu-id="7b2d6-101">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7b2d6-101">Remove-AzureRmRouteConfig</span></span>

## <span data-ttu-id="7b2d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b2d6-102">SYNOPSIS</span></span>
<span data-ttu-id="7b2d6-103">Consente di rimuovere una route da una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="7b2d6-103">Removes a route from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b2d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b2d6-104">SYNTAX</span></span>

```
Remove-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b2d6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b2d6-105">DESCRIPTION</span></span>
<span data-ttu-id="7b2d6-106">Il cmdlet **Remove-AzureRmRouteConfig** consente di rimuovere una route da una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b2d6-106">The **Remove-AzureRmRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="7b2d6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b2d6-107">EXAMPLES</span></span>

### <span data-ttu-id="7b2d6-108">Esempio 1: rimuovere una route</span><span class="sxs-lookup"><span data-stu-id="7b2d6-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzureRmRouteConfig -Name "Route02" | Set-AzureRmRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"47099b62-60ec-4bc1-b87b-fad56cb8bed1"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"47099b62-60ec-4bc1-b87b-fad56cb8bed1\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="7b2d6-109">Questo comando ottiene la tabella route denominata RouteTable01 usando il cmdlet **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="7b2d6-109">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="7b2d6-110">Il comando passa la tabella al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="7b2d6-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7b2d6-111">Il cmdlet corrente rimuove la route denominata Route02 e passa il risultato al cmdlet **set-AzureRmRouteTable** , che aggiorna la tabella per riflettere le modifiche.</span><span class="sxs-lookup"><span data-stu-id="7b2d6-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="7b2d6-112">La tabella non contiene più la route denominata Route02.</span><span class="sxs-lookup"><span data-stu-id="7b2d6-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="7b2d6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b2d6-113">PARAMETERS</span></span>

### <span data-ttu-id="7b2d6-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b2d6-114">-Name</span></span>
<span data-ttu-id="7b2d6-115">Specifica il nome della route rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b2d6-115">Specifies the name of the route that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b2d6-116">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="7b2d6-116">-RouteTable</span></span>
<span data-ttu-id="7b2d6-117">Specifica la tabella di route che contiene la route eliminata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b2d6-117">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b2d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b2d6-118">-DefaultProfile</span></span>
<span data-ttu-id="7b2d6-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b2d6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b2d6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b2d6-120">CommonParameters</span></span>
<span data-ttu-id="7b2d6-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b2d6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b2d6-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b2d6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b2d6-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b2d6-123">INPUTS</span></span>

### <span data-ttu-id="7b2d6-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="7b2d6-124">PSRouteTable</span></span>
<span data-ttu-id="7b2d6-125">Il parametro ' RouteTable ' accetta il valore di tipo ' PSRouteTable ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7b2d6-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="7b2d6-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b2d6-126">OUTPUTS</span></span>

### <span data-ttu-id="7b2d6-127">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="7b2d6-127">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="7b2d6-128">Note</span><span class="sxs-lookup"><span data-stu-id="7b2d6-128">NOTES</span></span>

## <span data-ttu-id="7b2d6-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b2d6-129">RELATED LINKS</span></span>

[<span data-ttu-id="7b2d6-130">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7b2d6-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="7b2d6-131">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7b2d6-131">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="7b2d6-132">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7b2d6-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="7b2d6-133">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7b2d6-133">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


