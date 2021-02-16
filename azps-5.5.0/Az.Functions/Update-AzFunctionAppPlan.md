---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200279"
---
# Update-AzFunctionAppPlan

## SYNOPSIS
Aggiorna un piano di servizio app per le funzioni.

## SINTASSI

### ByName (Impostazione predefinita)
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIZIONE
Aggiorna un piano di servizio app per le funzioni.

## ESEMPI

### Esempio 1: Aggiornare un piano di servizio app alla SKU EP2 con venti massime lavorate.
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

Questo comando aggiorna un piano di servizio app alle SKU EP2 con venti utenti massimi.

## PARAMETERS

### -AsJob
Eseguire il comando come processo.

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

### -DefaultProfile


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaximumWorkerCount
Il numero massimo di persone per il piano di servizio app.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinimumWorkerCount
Il numero minimo di persone per il piano di servizio app.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Nome del piano di servizio dell'app.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Eseguire il comando in modo asincrono.

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

### -ResourceGroupName
Nome del gruppo di risorse a cui appartiene la risorsa.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
SKU del piano.
Gli input validi sono: EP1, EP2, EP3

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID sottoscrizione di Azure.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Tag di risorse.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

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
Mostra cosa accadrebbe se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

## OUTPUT

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

## NOTE

ALIAS

PROPRIETÀ DEI PARAMETRI COMPLESSE

Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


INPUTOBJECT <IAppServicePlan> : 
  - `Location <String>`: Posizione risorsa.
  - `[Kind <String>]`: tipo di risorsa.
  - `[Tag <IResourceTags>]`: tag di risorsa.
    - `[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.
  - `[Capacity <Int32?>]`: numero corrente di istanze assegnate alla risorsa.
  - `[FreeOfferExpirationTime <DateTime?>]`: il tempo in cui scade l'offerta gratuita della server farm.
  - `[HostingEnvironmentProfileId <String>]`: ID risorsa dell'ambiente del servizio app.
  - `[HyperV <Boolean?>]`: se il piano di servizio app contenitore Hyper-V, <code>true</code> in <code>false</code> caso contrario.
  - `[IsSpot <Boolean?>]`: se <code>true</code> , questo piano di servizio dell'app è proprietario di istanze spot.
  - `[IsXenon <Boolean?>]`: Obsoleta: se il piano di servizio app contenitore Hyper-V, <code>true</code> in <code>false</code> caso contrario.
  - `[MaximumElasticWorkerCount <Int32?>]`: numero massimo di persone totali consentite per questo piano di servizio app ElasticScaleEnabled
  - `[PerSiteScaling <Boolean?>]`: se <code>true</code> , le app assegnate a questo piano di servizio app possono essere ridimensionate in modo indipendente.         Se <code>false</code> , le app assegnate a questo piano di servizio app verranno ridimensionate in base a tutte le istanze del piano.
  - `[Reserved <Boolean?>]`: se il piano di servizio dell'app <code>true</code> Linux, in <code>false</code> caso contrario.
  - `[SkuCapability <ICapability[]>]`: le funzionalità dello SKU, ad esempio, sono abilitate da Gestione traffico?
    - `[Name <String>]`: nome della funzionalità SKU.
    - `[Reason <String>]`: motivo della funzionalità SKU.
    - `[Value <String>]`: valore della funzionalità SKU.
  - `[SkuCapacityDefault <Int32?>]`: numero predefinito di dipendenti per questo SKU del piano di servizio app.
  - `[SkuCapacityMaximum <Int32?>]`: numero massimo di persone per questo SKU del piano di servizio app.
  - `[SkuCapacityMinimum <Int32?>]`: numero minimo di dipendenti per questo SKU del piano di servizio app.
  - `[SkuCapacityScaleType <String>]`: configurazioni di scala disponibili per un piano di servizio app.
  - `[SkuFamily <String>]`: codice famiglia dello SKU della risorsa.
  - `[SkuLocation <String[]>]`: posizione dello SKU.
  - `[SkuName <String>]`: nome della SKU della risorsa.
  - `[SkuSize <String>]`: specificatore di dimensioni dello SKU della risorsa.
  - `[SkuTier <String>]`: livello di servizio della SKU della risorsa.
  - `[SpotExpirationTime <DateTime?>]`: ora di scadenza della server farm. Valido solo se si tratta di una server farm spot.
  - `[TargetWorkerCount <Int32?>]`: per ridimensionare il numero di lavoratori.
  - `[TargetWorkerSizeId <Int32?>]`: per ridimensionare l'ID delle dimensioni dei lavoratori.
  - `[WorkerTierName <String>]`: livello di utente di destinazione assegnato al piano di servizio app.

## COLLEGAMENTI CORRELATI

