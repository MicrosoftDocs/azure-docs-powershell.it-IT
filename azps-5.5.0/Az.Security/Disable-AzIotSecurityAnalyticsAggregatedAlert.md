---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 3747109d13fd4224b0f86bc5ecf2992ed4229487
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178662"
---
# <span data-ttu-id="31282-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="31282-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="31282-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31282-102">SYNOPSIS</span></span>
<span data-ttu-id="31282-103">Ignora avviso Iot aggregato</span><span class="sxs-lookup"><span data-stu-id="31282-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="31282-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31282-104">SYNTAX</span></span>

### <span data-ttu-id="31282-105">SolutionLevelResource (Default)</span><span class="sxs-lookup"><span data-stu-id="31282-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31282-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="31282-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31282-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="31282-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31282-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="31282-108">DESCRIPTION</span></span>
<span data-ttu-id="31282-109">Il cmdlet Disable-AzIotSecurityAnalyticsAggregatedAlert ignora uno specifico avviso attivato nei dispositivi dell'hub iot.</span><span class="sxs-lookup"><span data-stu-id="31282-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="31282-110">Il nome degli avvisi aggregati è una combinazione del tipo di avviso e della data dell'avviso, separati da "/".</span><span class="sxs-lookup"><span data-stu-id="31282-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="31282-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31282-111">EXAMPLES</span></span>

### <span data-ttu-id="31282-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="31282-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="31282-113">Ignorare l'avviso aggregato "IoT_SucessfulLocalLogin/2020-03-15" (nome combinato dal tipo di avviso e dalla data aggregata) dalla soluzione di sicurezza IoT "MySolutionName" nel gruppo di risorse "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="31282-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="31282-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="31282-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="31282-115">Ignorare l'avviso aggregato con ID risorsa "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span><span class="sxs-lookup"><span data-stu-id="31282-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="31282-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31282-116">PARAMETERS</span></span>

### <span data-ttu-id="31282-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31282-117">-DefaultProfile</span></span>
<span data-ttu-id="31282-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31282-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31282-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31282-119">-InputObject</span></span>
<span data-ttu-id="31282-120">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="31282-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31282-121">-Name</span><span class="sxs-lookup"><span data-stu-id="31282-121">-Name</span></span>
<span data-ttu-id="31282-122">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="31282-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31282-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31282-123">-PassThru</span></span>
<span data-ttu-id="31282-124">Restituisce se l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="31282-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="31282-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31282-125">-ResourceGroupName</span></span>
<span data-ttu-id="31282-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="31282-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31282-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31282-127">-ResourceId</span></span>
<span data-ttu-id="31282-128">ID della risorsa di sicurezza su cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="31282-128">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31282-129">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="31282-129">-SolutionName</span></span>
<span data-ttu-id="31282-130">Nome della soluzione</span><span class="sxs-lookup"><span data-stu-id="31282-130">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31282-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31282-131">-Confirm</span></span>
<span data-ttu-id="31282-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31282-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31282-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31282-133">-WhatIf</span></span>
<span data-ttu-id="31282-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31282-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31282-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31282-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31282-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31282-136">CommonParameters</span></span>
<span data-ttu-id="31282-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31282-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31282-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="31282-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31282-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="31282-139">INPUTS</span></span>

### <span data-ttu-id="31282-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="31282-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="31282-141">System.String</span><span class="sxs-lookup"><span data-stu-id="31282-141">System.String</span></span>

## <span data-ttu-id="31282-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31282-142">OUTPUTS</span></span>

### <span data-ttu-id="31282-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="31282-143">System.Boolean</span></span>

## <span data-ttu-id="31282-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="31282-144">NOTES</span></span>

## <span data-ttu-id="31282-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31282-145">RELATED LINKS</span></span>
