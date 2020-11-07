---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: 33b55c70d88daf8493012945f49794c25e62b474
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685116"
---
# <span data-ttu-id="d708c-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="d708c-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="d708c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d708c-102">SYNOPSIS</span></span>
<span data-ttu-id="d708c-103">Impostare il piano prezzi e le informazioni sul volume dei dati giornalieri per una risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="d708c-103">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="d708c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d708c-104">SYNTAX</span></span>

### <span data-ttu-id="d708c-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d708c-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d708c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d708c-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d708c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d708c-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d708c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d708c-108">DESCRIPTION</span></span>
<span data-ttu-id="d708c-109">Impostare il piano prezzi e le informazioni sul volume dei dati giornalieri per una risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="d708c-109">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="d708c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d708c-110">EXAMPLES</span></span>

### <span data-ttu-id="d708c-111">Esempio 1 impostare il piano prezzi e le informazioni sul volume dei dati giornalieri per una risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="d708c-111">Example 1 Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="d708c-112">Impostare il piano per i prezzi su "base", impostare il CAP volumen di dati giornalieri su 400GB al giorno e interrompere l'invio della notifica quando l'hit Cap per la risorsa "test" nel gruppo di risorse "testgroup"</span><span class="sxs-lookup"><span data-stu-id="d708c-112">Set the pricing plan to "Basic", set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="d708c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d708c-113">PARAMETERS</span></span>

### <span data-ttu-id="d708c-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d708c-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="d708c-115">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="d708c-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="d708c-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="d708c-116">-DailyCapGB</span></span>
<span data-ttu-id="d708c-117">Cap giornaliero.</span><span class="sxs-lookup"><span data-stu-id="d708c-117">Daily Cap.</span></span>

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

### <span data-ttu-id="d708c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d708c-118">-DefaultProfile</span></span>
<span data-ttu-id="d708c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d708c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d708c-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="d708c-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="d708c-121">Interrompi invio notifica quando si preme il tappo.</span><span class="sxs-lookup"><span data-stu-id="d708c-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="d708c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d708c-122">-Name</span></span>
<span data-ttu-id="d708c-123">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="d708c-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="d708c-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="d708c-124">-PricingPlan</span></span>
<span data-ttu-id="d708c-125">Nome piano prezzi.</span><span class="sxs-lookup"><span data-stu-id="d708c-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="d708c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d708c-126">-ResourceGroupName</span></span>
<span data-ttu-id="d708c-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d708c-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="d708c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d708c-128">-ResourceId</span></span>
<span data-ttu-id="d708c-129">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="d708c-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="d708c-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d708c-130">-Confirm</span></span>
<span data-ttu-id="d708c-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d708c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d708c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d708c-132">-WhatIf</span></span>
<span data-ttu-id="d708c-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d708c-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d708c-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d708c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d708c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d708c-135">CommonParameters</span></span>
<span data-ttu-id="d708c-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d708c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d708c-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d708c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d708c-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d708c-138">INPUTS</span></span>

### <span data-ttu-id="d708c-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d708c-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="d708c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d708c-140">System.String</span></span>

## <span data-ttu-id="d708c-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d708c-141">OUTPUTS</span></span>

### <span data-ttu-id="d708c-142">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="d708c-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="d708c-143">Note</span><span class="sxs-lookup"><span data-stu-id="d708c-143">NOTES</span></span>

## <span data-ttu-id="d708c-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d708c-144">RELATED LINKS</span></span>
