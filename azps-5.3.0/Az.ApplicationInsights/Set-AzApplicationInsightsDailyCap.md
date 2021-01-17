---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: f13408e23dcf8f1db9de2e19fc05d899b712a783
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381233"
---
# <span data-ttu-id="6c4c0-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="6c4c0-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="6c4c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c4c0-102">SYNOPSIS</span></span>
<span data-ttu-id="6c4c0-103">Impostare il CAP del volume dei dati giornalieri per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="6c4c0-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="6c4c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c4c0-104">SYNTAX</span></span>

### <span data-ttu-id="6c4c0-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6c4c0-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c4c0-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c4c0-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c4c0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c4c0-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c4c0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c4c0-108">DESCRIPTION</span></span>
<span data-ttu-id="6c4c0-109">Impostare il CAP del volume dei dati giornalieri per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="6c4c0-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="6c4c0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c4c0-110">EXAMPLES</span></span>

### <span data-ttu-id="6c4c0-111">Esempio 1 impostare il CAP del volume dei dati giornalieri per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="6c4c0-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="6c4c0-112">Impostare il CAP del volume di dati giornalieri su 400GB per giorno e interrompere l'invio della notifica quando si preme il pulsante per la risorsa "test" nel gruppo di risorse "testgroup"</span><span class="sxs-lookup"><span data-stu-id="6c4c0-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="6c4c0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c4c0-113">PARAMETERS</span></span>

### <span data-ttu-id="6c4c0-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6c4c0-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="6c4c0-115">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c4c0-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="6c4c0-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="6c4c0-116">-DailyCapGB</span></span>
<span data-ttu-id="6c4c0-117">Cap giornaliero.</span><span class="sxs-lookup"><span data-stu-id="6c4c0-117">Daily Cap.</span></span>

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

### <span data-ttu-id="6c4c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c4c0-118">-DefaultProfile</span></span>
<span data-ttu-id="6c4c0-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c4c0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c4c0-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="6c4c0-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="6c4c0-121">Interrompi invio notifica quando si preme il tappo.</span><span class="sxs-lookup"><span data-stu-id="6c4c0-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="6c4c0-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c4c0-122">-Name</span></span>
<span data-ttu-id="6c4c0-123">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c4c0-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="6c4c0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c4c0-124">-ResourceGroupName</span></span>
<span data-ttu-id="6c4c0-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6c4c0-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="6c4c0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c4c0-126">-ResourceId</span></span>
<span data-ttu-id="6c4c0-127">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c4c0-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="6c4c0-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6c4c0-128">-Confirm</span></span>
<span data-ttu-id="6c4c0-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c4c0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c4c0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c4c0-130">-WhatIf</span></span>
<span data-ttu-id="6c4c0-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c4c0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c4c0-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c4c0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c4c0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c4c0-133">CommonParameters</span></span>
<span data-ttu-id="6c4c0-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c4c0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c4c0-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c4c0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c4c0-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c4c0-136">INPUTS</span></span>

### <span data-ttu-id="6c4c0-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6c4c0-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="6c4c0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6c4c0-138">System.String</span></span>

## <span data-ttu-id="6c4c0-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c4c0-139">OUTPUTS</span></span>

### <span data-ttu-id="6c4c0-140">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="6c4c0-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="6c4c0-141">Note</span><span class="sxs-lookup"><span data-stu-id="6c4c0-141">NOTES</span></span>

## <span data-ttu-id="6c4c0-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c4c0-142">RELATED LINKS</span></span>
