---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
ms.openlocfilehash: 7fba74a3778df0c8c26ed4b581e5d2777ff75029
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020546"
---
# <span data-ttu-id="313fc-101">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="313fc-101">Update-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="313fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="313fc-102">SYNOPSIS</span></span>
<span data-ttu-id="313fc-103">Aggiornare una regola di routing allo slot.</span><span class="sxs-lookup"><span data-stu-id="313fc-103">Update a routing Rule to the Slot.</span></span>

## <span data-ttu-id="313fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="313fc-104">SYNTAX</span></span>

```
Update-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="313fc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="313fc-105">DESCRIPTION</span></span>
<span data-ttu-id="313fc-106">Il cmdlet **Update-AzWebAppTrafficRouting** aggiorna la configurazione della regola di routing per uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="313fc-106">The **Update-AzWebAppTrafficRouting** cmdlet updates the routing rule configuration for an Azure Web App Slot.</span></span>

## <span data-ttu-id="313fc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="313fc-107">EXAMPLES</span></span>

### <span data-ttu-id="313fc-108">Esempio 1 aggiornare una regola di routing per trasferire il 15% del traffico di produzione allo slot STG</span><span class="sxs-lookup"><span data-stu-id="313fc-108">Example 1 Update a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
- RoutingRule @{AtionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="313fc-109">Questo comando aggiorna una regola di routing per trasferire il 15% del traffico di produzione allo slot STG.</span><span class="sxs-lookup"><span data-stu-id="313fc-109">This command updates a routing rule to transfer 15% of production traffic to Stg slot.</span></span>

### <span data-ttu-id="313fc-110">Esempio 2 aggiornare una regola di routing per trasferire il traffico di produzione allo slot STG compreso tra 50% e 90% in modo incrementale.</span><span class="sxs-lookup"><span data-stu-id="313fc-110">Example 2 Update a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="313fc-111">Questo comando aggiorna una regola di routing per trasferire il traffico di produzione allo slot STG compreso tra 50% e 90% in modo incrementale.</span><span class="sxs-lookup"><span data-stu-id="313fc-111">This command Updates a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="313fc-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="313fc-112">PARAMETERS</span></span>

### <span data-ttu-id="313fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="313fc-113">-DefaultProfile</span></span>
<span data-ttu-id="313fc-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="313fc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="313fc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="313fc-115">-ResourceGroupName</span></span>
<span data-ttu-id="313fc-116">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="313fc-116">ResourceGroupName</span></span>
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

### <span data-ttu-id="313fc-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="313fc-117">-RoutingRule</span></span>
<span data-ttu-id="313fc-118">Web App RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="313fc-118">Web App RoutingRule.</span></span>
<span data-ttu-id="313fc-119">Esempio:-RoutingRule @ {ActionHostName = $slot. DefaultHostName ReroutePercentage = $ReroutePercentage; Name = $slotName}</span><span class="sxs-lookup"><span data-stu-id="313fc-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313fc-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="313fc-120">-WebAppName</span></span>
<span data-ttu-id="313fc-121">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="313fc-121">WebApp Name</span></span>

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

### <span data-ttu-id="313fc-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="313fc-122">-Confirm</span></span>
<span data-ttu-id="313fc-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="313fc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="313fc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="313fc-124">-WhatIf</span></span>
<span data-ttu-id="313fc-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="313fc-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="313fc-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="313fc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="313fc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="313fc-127">CommonParameters</span></span>
<span data-ttu-id="313fc-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="313fc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="313fc-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="313fc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="313fc-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="313fc-130">INPUTS</span></span>

### <span data-ttu-id="313fc-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="313fc-131">None</span></span>

## <span data-ttu-id="313fc-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="313fc-132">OUTPUTS</span></span>

### <span data-ttu-id="313fc-133">Microsoft. Azure. Management. website. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="313fc-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="313fc-134">Note</span><span class="sxs-lookup"><span data-stu-id="313fc-134">NOTES</span></span>

## <span data-ttu-id="313fc-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="313fc-135">RELATED LINKS</span></span>

[<span data-ttu-id="313fc-136">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="313fc-136">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="313fc-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="313fc-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="313fc-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="313fc-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)