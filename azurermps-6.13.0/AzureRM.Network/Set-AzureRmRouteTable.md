---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
ms.openlocfilehash: e94eaeb7c9b4302c0d7e5e1f89496939a612d4d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518623"
---
# <span data-ttu-id="4c20a-101">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4c20a-101">Set-AzureRmRouteTable</span></span>

## <span data-ttu-id="4c20a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c20a-102">SYNOPSIS</span></span>
<span data-ttu-id="4c20a-103">Imposta lo stato dell'obiettivo per una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="4c20a-103">Sets the goal state for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c20a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c20a-104">SYNTAX</span></span>

```
Set-AzureRmRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c20a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c20a-105">DESCRIPTION</span></span>
<span data-ttu-id="4c20a-106">Il cmdlet **set-AzureRmRouteTable** imposta lo stato dell'obiettivo per una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c20a-106">The **Set-AzureRmRouteTable** cmdlet sets the goal state for an Azure route table.</span></span>

## <span data-ttu-id="4c20a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c20a-107">EXAMPLES</span></span>

### <span data-ttu-id="4c20a-108">Esempio 1: aggiungere una route e quindi impostare lo stato obiettivo della tabella route</span><span class="sxs-lookup"><span data-stu-id="4c20a-108">Example 1: Add a route and then set the goal state of the route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzureRmRouteTable
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

<span data-ttu-id="4c20a-109">Questo comando consente di ottenere la tabella route denominata RouteTable01 usando il cmdlet Get-AzureRmRouteTable.</span><span class="sxs-lookup"><span data-stu-id="4c20a-109">This command gets the route table named RouteTable01 by using Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="4c20a-110">Il comando passa la tabella al cmdlet Add-AzureRmRouteConfig usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="4c20a-110">The command passes that table to the Add-AzureRmRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4c20a-111">**Add-AzureRmRouteConfig** aggiunge la route denominata Route07 e quindi passa il risultato al cmdlet corrente, che aggiorna la tabella per riflettere le modifiche.</span><span class="sxs-lookup"><span data-stu-id="4c20a-111">**Add-AzureRmRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="4c20a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c20a-112">PARAMETERS</span></span>

### <span data-ttu-id="4c20a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c20a-113">-AsJob</span></span>
<span data-ttu-id="4c20a-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4c20a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c20a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c20a-115">-DefaultProfile</span></span>
<span data-ttu-id="4c20a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c20a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c20a-117">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="4c20a-117">-RouteTable</span></span>
<span data-ttu-id="4c20a-118">Specifica un oggetto tabella route che rappresenta lo stato dell'obiettivo a cui questo cmdlet imposta la tabella di route.</span><span class="sxs-lookup"><span data-stu-id="4c20a-118">Specifies a route table object that represents the goal state to which this cmdlet sets the route table.</span></span>

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

### <span data-ttu-id="4c20a-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4c20a-119">-Confirm</span></span>
<span data-ttu-id="4c20a-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c20a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c20a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c20a-121">-WhatIf</span></span>
<span data-ttu-id="4c20a-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c20a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c20a-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c20a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c20a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c20a-124">CommonParameters</span></span>
<span data-ttu-id="4c20a-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c20a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c20a-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c20a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c20a-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c20a-127">INPUTS</span></span>

### <span data-ttu-id="4c20a-128">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4c20a-128">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>
<span data-ttu-id="4c20a-129">Parametri: RouteTable (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4c20a-129">Parameters: RouteTable (ByValue)</span></span>

## <span data-ttu-id="4c20a-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c20a-130">OUTPUTS</span></span>

### <span data-ttu-id="4c20a-131">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4c20a-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="4c20a-132">Note</span><span class="sxs-lookup"><span data-stu-id="4c20a-132">NOTES</span></span>

## <span data-ttu-id="4c20a-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c20a-133">RELATED LINKS</span></span>

[<span data-ttu-id="4c20a-134">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4c20a-134">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="4c20a-135">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4c20a-135">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="4c20a-136">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4c20a-136">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="4c20a-137">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4c20a-137">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

