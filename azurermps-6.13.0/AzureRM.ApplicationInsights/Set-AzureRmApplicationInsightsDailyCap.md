---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
ms.openlocfilehash: 7b47576c0fd506831d8e48201d39bd66fec72032
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512011"
---
# <span data-ttu-id="24201-101">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="24201-101">Set-AzureRmApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="24201-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24201-102">SYNOPSIS</span></span>
<span data-ttu-id="24201-103">Impostare il CAP del volume dei dati giornalieri per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="24201-103">Set daily data volume cap for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24201-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24201-104">SYNTAX</span></span>

### <span data-ttu-id="24201-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="24201-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24201-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24201-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24201-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24201-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24201-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24201-108">DESCRIPTION</span></span>
<span data-ttu-id="24201-109">Impostare il CAP del volume dei dati giornalieri per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="24201-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="24201-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24201-110">EXAMPLES</span></span>

### <span data-ttu-id="24201-111">Esempio 1 impostare il CAP del volume dei dati giornalieri per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="24201-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="24201-112">Impostare il CAP volumen di dati giornalieri su 400GB al giorno e interrompere l'invio della notifica quando si preme il pulsante per la risorsa "test" nel gruppo di risorse "testgroup"</span><span class="sxs-lookup"><span data-stu-id="24201-112">Set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="24201-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24201-113">PARAMETERS</span></span>

### <span data-ttu-id="24201-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="24201-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="24201-115">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="24201-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="24201-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="24201-116">-DailyCapGB</span></span>
<span data-ttu-id="24201-117">Cap giornaliero.</span><span class="sxs-lookup"><span data-stu-id="24201-117">Daily Cap.</span></span>

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

### <span data-ttu-id="24201-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24201-118">-DefaultProfile</span></span>
<span data-ttu-id="24201-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24201-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24201-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="24201-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="24201-121">Interrompi invio notifica quando si preme il tappo.</span><span class="sxs-lookup"><span data-stu-id="24201-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="24201-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="24201-122">-Name</span></span>
<span data-ttu-id="24201-123">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="24201-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="24201-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24201-124">-ResourceGroupName</span></span>
<span data-ttu-id="24201-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="24201-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="24201-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24201-126">-ResourceId</span></span>
<span data-ttu-id="24201-127">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="24201-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="24201-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="24201-128">-Confirm</span></span>
<span data-ttu-id="24201-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24201-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24201-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24201-130">-WhatIf</span></span>
<span data-ttu-id="24201-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24201-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24201-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24201-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24201-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24201-133">CommonParameters</span></span>
<span data-ttu-id="24201-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24201-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24201-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24201-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24201-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24201-136">INPUTS</span></span>

### <span data-ttu-id="24201-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="24201-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="24201-138">Parametri: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="24201-138">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="24201-139">System. String</span><span class="sxs-lookup"><span data-stu-id="24201-139">System.String</span></span>

## <span data-ttu-id="24201-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24201-140">OUTPUTS</span></span>

### <span data-ttu-id="24201-141">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="24201-141">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="24201-142">Note</span><span class="sxs-lookup"><span data-stu-id="24201-142">NOTES</span></span>

## <span data-ttu-id="24201-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24201-143">RELATED LINKS</span></span>
