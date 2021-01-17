---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: d9ddfdb43db8e94d0dc65606f6c5f86f05db31d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353419"
---
# <span data-ttu-id="64141-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="64141-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="64141-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64141-102">SYNOPSIS</span></span>
<span data-ttu-id="64141-103">Impostare il piano prezzi e le informazioni sul volume dei dati giornalieri per una risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="64141-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="64141-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64141-104">SYNTAX</span></span>

### <span data-ttu-id="64141-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="64141-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64141-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64141-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64141-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64141-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64141-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64141-108">DESCRIPTION</span></span>
<span data-ttu-id="64141-109">Impostare il piano prezzi e le informazioni sul volume dei dati giornalieri per una risorsa approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="64141-109">Set pricing plan and daily data volume information for an application insights resource.</span></span>
<span data-ttu-id="64141-110">Questo cmdlet non può essere impostato con il piano dei prezzi degli approfondimenti delle applicazioni creati dopo il 2018 di aprile: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span><span class="sxs-lookup"><span data-stu-id="64141-110">Pricing plan of application insights created after April 2018 cannot be set by this cmdlet: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span></span>

## <span data-ttu-id="64141-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64141-111">EXAMPLES</span></span>

### <span data-ttu-id="64141-112">Esempio 1 impostare il piano prezzi e le informazioni sul volume dei dati giornalieri per una risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="64141-112">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="64141-113">Impostare il piano per i prezzi su "base", impostare il CAP del volume di dati giornalieri su 400GB per giorno e interrompere l'invio della notifica quando si preme il pulsante per la risorsa "test" nel gruppo di risorse "testgroup"</span><span class="sxs-lookup"><span data-stu-id="64141-113">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="64141-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64141-114">PARAMETERS</span></span>

### <span data-ttu-id="64141-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="64141-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="64141-116">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="64141-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="64141-117">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="64141-117">-DailyCapGB</span></span>
<span data-ttu-id="64141-118">Cap giornaliero.</span><span class="sxs-lookup"><span data-stu-id="64141-118">Daily Cap.</span></span>

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

### <span data-ttu-id="64141-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64141-119">-DefaultProfile</span></span>
<span data-ttu-id="64141-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64141-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64141-121">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="64141-121">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="64141-122">Interrompi invio notifica quando si preme il tappo.</span><span class="sxs-lookup"><span data-stu-id="64141-122">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="64141-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="64141-123">-Name</span></span>
<span data-ttu-id="64141-124">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="64141-124">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="64141-125">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="64141-125">-PricingPlan</span></span>
<span data-ttu-id="64141-126">Nome piano prezzi.</span><span class="sxs-lookup"><span data-stu-id="64141-126">Pricing plan name.</span></span>

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

### <span data-ttu-id="64141-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64141-127">-ResourceGroupName</span></span>
<span data-ttu-id="64141-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="64141-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="64141-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64141-129">-ResourceId</span></span>
<span data-ttu-id="64141-130">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="64141-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="64141-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="64141-131">-Confirm</span></span>
<span data-ttu-id="64141-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64141-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64141-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64141-133">-WhatIf</span></span>
<span data-ttu-id="64141-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64141-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64141-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64141-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64141-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64141-136">CommonParameters</span></span>
<span data-ttu-id="64141-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64141-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64141-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64141-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64141-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64141-139">INPUTS</span></span>

### <span data-ttu-id="64141-140">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="64141-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="64141-141">System. String</span><span class="sxs-lookup"><span data-stu-id="64141-141">System.String</span></span>

## <span data-ttu-id="64141-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64141-142">OUTPUTS</span></span>

### <span data-ttu-id="64141-143">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="64141-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="64141-144">Note</span><span class="sxs-lookup"><span data-stu-id="64141-144">NOTES</span></span>

## <span data-ttu-id="64141-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64141-145">RELATED LINKS</span></span>
