---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteTable.md
ms.openlocfilehash: 531c2724289e90f92bf14347518d53b6208be932
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862722"
---
# <span data-ttu-id="41bb7-101">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="41bb7-101">Set-AzRouteTable</span></span>

## <span data-ttu-id="41bb7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="41bb7-102">SYNOPSIS</span></span>
<span data-ttu-id="41bb7-103">Imposta lo stato dell'obiettivo per una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="41bb7-103">Sets the goal state for a route table.</span></span>

## <span data-ttu-id="41bb7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41bb7-104">SYNTAX</span></span>

```
Set-AzRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41bb7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41bb7-105">DESCRIPTION</span></span>
<span data-ttu-id="41bb7-106">Il cmdlet **set-AzRouteTable** imposta lo stato dell'obiettivo per una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="41bb7-106">The **Set-AzRouteTable** cmdlet sets the goal state for an Azure route table.</span></span>

## <span data-ttu-id="41bb7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41bb7-107">EXAMPLES</span></span>

### <span data-ttu-id="41bb7-108">Esempio 1: aggiungere una route e quindi impostare lo stato obiettivo della tabella route</span><span class="sxs-lookup"><span data-stu-id="41bb7-108">Example 1: Add a route and then set the goal state of the route table</span></span>
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

<span data-ttu-id="41bb7-109">Questo comando consente di ottenere la tabella route denominata RouteTable01 usando il cmdlet Get-AzRouteTable.</span><span class="sxs-lookup"><span data-stu-id="41bb7-109">This command gets the route table named RouteTable01 by using Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="41bb7-110">Il comando passa la tabella al cmdlet Add-AzRouteConfig usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="41bb7-110">The command passes that table to the Add-AzRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="41bb7-111">**Add-AzRouteConfig** aggiunge la route denominata Route07 e quindi passa il risultato al cmdlet corrente, che aggiorna la tabella per riflettere le modifiche.</span><span class="sxs-lookup"><span data-stu-id="41bb7-111">**Add-AzRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="41bb7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="41bb7-112">PARAMETERS</span></span>

### <span data-ttu-id="41bb7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41bb7-113">-AsJob</span></span>
<span data-ttu-id="41bb7-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="41bb7-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41bb7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41bb7-115">-DefaultProfile</span></span>
<span data-ttu-id="41bb7-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41bb7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41bb7-117">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="41bb7-117">-RouteTable</span></span>
<span data-ttu-id="41bb7-118">Specifica un oggetto tabella route che rappresenta lo stato dell'obiettivo a cui questo cmdlet imposta la tabella di route.</span><span class="sxs-lookup"><span data-stu-id="41bb7-118">Specifies a route table object that represents the goal state to which this cmdlet sets the route table.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41bb7-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="41bb7-119">-Confirm</span></span>
<span data-ttu-id="41bb7-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41bb7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41bb7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41bb7-121">-WhatIf</span></span>
<span data-ttu-id="41bb7-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41bb7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41bb7-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41bb7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41bb7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41bb7-124">CommonParameters</span></span>
<span data-ttu-id="41bb7-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41bb7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41bb7-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41bb7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41bb7-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="41bb7-127">INPUTS</span></span>

### <span data-ttu-id="41bb7-128">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="41bb7-128">PSRouteTable</span></span>
<span data-ttu-id="41bb7-129">Il parametro ' RouteTable ' accetta il valore di tipo ' PSRouteTable ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="41bb7-129">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="41bb7-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41bb7-130">OUTPUTS</span></span>

### <span data-ttu-id="41bb7-131">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="41bb7-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="41bb7-132">Note</span><span class="sxs-lookup"><span data-stu-id="41bb7-132">NOTES</span></span>

## <span data-ttu-id="41bb7-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41bb7-133">RELATED LINKS</span></span>

[<span data-ttu-id="41bb7-134">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="41bb7-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="41bb7-135">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="41bb7-135">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="41bb7-136">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="41bb7-136">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="41bb7-137">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="41bb7-137">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)


