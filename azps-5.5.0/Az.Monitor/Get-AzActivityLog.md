---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187398"
---
# Get-AzActivityLog

## SYNOPSIS
Recuperare gli eventi del log attività.

## SINTASSI

### GetByCorrelationId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceProvider
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySubscription
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il Get-AzActivityLog cmdlet recupera gli eventi del log attività. Gli eventi possono essere associati all'ID della sottoscrizione corrente, all'ID di correlazione, al gruppo di risorse, all'ID risorsa o al provider di risorse corrente.

## ESEMPI

### Esempio 1: Ottenere un log eventi in base all'ID sottoscrizione
```
PS C:\>Get-ActivityAzLog
```

Questo comando elenca al massimo 1000 eventi associati all'ID sottoscrizione dell'utente, che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.

### Esempio 2: Ottenere un log eventi in base all'ID sottoscrizione con un numero massimo di eventi
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

Questo comando elenca al massimo 100 eventi associati all'ID sottoscrizione dell'utente, che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.

### Esempio 3: Ottenere un log eventi in base all'ID abbonamento con un'ora di inizio.
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

Questo comando elenca al massimo 1000 eventi associati all'ID sottoscrizione dell'utente che hanno avuto luogo il 06-06-01T10:30 ora locale se tale data/ora non è a partire da 90 giorni dalla data/ora corrente.

### Esempio 4: Ottenere un log eventi in base all'ID abbonamento con un'ora di inizio e un'ora di fine.
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

Questo comando elenca al massimo 1000 degli eventi associati all'ID abbonamento dell'utente che hanno avuto luogo il 04-04-04-01T10:30 ora locale e prima dell'ora locale 2017-04-14T11:30 se l'intero intervallo di data/ora non è a partire da 90 giorni dalla data/ora corrente, ad esempio il periodo di conservazione.

### Esempio 5: Ottenere un log eventi in base all'ID di correlazione
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

Questo comando elenca al massimo 1000 eventi associati all'ID di correlazione specificato, che hanno avuto luogo 7 giorni a partire dalla data/ora corrente. 
**NOTA:** in genere si tratta di un solo evento.

### Esempio 6: Ottenere un log eventi per ID di correlazione con un numero massimo di eventi
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

Questo comando elenca al massimo 100 eventi associati all'ID di correlazione specificato, che hanno avuto luogo 7 giorni a partire dalla data/ora corrente. 
**NOTA:** in genere si tratta di un solo evento.

### Esempio 7: Ottenere un log eventi in base all'ID di correlazione e all'ora di inizio
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

Questo comando elenca al massimo 1000 eventi associati all'ID di correlazione specificato che hanno avuto luogo il 05-05-22T04:30:00 ora locale se l'ora di inizio non è a più di 90 giorni dalla data/ora corrente.
**NOTA:** in genere si tratta di un solo evento.

### Esempio 8: Ottenere un log eventi per ID di correlazione con ora di inizio e ora di fine
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

Questo comando elenca al massimo 1000 eventi associati all'ID di correlazione specificato che hanno avuto luogo il 04-04-15T04:30 ora locale prima dell'ora locale 2017-04-25T12:30 se l'intero intervallo di data/ora non è precedente a 90 giorni dalla data/ora corrente, ad esempio il periodo di conservazione.

### Esempio 9: Ottenere un registro eventi per un gruppo di risorse
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

Questo comando elenca al massimo 1000 eventi associati al gruppo di risorse specificato che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.

### Esempio 10: Ottenere un log eventi per un gruppo di risorse con un numero massimo di eventi
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

Questo comando elenca al massimo 100 eventi associati al gruppo di risorse specificato che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.

### Esempio 11: Ottenere un registro eventi per un gruppo di risorse in base all'ora di inizio
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

Questo comando elenca al massimo 1000 eventi associati al gruppo di risorse specificato che hanno avuto luogo il 05-05-22T04:30:00 ora locale se l'ora di inizio non è precedente a 90 giorni dalla data/ora corrente.

### Esempio 12: Ottenere un log eventi per un gruppo di risorse con un'ora di inizio e un'ora di fine
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Questo comando elenca al massimo 1000 eventi associati al gruppo di risorse specificato che hanno avuto luogo il 04-04-15T04:30 ora locale 2017-04-25T12:30 se l'intero intervallo di data/ora non è precedente a 90 giorni dalla data/ora corrente, ad esempio il periodo di conservazione.

### Esempio 13: Ottenere un log eventi in base all'ID risorsa
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

Questo comando elenca al massimo 1000 eventi associati all'ID risorsa specificato, che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.

### Esempio 14: Ottenere un log eventi in base all'ID risorsa con un numero massimo di eventi
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

Questo comando elenca al massimo 100 eventi associati all'ID risorsa specificato, che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.

### Esempio 15: Ottenere un log eventi in base all'ID risorsa con un'ora di inizio
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

Questo comando elenca al massimo 1000 eventi associati all'ID risorsa specificato che hanno avuto luogo il 05-05-22T04:30:00 ora locale se l'ora di inizio non è a partire da 90 giorni dalla data/ora corrente.

### Esempio 16: Ottenere un log eventi in base all'ID risorsa con un'ora di inizio e un'ora di fine
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Questo comando elenca al massimo 1000 eventi associati all'ID risorsa specificato che hanno avuto luogo il 04-04-15T04:30 ora locale 2017-04-25T12:30, se l'intero intervallo di data/ora non è precedente a 90 giorni dalla data/ora corrente, ad esempio il periodo di conservazione.

### Esempio 17: Ottenere un log eventi in base al provider di risorse
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

Questo comando elenca al massimo 1000 eventi associati al provider di risorse specificato, che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.

### Esempio 18: Ottenere un log eventi per provider di risorse con un numero massimo di eventi
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

Questo comando elenca al massimo 100 eventi associati al provider di risorse specificato, che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.

### Esempio 19: Ottenere un registro eventi per provider di risorse con un'ora di inizio
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

Questo comando elenca al massimo 1000 eventi associati al provider di risorse specificato che hanno avuto luogo il 05-05-22T04:30:00 ora locale se l'ora di inizio non è precedente a 90 giorni dalla data/ora corrente.

### Esempio 20: Ottenere un log eventi per provider di risorse con un'ora di inizio e un'ora di fine
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Questo comando elenca al massimo 1000 eventi associati al provider di risorse specificato che hanno avuto luogo il 04-04-15T04:30 ora locale 2017-04-25T12:30 se l'intero intervallo di data/ora non è a partire da 90 giorni dalla data/ora corrente, ad esempio il periodo di conservazione.

## PARAMETERS

### -Caller
Il chiamante degli eventi da recuperare

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

### -CorrelationId
Id correlazione

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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

### -DetailedOutput
Restituire l'oggetto con tutti i dettagli degli eventi (per impostazione predefinita vengono restituiti solo alcuni attributi, ad esempio nessun dettaglio)

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndTime
EndTime della query

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxRecord
Numero massimo di record da recuperare.
Alias: MaxRecords, MaxEvents

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
L'ID Risorsa

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceProvider
Nome ResourceProvider

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartTime
Id di correlazione della query

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Stato
Stato degli eventi da recuperare

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

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.String

### System.Management.Automation.SwitchParameter

### System.Int32

## OUTPUT

### Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData

## NOTE

## COLLEGAMENTI CORRELATI
