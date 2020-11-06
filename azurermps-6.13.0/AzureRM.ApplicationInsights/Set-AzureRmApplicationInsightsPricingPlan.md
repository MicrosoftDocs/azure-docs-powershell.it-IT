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
# Set-AzureRmApplicationInsightsPricingPlan

## Sinossi
Impostare il piano prezzi e le informazioni sul volume dei dati giornalieri per una risorsa approfondimenti applicazione

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### ComponentNameParameterSet (impostazione predefinita)
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ComponentObjectParameterSet
```
Set-AzureRmApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrizione
Impostare il piano prezzi e le informazioni sul volume dei dati giornalieri per una risorsa approfondimenti applicazione

## ESEMPI

### Esempio 1 impostare il piano prezzi e le informazioni sul volume dei dati giornalieri per una risorsa approfondimenti applicazione
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

Impostare il piano per i prezzi su "base", impostare il CAP volumen di dati giornalieri su 400GB al giorno e interrompere l'invio della notifica quando l'hit Cap per la risorsa "test" nel gruppo di risorse "testgroup"

## PARAMETRI

### -ApplicationInsightsComponent
Oggetto componente approfondimenti applicazione.

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

### -DailyCapGB
Cap giornaliero.

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

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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

### -DisableNotificationWhenHitCap
Interrompi invio notifica quando si preme il tappo.

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

### -Nome
Nome del componente approfondimenti applicazione.

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

### -PricingPlan
Nome piano prezzi.

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

### -ResourceGroupName
Nome del gruppo di risorse.

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

### -ResourceId
ID risorsa componente approfondimenti applicazione.

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

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

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

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent
Parametri: ApplicationInsightsComponent (ByValue)

### System. String

## OUTPUT

### Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingPlan

## Note

## COLLEGAMENTI CORRELATI
