---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: f13408e23dcf8f1db9de2e19fc05d899b712a783
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201239"
---
# <span data-ttu-id="50f28-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="50f28-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="50f28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50f28-102">SYNOPSIS</span></span>
<span data-ttu-id="50f28-103">Impostare il limite giornaliero del volume dei dati per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="50f28-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="50f28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50f28-104">SYNTAX</span></span>

### <span data-ttu-id="50f28-105">ComponentNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50f28-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50f28-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50f28-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50f28-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="50f28-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50f28-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="50f28-108">DESCRIPTION</span></span>
<span data-ttu-id="50f28-109">Impostare il limite giornaliero del volume dei dati per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="50f28-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="50f28-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50f28-110">EXAMPLES</span></span>

### <span data-ttu-id="50f28-111">Esempio 1: impostare il limite del volume dei dati giornalieri per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="50f28-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="50f28-112">Impostare il limite giornaliero del volume dei dati su 400 GB al giorno e interrompere l'invio della notifica quando viene raggiunto il limite per la risorsa "test" nel gruppo di risorse "gruppo di test"</span><span class="sxs-lookup"><span data-stu-id="50f28-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="50f28-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50f28-113">PARAMETERS</span></span>

### <span data-ttu-id="50f28-114">-ApplicationInsightsInsightsIn</span><span class="sxs-lookup"><span data-stu-id="50f28-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="50f28-115">Oggetto componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="50f28-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="50f28-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="50f28-116">-DailyCapGB</span></span>
<span data-ttu-id="50f28-117">Limite giornaliero.</span><span class="sxs-lookup"><span data-stu-id="50f28-117">Daily Cap.</span></span>

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

### <span data-ttu-id="50f28-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f28-118">-DefaultProfile</span></span>
<span data-ttu-id="50f28-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50f28-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50f28-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="50f28-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="50f28-121">Interrompi l'invio della notifica quando viene raggiunto il limite.</span><span class="sxs-lookup"><span data-stu-id="50f28-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="50f28-122">-Name</span><span class="sxs-lookup"><span data-stu-id="50f28-122">-Name</span></span>
<span data-ttu-id="50f28-123">Nome del componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="50f28-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="50f28-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50f28-124">-ResourceGroupName</span></span>
<span data-ttu-id="50f28-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="50f28-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="50f28-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50f28-126">-ResourceId</span></span>
<span data-ttu-id="50f28-127">ID risorsa componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="50f28-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="50f28-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50f28-128">-Confirm</span></span>
<span data-ttu-id="50f28-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50f28-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50f28-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50f28-130">-WhatIf</span></span>
<span data-ttu-id="50f28-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50f28-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50f28-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50f28-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50f28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f28-133">CommonParameters</span></span>
<span data-ttu-id="50f28-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50f28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f28-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50f28-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f28-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="50f28-136">INPUTS</span></span>

### <span data-ttu-id="50f28-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="50f28-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="50f28-138">System.String</span><span class="sxs-lookup"><span data-stu-id="50f28-138">System.String</span></span>

## <span data-ttu-id="50f28-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50f28-139">OUTPUTS</span></span>

### <span data-ttu-id="50f28-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="50f28-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="50f28-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="50f28-141">NOTES</span></span>

## <span data-ttu-id="50f28-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50f28-142">RELATED LINKS</span></span>
