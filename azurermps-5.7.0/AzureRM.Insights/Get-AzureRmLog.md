---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLog.md
ms.openlocfilehash: bdafc4ba051383a270c361f3a88453022504fe9a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508139"
---
# Get-AzureRmLog

## Sinossi
Ottiene un log di eventi.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### GetByCorrelationId
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceId
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceProvider
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySubscription
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmLog** ottiene un log di eventi.
Gli eventi possono essere associati all'ID corrente dell'abbonamento, all'ID di correlazione, al gruppo di risorse, all'ID risorsa o al provider di risorse.

## ESEMPI

### Esempio 1: ottenere un log eventi in base all'ID abbonamento
```
PS C:\>Get-AzureRmLog
```

Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID abbonamento dell'utente che ha avuto luogo 7 giorni dalla data/ora corrente.

### Esempio 2: ottenere un log eventi in base all'ID abbonamento con un numero massimo di eventi
```
PS C:\>Get-AzureRmLog -MaxEvents 100
```

Questo comando elenca la maggior parte degli eventi di 100 associati all'ID abbonamento dell'utente che ha avuto luogo 7 giorni dalla data/ora corrente.

### Esempio 3: ottenere un log eventi in base all'ID abbonamento con l'ora di inizio.
```
PS C:\>Get-AzureRmLog -StartTime 2017-06-01T10:30
```

Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID abbonamento dell'utente che ha avuto luogo dopo il 2017-06-01T10:30 ora locale, se tale data/ora non è superiore a 90 giorni dalla data/ora corrente.

### Esempio 4: ottenere un log eventi in base all'ID abbonamento con l'ora di inizio e l'ora di fine.
```
PS C:\>Get-AzureRmLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

Questo comando elenca al massimo 1000 degli eventi associati all'ID abbonamento dell'utente che ha avuto luogo dopo il 2017-04-01T10:30 local time e before 2017-04-14T11:30 local time se l'intero intervallo di data/ora non supera i 90 giorni dalla data/ora corrente, ossia: il periodo di conservazione.

### Esempio 5: ottenere un log eventi tramite un ID di correlazione
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID di correlazione specificato che ha avuto luogo 7 giorni dalla data/ora corrente. 
**Nota** : si tratta in genere di un solo evento.

### Esempio 6: ottenere un log eventi tramite un ID di correlazione con un numero massimo di eventi
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxEvents 100
```

Questo comando elenca la maggior parte degli eventi di 100 associati all'ID di correlazione specificato che ha avuto luogo 7 giorni dalla data/ora corrente. 
**Nota** : si tratta in genere di un solo evento.

### Esempio 7: ottenere un log eventi dall'ID di correlazione e dall'ora di inizio
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID di correlazione specificato che ha avuto luogo dopo il 2017-05-22T04:30:00 ora locale, se l'ora di inizio non è superiore a 90 giorni dalla data/ora corrente.
**Nota** : si tratta in genere di un solo evento.

### Esempio 8: ottenere un log eventi in base all'ID di correlazione con ora di inizio e ora di fine
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID di correlazione specificato che ha avuto luogo dopo il 2017-04-15T04:30 local time, ma prima del 2017-04-25T12:30 local time se l'intero intervallo di data/ora non è più vecchio di 90 giorni dalla data/ora corrente, ovvero il periodo di conservazione.

### Esempio 9: ottenere un log eventi per un gruppo di risorse
```
PS C:\>Get-AzureRmLog -ResourceGroupName "Contoso-Web-CentralUS"
```

Questo comando elenca al massimo 1000 gli eventi associati al gruppo di risorse specificato che ha avuto luogo 7 giorni dalla data/ora corrente.

### Esempio 10: ottenere un log eventi per un gruppo di risorse con un numero massimo di eventi
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -MaxEvents 100
```

Questo comando elenca la maggior parte degli eventi di 100 associati al gruppo di risorse specificato che ha avuto luogo 7 giorni dalla data/ora corrente.

### Esempio 11: ottenere un log eventi per un gruppo di risorse per ora di inizio
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

Questo comando elenca al massimo 1000 Evetns associato al gruppo di risorse specificato che ha avuto luogo dopo il 2017-05-22T04:30:00 ora locale se l'ora di inizio non è superiore a 90 giorni dalla data/ora corrente.

### Esempio 12: ottenere un log eventi per un gruppo di risorse con ora di inizio e ora di fine
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Questo comando elenca la maggior parte degli eventi di 1000 associati al gruppo di risorse specificato che ha avuto luogo dopo il 2017-04-15T04:30 local time, ma prima del 2017-04-25T12:30 local time se l'intero intervallo di data/ora non è superiore a 90 giorni dalla data/ora corrente, ovvero il periodo di conservazione.

### Esempio 13: ottenere un log eventi in base all'ID risorsa
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID risorsa specificato che ha avuto luogo 7 giorni dalla data/ora corrente.

### Esempio 14: ottenere un log eventi in base all'ID risorsa con un numero massimo di eventi
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxEvents 100
```

Questo comando elenca la maggior parte degli eventi di 100 associati all'ID risorsa specificato che ha avuto luogo 7 giorni dalla data/ora corrente.

### Esempio 15: ottenere un log eventi in base all'ID risorsa con un'ora di inizio
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID risorsa specificato che ha avuto luogo dopo il 2017-05-22T04:30:00 ora locale, se l'ora di inizio non è superiore a 90 giorni dalla data/ora corrente.

### Esempio 16: ottenere un log eventi in base all'ID risorsa con l'ora di inizio e di fine
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID risorsa specificato che ha avuto luogo dopo il 2017-04-15T04:30 local time, ma prima del 2017-04-25T12:30 local time se l'intero intervallo di data/ora non è maggiore di 90 giorni dalla data/ora corrente, ovvero il periodo di conservazione.

### Esempio 17: ottenere un log eventi in base al provider di risorse
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web"
```

Questo comando elenca la maggior parte degli eventi di 1000 associati al provider di risorse specificato che ha avuto luogo 7 giorni dalla data/ora corrente.

### Esempio 18: ottenere un log eventi in base al provider di risorse con un numero massimo di eventi
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -MaxEvents 100
```

Questo comando elenca la maggior parte degli eventi di 100 associati al provider di risorse specificato che ha avuto luogo 7 giorni dalla data/ora corrente.

### Esempio 19: ottenere un log eventi in base al provider di risorse con un orario di inizio
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

Questo comando elenca la maggior parte degli eventi di 1000 associati al provider di risorse specificato che ha avuto luogo dopo il 2017-05-22T04:30:00 ora locale, se l'ora di inizio non è superiore a 90 giorni dalla data/ora corrente.

### Esempio 20: ottenere un log eventi in base al provider di risorse con l'ora di inizio e di fine
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Questo comando elenca la maggior parte degli eventi di 1000 associati al provider di risorse specificato che ha avuto luogo dopo il 2017-04-15T04:30 local time, ma prima del 2017-04-25T12:30 local time se l'intero intervallo di data/ora non è maggiore di 90 giorni dalla data/ora corrente, ovvero il periodo di conservazione.

## PARAMETRI

### -Chiamante
Specifica un chiamante.

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

### -CorrelationId
Specifica l'ID di correlazione.
Questo parametro è obbligatorio.

```yaml
Type: String
Parameter Sets: GetByCorrelationId
Aliases: 

Required: True
Position: 0
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

### -DetailedOutput
Indica che questo cmdlet Visualizza l'output dettagliato.
Per impostazione predefinita, l'output viene riepilogato.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndTime
Specifica l'ora di fine della query in ora locale.
Il valore predefinito è l'ora corrente.
Il valore deve essere successivo a *StartTime*.

Puoi usare il cmdlet Get-Date per ottenere un oggetto **DateTime** .

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxRecord
Specifica il numero totale di record da recuperare per il filtro specificato.
Il valore predefinito è 1000 e il valore massimo accettato è 100000. I valori negativi e 0 vengono ignorati e viene usato il valore predefinito.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaxRecords, MaxEvents

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse.

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Specifica l'ID risorsa.

```yaml
Type: String
Parameter Sets: GetByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceProvider
Specifica un filtro in base al provider di risorse.

```yaml
Type: String
Parameter Sets: GetByResourceProvider
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartTime
Specifica l'ora di inizio della query in ora locale.
Il valore predefinito è *EndTime* meno sette giorni.

Puoi usare il cmdlet Get-Date per ottenere un oggetto **DateTime** .

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Stato
Specifica lo stato.

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

### Elenco<Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData>

### Nessuno

## Note

## COLLEGAMENTI CORRELATI

