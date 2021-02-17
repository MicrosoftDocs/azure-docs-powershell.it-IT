---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
ms.openlocfilehash: bd419d3b6ec55af885a0f05b7be5c5de269fccdd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193343"
---
# <span data-ttu-id="db5da-101">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="db5da-101">Set-AzRouteTable</span></span>

## <span data-ttu-id="db5da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db5da-102">SYNOPSIS</span></span>
<span data-ttu-id="db5da-103">Aggiorna una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="db5da-103">Updates a route table.</span></span>

## <span data-ttu-id="db5da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db5da-104">SYNTAX</span></span>

```
Set-AzRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db5da-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="db5da-105">DESCRIPTION</span></span>
<span data-ttu-id="db5da-106">Il cmdlet **Set-AzRouteTable** aggiorna una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="db5da-106">The **Set-AzRouteTable** cmdlet updates a route table.</span></span>

## <span data-ttu-id="db5da-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db5da-107">EXAMPLES</span></span>

### <span data-ttu-id="db5da-108">Esempio 1: Aggiornare una tabella di route aggiungendo la configurazione della route</span><span class="sxs-lookup"><span data-stu-id="db5da-108">Example 1: Update a route table by adding route configuration to it</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="db5da-109">Questo comando recupera la tabella di route denominata RouteTable01 usando Get-AzRouteTable cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db5da-109">This command gets the route table named RouteTable01 by using Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="db5da-110">Il comando passa la tabella al cmdlet Add-AzRouteConfig tramite l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="db5da-110">The command passes that table to the Add-AzRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="db5da-111">**Add-AzRouteConfig** aggiunge la route denominata Route07, quindi passa il risultato al cmdlet corrente, che aggiorna la tabella in base alle modifiche apportate.</span><span class="sxs-lookup"><span data-stu-id="db5da-111">**Add-AzRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

### <span data-ttu-id="db5da-112">Esempio 2: Modificare la tabella route</span><span class="sxs-lookup"><span data-stu-id="db5da-112">Example 2: Modify route table</span></span>

```
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
False
PS C:\> $rt.DisableBgpRoutePropagation = $true
PS C:\> Set-AzRouteTable -RouteTable $rt
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
True
```

<span data-ttu-id="db5da-113">Il primo comando ottiene la tabella di route denominata rtName e la archivia nella $rt variabile.</span><span class="sxs-lookup"><span data-stu-id="db5da-113">The first command gets the route table named rtName and stores it in the $rt variable.</span></span>
<span data-ttu-id="db5da-114">Il secondo comando visualizza il valore di DisableBgpRoutePropagation.</span><span class="sxs-lookup"><span data-stu-id="db5da-114">The second command displays the value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="db5da-115">Il terzo comando aggiorna il valore di DisableBgpRoutePropagation.</span><span class="sxs-lookup"><span data-stu-id="db5da-115">The third command updates value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="db5da-116">Il quarto comando aggiorna la tabella di route nel server.</span><span class="sxs-lookup"><span data-stu-id="db5da-116">The fourth command updates route table on the server.</span></span>
<span data-ttu-id="db5da-117">Il quinto comando viene aggiornato nella tabella di route e la archivia nella $rt variabile.</span><span class="sxs-lookup"><span data-stu-id="db5da-117">The fifth command gets updated route table and stores it in the $rt variable.</span></span>
<span data-ttu-id="db5da-118">Il sesto comando visualizza il valore di DisableBgpRoutePropagation.</span><span class="sxs-lookup"><span data-stu-id="db5da-118">The sixth command displays the value of DisableBgpRoutePropagation.</span></span>

## <span data-ttu-id="db5da-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db5da-119">PARAMETERS</span></span>

### <span data-ttu-id="db5da-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db5da-120">-AsJob</span></span>
<span data-ttu-id="db5da-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="db5da-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5da-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db5da-122">-DefaultProfile</span></span>
<span data-ttu-id="db5da-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db5da-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db5da-124">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="db5da-124">-RouteTable</span></span>
<span data-ttu-id="db5da-125">Specifica un oggetto tabella di route che rappresenta lo stato su cui deve essere impostata la tabella di route.</span><span class="sxs-lookup"><span data-stu-id="db5da-125">Specifies a route table object representing the state to which the route table should be set.</span></span>

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

### <span data-ttu-id="db5da-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db5da-126">-Confirm</span></span>
<span data-ttu-id="db5da-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db5da-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db5da-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db5da-128">-WhatIf</span></span>
<span data-ttu-id="db5da-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db5da-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db5da-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db5da-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db5da-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db5da-131">CommonParameters</span></span>
<span data-ttu-id="db5da-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db5da-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db5da-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db5da-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db5da-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="db5da-134">INPUTS</span></span>

### <span data-ttu-id="db5da-135">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="db5da-135">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="db5da-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db5da-136">OUTPUTS</span></span>

### <span data-ttu-id="db5da-137">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="db5da-137">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="db5da-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="db5da-138">NOTES</span></span>

## <span data-ttu-id="db5da-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db5da-139">RELATED LINKS</span></span>

[<span data-ttu-id="db5da-140">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="db5da-140">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="db5da-141">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="db5da-141">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="db5da-142">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="db5da-142">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="db5da-143">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="db5da-143">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)


