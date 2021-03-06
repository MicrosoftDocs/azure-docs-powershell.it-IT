---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192900"
---
# Remove-AzFunctionAppPlan

## Sinossi
Elimina un piano dell'app funzione.

## SINTASSI

### ByName (impostazione predefinita)
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Descrizione
Elimina un piano dell'app funzione.

## ESEMPI

### Esempio 1: ottenere un piano per l'app di funzioni per nome ed eliminarlo.
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

Questo comando consente di ottenere un piano per l'app di funzioni per nome ed eliminarlo.

### Esempio 2: eliminare un piano dell'app funzione per nome.
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Questo comando Elimina un piano per nome dell'app funzione.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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

### -Force
Impone al cmdlet di rimuovere il piano dell'app funzione senza richiedere conferma.

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

### -InputObject
Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.

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

### -Nome
Nome dell'app funzione.

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

### -PassThru
Restituisce vero quando il comando riesce.

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

### -SubscriptionId
ID abbonamento di Azure.

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
Mostra cosa succede se il cmdlet viene eseguito.
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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. IAppServicePlan

## OUTPUT

### System. Boolean

## Note

ALIAS

PROPRIETÀ COMPLESSE DI PARAMETRI

Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


INPUTOBJECT <IAppServicePlan> : 
  - `Location <String>`: Percorso delle risorse.
  - `[Kind <String>]`: Tipo di risorsa.
  - `[Tag <IResourceTags>]`: Tag delle risorse.
    - `[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.
  - `[Capacity <Int32?>]`: Numero corrente di istanze assegnate alla risorsa.
  - `[FreeOfferExpirationTime <DateTime?>]`: Il momento in cui l'offerta gratuita della server farm scade.
  - `[HostingEnvironmentProfileId <String>]`: ID risorsa dell'ambiente di servizio app.
  - `[HyperV <Boolean?>]`: Se il piano di servizio app contenitore Hyper-V <code>true</code> , <code>false</code> in caso contrario.
  - `[IsSpot <Boolean?>]`: Se <code>true</code> , questo piano di servizio app possiede istanze di spot.
  - `[IsXenon <Boolean?>]`: Obsolete: se piano di servizio app contenitore Hyper-V <code>true</code> , <code>false</code> in caso contrario.
  - `[MaximumElasticWorkerCount <Int32?>]`: Numero massimo di lavoratori totali consentiti per il piano di servizio app ElasticScaleEnabled
  - `[PerSiteScaling <Boolean?>]`: Se le <code>true</code> app assegnate a questo piano di servizio app possono essere ridimensionate in modo indipendente.         Se <code>false</code> , le app assegnate al piano del servizio app verranno ridimensionate in tutte le istanze del piano.
  - `[Reserved <Boolean?>]`: Se piano di servizio app Linux <code>true</code> , <code>false</code> in caso contrario.
  - `[SkuCapability <ICapability[]>]`: Le funzionalità dell'USK, ad esempio, sono abilitate per Traffic Manager?
    - `[Name <String>]`: Nome della funzionalità SKU.
    - `[Reason <String>]`: Motivo della funzionalità SKU.
    - `[Value <String>]`: Valore della funzionalità SKU.
  - `[SkuCapacityDefault <Int32?>]`: Numero predefinito di Worker per questo piano di servizio App SKU.
  - `[SkuCapacityMaximum <Int32?>]`: Numero massimo di dipendenti per questo piano di servizio App SKU.
  - `[SkuCapacityMinimum <Int32?>]`: Numero minimo di dipendenti per questo piano di servizio App SKU.
  - `[SkuCapacityScaleType <String>]`: Configurazioni di scala disponibili per un piano di servizio app.
  - `[SkuFamily <String>]`: Codice famiglia della SKU di risorse.
  - `[SkuLocation <String[]>]`: Posizioni dell'USK.
  - `[SkuName <String>]`: Nome della SKU di risorse.
  - `[SkuSize <String>]`: Specificatore di dimensioni della SKU di risorse.
  - `[SkuTier <String>]`: Livello di servizio della SKU di risorse.
  - `[SpotExpirationTime <DateTime?>]`: L'ora in cui scade la server farm. Valido solo se si tratta di una farm di server di punti.
  - `[TargetWorkerCount <Int32?>]`: Ridimensionamento del conteggio lavoratori.
  - `[TargetWorkerSizeId <Int32?>]`: Ridimensionamento ID dimensione lavoratore.
  - `[WorkerTierName <String>]`: Livello di lavoro di destinazione assegnato al piano di servizio app.

## COLLEGAMENTI CORRELATI

