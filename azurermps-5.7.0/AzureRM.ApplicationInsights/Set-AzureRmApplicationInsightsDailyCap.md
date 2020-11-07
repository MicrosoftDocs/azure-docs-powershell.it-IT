---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
ms.openlocfilehash: 12e8e4f76f623391e6046f4f8b0bd424e7b9334d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685853"
---
# <span data-ttu-id="9bfab-101">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="9bfab-101">Set-AzureRmApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="9bfab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9bfab-102">SYNOPSIS</span></span>
<span data-ttu-id="9bfab-103">Impostare il CAP del volume dei dati giornalieri per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="9bfab-103">Set daily data volume cap for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bfab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9bfab-104">SYNTAX</span></span>

### <span data-ttu-id="9bfab-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9bfab-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9bfab-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bfab-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bfab-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bfab-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bfab-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bfab-108">DESCRIPTION</span></span>
<span data-ttu-id="9bfab-109">Impostare il CAP del volume dei dati giornalieri per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="9bfab-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="9bfab-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9bfab-110">EXAMPLES</span></span>

### <span data-ttu-id="9bfab-111">Esempio 1 impostare il CAP del volume dei dati giornalieri per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="9bfab-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="9bfab-112">Impostare il CAP volumen di dati giornalieri su 400GB al giorno e interrompere l'invio della notifica quando si preme il pulsante per la risorsa "test" nel gruppo di risorse "testgroup"</span><span class="sxs-lookup"><span data-stu-id="9bfab-112">Set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="9bfab-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9bfab-113">PARAMETERS</span></span>

### <span data-ttu-id="9bfab-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9bfab-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="9bfab-115">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="9bfab-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bfab-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9bfab-116">-Confirm</span></span>
<span data-ttu-id="9bfab-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bfab-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bfab-118">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="9bfab-118">-DailyCapGB</span></span>
<span data-ttu-id="9bfab-119">Cap giornaliero.</span><span class="sxs-lookup"><span data-stu-id="9bfab-119">Daily Cap.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bfab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bfab-120">-DefaultProfile</span></span>
<span data-ttu-id="9bfab-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9bfab-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bfab-122">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="9bfab-122">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="9bfab-123">Interrompi invio notifica quando si preme il tappo.</span><span class="sxs-lookup"><span data-stu-id="9bfab-123">Stop send notification when hit cap.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bfab-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9bfab-124">-Name</span></span>
<span data-ttu-id="9bfab-125">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="9bfab-125">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bfab-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bfab-126">-ResourceGroupName</span></span>
<span data-ttu-id="9bfab-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9bfab-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bfab-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bfab-128">-ResourceId</span></span>
<span data-ttu-id="9bfab-129">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="9bfab-129">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bfab-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bfab-130">-WhatIf</span></span>
<span data-ttu-id="9bfab-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bfab-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9bfab-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bfab-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bfab-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bfab-133">CommonParameters</span></span>
<span data-ttu-id="9bfab-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bfab-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bfab-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bfab-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bfab-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9bfab-136">INPUTS</span></span>

### <span data-ttu-id="9bfab-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9bfab-137">System.String</span></span>
<span data-ttu-id="9bfab-138">System. Double System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9bfab-138">System.Double System.Boolean</span></span>

## <span data-ttu-id="9bfab-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9bfab-139">OUTPUTS</span></span>

### <span data-ttu-id="9bfab-140">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingTier</span><span class="sxs-lookup"><span data-stu-id="9bfab-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingTier</span></span>

## <span data-ttu-id="9bfab-141">Note</span><span class="sxs-lookup"><span data-stu-id="9bfab-141">NOTES</span></span>

## <span data-ttu-id="9bfab-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9bfab-142">RELATED LINKS</span></span>

