---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 8a3949397b12b54062c5cc68f367187f691fb02d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182518"
---
# <span data-ttu-id="625c8-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="625c8-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="625c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="625c8-102">SYNOPSIS</span></span>
<span data-ttu-id="625c8-103">Aggiungere una regola di routing nello slot.</span><span class="sxs-lookup"><span data-stu-id="625c8-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="625c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="625c8-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="625c8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="625c8-105">DESCRIPTION</span></span>
<span data-ttu-id="625c8-106">Il cmdlet **Add-AzWebAppTrafficRouting aggiunge** una regola di routing a uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="625c8-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="625c8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="625c8-107">EXAMPLES</span></span>

### <span data-ttu-id="625c8-108">Esempio 1 Aggiungere una regola di routing per trasferire il 15% del traffico di produzione nello slot Stg</span><span class="sxs-lookup"><span data-stu-id="625c8-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="625c8-109">Questo comando aggiunge una regola di routing per trasferire il 15% del traffico di produzione nello slot Stg</span><span class="sxs-lookup"><span data-stu-id="625c8-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="625c8-110">Esempio 2 Aggiungere una regola di routing per trasferire il traffico di produzione agli intervalli di slot Stg dal 50% al 90% in modo incrementale.</span><span class="sxs-lookup"><span data-stu-id="625c8-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="625c8-111">Questo comando aggiunge una regola di routing per trasferire il traffico di produzione agli intervalli di slot Stg dal 50% al 90% in modo incrementale.</span><span class="sxs-lookup"><span data-stu-id="625c8-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="625c8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="625c8-112">PARAMETERS</span></span>

### <span data-ttu-id="625c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="625c8-113">-DefaultProfile</span></span>
<span data-ttu-id="625c8-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="625c8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="625c8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="625c8-115">-ResourceGroupName</span></span>
<span data-ttu-id="625c8-116">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="625c8-116">Resource Group Name</span></span>

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

### <span data-ttu-id="625c8-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="625c8-117">-RoutingRule</span></span>
<span data-ttu-id="625c8-118">RoutingRule di Web App.</span><span class="sxs-lookup"><span data-stu-id="625c8-118">Web App RoutingRule.</span></span>
<span data-ttu-id="625c8-119">Esempio: -RoutingRule @{ActionHostName=$slot. DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span><span class="sxs-lookup"><span data-stu-id="625c8-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="625c8-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="625c8-120">-WebAppName</span></span>
<span data-ttu-id="625c8-121">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="625c8-121">WebApp Name</span></span>

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

### <span data-ttu-id="625c8-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="625c8-122">-Confirm</span></span>
<span data-ttu-id="625c8-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="625c8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="625c8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="625c8-124">-WhatIf</span></span>
<span data-ttu-id="625c8-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="625c8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="625c8-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="625c8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="625c8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="625c8-127">CommonParameters</span></span>
<span data-ttu-id="625c8-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="625c8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="625c8-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="625c8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="625c8-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="625c8-130">INPUTS</span></span>

### <span data-ttu-id="625c8-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="625c8-131">None</span></span>

## <span data-ttu-id="625c8-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="625c8-132">OUTPUTS</span></span>

### <span data-ttu-id="625c8-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="625c8-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="625c8-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="625c8-134">NOTES</span></span>

## <span data-ttu-id="625c8-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="625c8-135">RELATED LINKS</span></span>
[<span data-ttu-id="625c8-136">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="625c8-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="625c8-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="625c8-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="625c8-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="625c8-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
