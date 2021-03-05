---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: ce4c9d8fd297b53eb628ffcc32ad9479e0647dd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014333"
---
# <span data-ttu-id="0d412-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="0d412-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="0d412-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d412-102">SYNOPSIS</span></span>
<span data-ttu-id="0d412-103">Impostare il limite giornaliero del volume dei dati per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="0d412-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="0d412-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d412-104">SYNTAX</span></span>

### <span data-ttu-id="0d412-105">ComponentNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="0d412-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d412-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d412-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d412-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d412-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d412-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0d412-108">DESCRIPTION</span></span>
<span data-ttu-id="0d412-109">Impostare il limite giornaliero del volume dei dati per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="0d412-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="0d412-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d412-110">EXAMPLES</span></span>

### <span data-ttu-id="0d412-111">Esempio 1: impostare il limite del volume dei dati giornalieri per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="0d412-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="0d412-112">Impostare il limite giornaliero del volume dei dati su 400 GB al giorno e interrompere l'invio della notifica quando viene raggiunto il limite per la risorsa "test" nel gruppo di risorse "gruppo di test"</span><span class="sxs-lookup"><span data-stu-id="0d412-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="0d412-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d412-113">PARAMETERS</span></span>

### <span data-ttu-id="0d412-114">-ApplicationInsightsInsightsIn</span><span class="sxs-lookup"><span data-stu-id="0d412-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="0d412-115">Application Insights Component Object.</span><span class="sxs-lookup"><span data-stu-id="0d412-115">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d412-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="0d412-116">-DailyCapGB</span></span>
<span data-ttu-id="0d412-117">Limite giornaliero.</span><span class="sxs-lookup"><span data-stu-id="0d412-117">Daily Cap.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d412-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d412-118">-DefaultProfile</span></span>
<span data-ttu-id="0d412-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d412-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d412-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="0d412-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="0d412-121">Interrompi l'invio della notifica quando viene raggiunto il limite.</span><span class="sxs-lookup"><span data-stu-id="0d412-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="0d412-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0d412-122">-Name</span></span>
<span data-ttu-id="0d412-123">Nome del componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="0d412-123">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d412-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d412-124">-ResourceGroupName</span></span>
<span data-ttu-id="0d412-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0d412-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d412-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d412-126">-ResourceId</span></span>
<span data-ttu-id="0d412-127">ID risorsa componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="0d412-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d412-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d412-128">-Confirm</span></span>
<span data-ttu-id="0d412-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d412-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d412-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d412-130">-WhatIf</span></span>
<span data-ttu-id="0d412-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d412-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d412-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d412-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d412-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d412-133">CommonParameters</span></span>
<span data-ttu-id="0d412-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d412-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d412-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d412-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d412-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="0d412-136">INPUTS</span></span>

### <span data-ttu-id="0d412-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="0d412-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="0d412-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0d412-138">System.String</span></span>

## <span data-ttu-id="0d412-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d412-139">OUTPUTS</span></span>

### <span data-ttu-id="0d412-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="0d412-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="0d412-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="0d412-141">NOTES</span></span>

## <span data-ttu-id="0d412-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d412-142">RELATED LINKS</span></span>
