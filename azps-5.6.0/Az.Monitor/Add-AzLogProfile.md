---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: a5d60cbda668e963793dbb350950ea0e85812892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980318"
---
# Add-AzLogProfile

## SYNOPSIS
Crea un nuovo profilo del log attività. Questo profilo viene usato per archiviare il log attività in un account di archiviazione di Azure o per trasmettere il log a un hub eventi di Azure nella stessa sottoscrizione. 

## SINTASSI

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Add-AzLogProfile** crea un profilo di log.
- **Account di archiviazione:** è supportato solo l'account di archiviazione standard (l'account di archiviazione Premium non è supportato). Può essere di tipo ARM o classico. Se è registrato a un account di archiviazione, il costo di archiviazione del log attività viene fatturato a tariffe standard di archiviazione normali. Per ogni abbonamento può essere usato un solo profilo di log per ogni abbonamento, consequenzialemente, per esportare il log attività. 
- **Hub eventi:** per esportare il log attività può essere usato un solo profilo di log per ogni abbonamento. Se il log attività viene trasmesso a un hub eventi, verrà applicato il prezzo standard dell'hub eventi. Nel log attività gli eventi possono riguardare un'area geografica o "globale". Globalmente, significa essenzialmente che questi eventi sono agnostici nella regione e sono indipendenti dall'area geografica, di fatto la maggior parte degli eventi rientrano in questa categoria. Se il profilo del log attività viene impostato dal portale, viene aggiunto in modo implicito "Globale" insieme a qualsiasi altra area geografica selezionata nell'interfaccia utente. Quando si usa il cmdlet, la posizione "Globale" deve essere esplicitamente menzionata oltre a qualsiasi altra area geografica. 
**Nota:-** **Se non si imposta "Globale" nelle** posizioni, la maggior parte del log attività non viene esportata. Questo cmdlet implementa il criterio ShouldProcess, ad esempio potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere effettivamente la risorsa.

## ESEMPI

### Esempio 1: Aggiungere un nuovo profilo di log per esportare il log attività che corrisponde alla condizione della posizione a un account di archiviazione
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### Esempio 2

Crea un nuovo profilo del log attività. (autogenerati)

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## PARAMETERS

### -Category
Specifica l'elenco delle categorie.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -Location
Specifica la posizione del profilo di log.
Valori validi: eseguire il cmdlet seguente per ottenere l'elenco più recente di posizioni. Get-AzLocation | Selezionare DisplayName

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifica il nome del profilo.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
Specifica i criteri di conservazione, in giorni. Numero di giorni per cui i log vengono conservati nell'account di archiviazione specificato. Per conservare i dati per sempre, impostare questo valore su **0.** Se non è specificato, viene utilizzato il valore predefinito **0.** Per la conservazione dei dati verranno applicate tariffe normali per l'archiviazione standard o la fatturazione dell'hub eventi.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceBusRuleId
Specifica l'ID della regola del bus di servizio.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountId
Specifica l'ID dell'account di archiviazione. ID è l'ID risorsa completo dell'account di archiviazione, ad esempio  
/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Mostra cosa accadrebbe se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

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

### System.String

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## OUTPUT

### Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzLogProfile](./Get-AzLogProfile.md)

[Remove-AzLogProfile](./Remove-AzLogProfile.md)


