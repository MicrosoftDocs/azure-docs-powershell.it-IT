---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: d9ddfdb43db8e94d0dc65606f6c5f86f05db31d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182246"
---
# <span data-ttu-id="ca593-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="ca593-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="ca593-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca593-102">SYNOPSIS</span></span>
<span data-ttu-id="ca593-103">Impostare il piano tariffario e le informazioni sul volume giornaliero dei dati per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="ca593-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="ca593-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca593-104">SYNTAX</span></span>

### <span data-ttu-id="ca593-105">ComponentNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ca593-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca593-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca593-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca593-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca593-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca593-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ca593-108">DESCRIPTION</span></span>
<span data-ttu-id="ca593-109">Impostare il piano tariffario e le informazioni sul volume giornaliero dei dati per una risorsa di Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ca593-109">Set pricing plan and daily data volume information for an application insights resource.</span></span>
<span data-ttu-id="ca593-110">Il piano dei prezzi delle informazioni dettagliate sull'applicazione creato dopo aprile 2018 non può essere impostato da questo cmdlet: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span><span class="sxs-lookup"><span data-stu-id="ca593-110">Pricing plan of application insights created after April 2018 cannot be set by this cmdlet: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span></span>

## <span data-ttu-id="ca593-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca593-111">EXAMPLES</span></span>

### <span data-ttu-id="ca593-112">Esempio 1: impostare il piano per i prezzi e le informazioni sul volume dei dati giornalieri per una risorsa application insights</span><span class="sxs-lookup"><span data-stu-id="ca593-112">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="ca593-113">Impostare il piano prezzi su "Base", impostare il limite giornaliero del volume di dati su 400 GB al giorno e interrompere l'invio della notifica quando si preme "test" della risorsa nel gruppo di risorse "testgroup"</span><span class="sxs-lookup"><span data-stu-id="ca593-113">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="ca593-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca593-114">PARAMETERS</span></span>

### <span data-ttu-id="ca593-115">-ApplicationInsightsInsightsIn</span><span class="sxs-lookup"><span data-stu-id="ca593-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="ca593-116">Oggetto componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ca593-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="ca593-117">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="ca593-117">-DailyCapGB</span></span>
<span data-ttu-id="ca593-118">Limite giornaliero.</span><span class="sxs-lookup"><span data-stu-id="ca593-118">Daily Cap.</span></span>

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

### <span data-ttu-id="ca593-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca593-119">-DefaultProfile</span></span>
<span data-ttu-id="ca593-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca593-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca593-121">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="ca593-121">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="ca593-122">Interrompi l'invio della notifica quando viene raggiunto il limite.</span><span class="sxs-lookup"><span data-stu-id="ca593-122">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="ca593-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ca593-123">-Name</span></span>
<span data-ttu-id="ca593-124">Nome del componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ca593-124">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="ca593-125">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="ca593-125">-PricingPlan</span></span>
<span data-ttu-id="ca593-126">Nome del piano di prezzi.</span><span class="sxs-lookup"><span data-stu-id="ca593-126">Pricing plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Application Insights Enterprise, Limited Basic

Required: False
Position: Named
Default value: "Basic"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca593-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca593-127">-ResourceGroupName</span></span>
<span data-ttu-id="ca593-128">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca593-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="ca593-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca593-129">-ResourceId</span></span>
<span data-ttu-id="ca593-130">ID risorsa componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ca593-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="ca593-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca593-131">-Confirm</span></span>
<span data-ttu-id="ca593-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca593-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca593-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca593-133">-WhatIf</span></span>
<span data-ttu-id="ca593-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca593-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca593-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca593-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca593-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca593-136">CommonParameters</span></span>
<span data-ttu-id="ca593-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca593-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca593-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca593-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca593-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="ca593-139">INPUTS</span></span>

### <span data-ttu-id="ca593-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="ca593-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="ca593-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ca593-141">System.String</span></span>

## <span data-ttu-id="ca593-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca593-142">OUTPUTS</span></span>

### <span data-ttu-id="ca593-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="ca593-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="ca593-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="ca593-144">NOTES</span></span>

## <span data-ttu-id="ca593-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca593-145">RELATED LINKS</span></span>
