---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: fe079282d85b5aea8ebedcf69504fbb0e3dab04b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862937"
---
# <span data-ttu-id="4baed-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4baed-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="4baed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4baed-102">SYNOPSIS</span></span>
<span data-ttu-id="4baed-103">Consente di rimuovere una route da una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="4baed-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="4baed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4baed-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4baed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4baed-105">DESCRIPTION</span></span>
<span data-ttu-id="4baed-106">Il cmdlet **Remove-AzRouteConfig** consente di rimuovere una route da una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="4baed-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="4baed-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4baed-107">EXAMPLES</span></span>

### <span data-ttu-id="4baed-108">Esempio 1: rimuovere una route</span><span class="sxs-lookup"><span data-stu-id="4baed-108">Example 1: Remove a route</span></span>
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

<span data-ttu-id="4baed-109">Questo comando ottiene la tabella route denominata RouteTable01 usando il cmdlet **Get-AzRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="4baed-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="4baed-110">Il comando passa la tabella al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="4baed-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4baed-111">Il cmdlet corrente rimuove la route denominata Route02 e passa il risultato al cmdlet **set-AzRouteTable** , che aggiorna la tabella per riflettere le modifiche.</span><span class="sxs-lookup"><span data-stu-id="4baed-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="4baed-112">La tabella non contiene più la route denominata Route02.</span><span class="sxs-lookup"><span data-stu-id="4baed-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="4baed-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4baed-113">PARAMETERS</span></span>

### <span data-ttu-id="4baed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4baed-114">-DefaultProfile</span></span>
<span data-ttu-id="4baed-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4baed-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4baed-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="4baed-116">-Name</span></span>
<span data-ttu-id="4baed-117">Specifica il nome della route rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4baed-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4baed-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="4baed-118">-RouteTable</span></span>
<span data-ttu-id="4baed-119">Specifica la tabella di route che contiene la route eliminata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4baed-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="4baed-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4baed-120">-Confirm</span></span>
<span data-ttu-id="4baed-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4baed-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4baed-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4baed-122">-WhatIf</span></span>
<span data-ttu-id="4baed-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4baed-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4baed-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4baed-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4baed-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4baed-125">CommonParameters</span></span>
<span data-ttu-id="4baed-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4baed-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4baed-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4baed-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4baed-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4baed-128">INPUTS</span></span>

### <span data-ttu-id="4baed-129">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4baed-129">PSRouteTable</span></span>
<span data-ttu-id="4baed-130">Il parametro ' RouteTable ' accetta il valore di tipo ' PSRouteTable ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="4baed-130">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="4baed-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4baed-131">OUTPUTS</span></span>

### <span data-ttu-id="4baed-132">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4baed-132">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="4baed-133">Note</span><span class="sxs-lookup"><span data-stu-id="4baed-133">NOTES</span></span>

## <span data-ttu-id="4baed-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4baed-134">RELATED LINKS</span></span>

[<span data-ttu-id="4baed-135">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4baed-135">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="4baed-136">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4baed-136">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="4baed-137">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4baed-137">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="4baed-138">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4baed-138">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


