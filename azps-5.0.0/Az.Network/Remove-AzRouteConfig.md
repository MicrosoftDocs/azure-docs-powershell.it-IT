---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: 57ef72599cdb0500a9903aeb09f67437fe5cc2f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311388"
---
# <span data-ttu-id="85dca-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="85dca-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="85dca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85dca-102">SYNOPSIS</span></span>
<span data-ttu-id="85dca-103">Consente di rimuovere una route da una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="85dca-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="85dca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85dca-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85dca-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85dca-105">DESCRIPTION</span></span>
<span data-ttu-id="85dca-106">Il cmdlet **Remove-AzRouteConfig** consente di rimuovere una route da una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="85dca-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="85dca-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85dca-107">EXAMPLES</span></span>

### <span data-ttu-id="85dca-108">Esempio 1: rimuovere una route</span><span class="sxs-lookup"><span data-stu-id="85dca-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzRouteConfig -Name "Route02" | Set-AzRouteTable
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

<span data-ttu-id="85dca-109">Questo comando ottiene la tabella route denominata RouteTable01 usando il cmdlet **Get-AzRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="85dca-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="85dca-110">Il comando passa la tabella al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="85dca-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="85dca-111">Il cmdlet corrente rimuove la route denominata Route02 e passa il risultato al cmdlet **set-AzRouteTable** , che aggiorna la tabella per riflettere le modifiche.</span><span class="sxs-lookup"><span data-stu-id="85dca-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="85dca-112">La tabella non contiene più la route denominata Route02.</span><span class="sxs-lookup"><span data-stu-id="85dca-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="85dca-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85dca-113">PARAMETERS</span></span>

### <span data-ttu-id="85dca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85dca-114">-DefaultProfile</span></span>
<span data-ttu-id="85dca-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85dca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85dca-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="85dca-116">-Name</span></span>
<span data-ttu-id="85dca-117">Specifica il nome della route rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85dca-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="85dca-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="85dca-118">-RouteTable</span></span>
<span data-ttu-id="85dca-119">Specifica la tabella di route che contiene la route eliminata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85dca-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="85dca-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="85dca-120">-Confirm</span></span>
<span data-ttu-id="85dca-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85dca-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85dca-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85dca-122">-WhatIf</span></span>
<span data-ttu-id="85dca-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85dca-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85dca-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85dca-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85dca-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85dca-125">CommonParameters</span></span>
<span data-ttu-id="85dca-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85dca-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85dca-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85dca-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85dca-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85dca-128">INPUTS</span></span>

### <span data-ttu-id="85dca-129">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="85dca-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="85dca-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85dca-130">OUTPUTS</span></span>

### <span data-ttu-id="85dca-131">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="85dca-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="85dca-132">Note</span><span class="sxs-lookup"><span data-stu-id="85dca-132">NOTES</span></span>

## <span data-ttu-id="85dca-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85dca-133">RELATED LINKS</span></span>

[<span data-ttu-id="85dca-134">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="85dca-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="85dca-135">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="85dca-135">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="85dca-136">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="85dca-136">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="85dca-137">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="85dca-137">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


