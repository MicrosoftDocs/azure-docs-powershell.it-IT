---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 0ef53015b3e07eeb69cdcfd0ab70c67317ab92cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521440"
---
# Add-AzureRmLogProfile

## Sinossi
Crea un nuovo profilo del log attività. Questo profilo viene usato per archiviare il log delle attività in un account di archiviazione di Azure o in un flusso di lavoro in un hub di eventi di Azure nello stesso abbonamento. 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Add-AzureRmLogProfile** crea un profilo di log.

- Solo **account di archiviazione standard (account di** archiviazione Premium non supportato) è supportato. Potrebbe essere di tipo ARM o Classic. Se è stato eseguito l'accesso a un account di archiviazione, il costo di archiviazione del log attività viene addebitato alle normali tariffe di archiviazione standard. Per esportare il log delle attività può essere usato un solo profilo di log per abbonamento in modo consequenziale solo un account di archiviazione per abbonamento. 

- **Hub eventi** : per esportare il log delle attività può essere usato solo un profilo di log per ogni sottoscrizione in modo consequenziale solo un hub eventi per ogni abbonamento. Se il log attività viene trasmesso a un hub eventi, verrà applicato il prezzo standard dell'hub eventi. 

Nel registro attività gli eventi possono essere relativi a un'area geografica o "globale". Global significa essenzialmente che questi eventi sono agnostici della regione e sono indipendenti dall'area geografica, infatti la maggior parte degli eventi rientra in questa categoria. Se il profilo del log attività è impostato dal portale, aggiunge implicitamente "globale" insieme a qualsiasi altra area selezionata nell'interfaccia utente. Quando si usa il cmdlet, la posizione "globale" deve essere menzionata in modo esplicito, oltre a qualsiasi altra area geografica. 

**Nota** : se **non si imposta "globale" nelle posizioni, la maggior parte del log delle attività non viene esportata.** 

Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.

## ESEMPI

### Esempio 1: aggiungere un nuovo profilo di log per esportare il log attività che corrisponde alla condizione di posizione a un account di archiviazione
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## PARAMETRI

### -Categoria
Specifica l'elenco di categorie.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: Categories

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -Posizione
Specifica la posizione del profilo del log.
Valori validi: Esegui sotto cmdlet per ottenere l'elenco più recente di posizioni. 

Get-AzureLocation | Selezionare DisplayName

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: Locations

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Specifica il nome del profilo.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
Specifica i criteri di conservazione, in giorni. Questo è il numero di giorni in cui i registri vengono conservati nell'account di archiviazione specificato. Per mantenere i dati impostati per sempre su **0**. Se non viene specificato, il valore predefinito è **0**. L'archiviazione standard normale o le tariffe di fatturazione dell'hub eventi verranno applicate per la conservazione dei dati.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceBusRuleId
Specifica l'ID della regola Service Bus.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountId
Specifica l'ID dell'account di archiviazione. ID è l'ID di risorsa completo dell'account di archiviazione, ad esempio  

/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfile

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmLogProfile](./Get-AzureRmLogProfile.md)

[Remove-AzureRmLogProfile](./Remove-AzureRmLogProfile.md)


