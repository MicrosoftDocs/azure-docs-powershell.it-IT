---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
ms.openlocfilehash: 03c1a556f6b3fc207fbbb612f31d172705e4f42b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512007"
---
# <span data-ttu-id="e61e9-101">Set-AzureRmApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="e61e9-101">Set-AzureRmApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="e61e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e61e9-102">SYNOPSIS</span></span>
<span data-ttu-id="e61e9-103">Impostare il piano prezzi e le informazioni sul volume dei dati giornalieri per una risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="e61e9-103">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e61e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e61e9-104">SYNTAX</span></span>

### <span data-ttu-id="e61e9-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e61e9-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e61e9-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e61e9-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e61e9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e61e9-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e61e9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e61e9-108">DESCRIPTION</span></span>
<span data-ttu-id="e61e9-109">Impostare il piano prezzi e le informazioni sul volume dei dati giornalieri per una risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="e61e9-109">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="e61e9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e61e9-110">EXAMPLES</span></span>

### <span data-ttu-id="e61e9-111">Esempio 1 impostare il piano prezzi e le informazioni sul volume dei dati giornalieri per una risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="e61e9-111">Example 1 Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="e61e9-112">Impostare il piano per i prezzi su "base", impostare il CAP volumen di dati giornalieri su 400GB al giorno e interrompere l'invio della notifica quando l'hit Cap per la risorsa "test" nel gruppo di risorse "testgroup"</span><span class="sxs-lookup"><span data-stu-id="e61e9-112">Set the pricing plan to "Basic", set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="e61e9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e61e9-113">PARAMETERS</span></span>

### <span data-ttu-id="e61e9-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e61e9-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="e61e9-115">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="e61e9-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="e61e9-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="e61e9-116">-DailyCapGB</span></span>
<span data-ttu-id="e61e9-117">Cap giornaliero.</span><span class="sxs-lookup"><span data-stu-id="e61e9-117">Daily Cap.</span></span>

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

### <span data-ttu-id="e61e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e61e9-118">-DefaultProfile</span></span>
<span data-ttu-id="e61e9-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e61e9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e61e9-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="e61e9-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="e61e9-121">Interrompi invio notifica quando si preme il tappo.</span><span class="sxs-lookup"><span data-stu-id="e61e9-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="e61e9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e61e9-122">-Name</span></span>
<span data-ttu-id="e61e9-123">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="e61e9-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="e61e9-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="e61e9-124">-PricingPlan</span></span>
<span data-ttu-id="e61e9-125">Nome piano prezzi.</span><span class="sxs-lookup"><span data-stu-id="e61e9-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="e61e9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e61e9-126">-ResourceGroupName</span></span>
<span data-ttu-id="e61e9-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e61e9-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="e61e9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e61e9-128">-ResourceId</span></span>
<span data-ttu-id="e61e9-129">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="e61e9-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="e61e9-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e61e9-130">-Confirm</span></span>
<span data-ttu-id="e61e9-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e61e9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e61e9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e61e9-132">-WhatIf</span></span>
<span data-ttu-id="e61e9-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e61e9-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e61e9-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e61e9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e61e9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e61e9-135">CommonParameters</span></span>
<span data-ttu-id="e61e9-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e61e9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e61e9-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e61e9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e61e9-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e61e9-138">INPUTS</span></span>

### <span data-ttu-id="e61e9-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e61e9-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="e61e9-140">Parametri: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e61e9-140">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="e61e9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e61e9-141">System.String</span></span>

## <span data-ttu-id="e61e9-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e61e9-142">OUTPUTS</span></span>

### <span data-ttu-id="e61e9-143">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="e61e9-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="e61e9-144">Note</span><span class="sxs-lookup"><span data-stu-id="e61e9-144">NOTES</span></span>

## <span data-ttu-id="e61e9-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e61e9-145">RELATED LINKS</span></span>
