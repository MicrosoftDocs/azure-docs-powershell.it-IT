---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: ca480d266f4ab7706841fb901fa714dbe632ec2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508175"
---
# Get-AzureRmDataLakeAnalyticsJob

## Sinossi
Ottiene un processo di analisi dei dati sul lago.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### GetAllInResourceGroupAndAccount (impostazione predefinita)
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetBySpecificJobInformation
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmDataLakeAnalyticsJob** ottiene un processo di analisi del Lago di dati di Azure.
Se non specifichi un processo, questo cmdlet ottiene tutti i processi.

## ESEMPI

### Esempio 1: ottenere un processo specificato
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

Questo comando ottiene il processo con l'ID specificato.

### Esempio 2: ottenere processi inviati nell'ultima settimana
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

Questo comando consente di ottenere i processi inviati nell'ultima settimana.

## PARAMETRI

### -Account
Specifica il nome di un account di analisi dei dati sul lago.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

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

### -Includi
Specifica le opzioni che indicano il tipo di informazioni aggiuntive da recuperare sul processo.
I valori accettabili per questo parametro sono i seguenti:

- Nessuno
- DebugInfo
- Statistiche
- Tutti

```yaml
Type: ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobId
Specifica l'ID del processo da ottenere.

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Nome
Specifica un nome da usare per filtrare i risultati dell'elenco processi.
I valori accettabili per questo parametro sono i seguenti:

- Nessuno
- DebugInfo
- Statistiche
- Tutti

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PipelineId
Un ID facoltativo che indica solo i processi parte della pipeline specificata deve essere restituito.

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecurrenceId
Un ID facoltativo che indica solo i processi parte della ricorrenza specificata deve essere restituito.

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Risultato
Specifica un filtro di risultato per i risultati del processo.
I valori accettabili per questo parametro sono i seguenti:

- Nessuno
- Annullata
- Fallito
- Succeeded

```yaml
Type: JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Stato
Specifica un filtro di stato per i risultati del processo.
I valori accettabili per questo parametro sono i seguenti:

- Accettato
- Nuovo
- Compilazione
- Pianificazione
- Accodati
- Iniziale
- In pausa
- Esecuzione
- Terminato

```yaml
Type: JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubmittedAfter
Specifica un filtro data.
Usa questo parametro per filtrare il risultato dell'elenco processi in processi inviati dopo la data specificata.

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubmittedBefore
Specifica un filtro data.
Usa questo parametro per filtrare il risultato dell'elenco processi in processi inviati prima della data specificata.

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Mittente
Specifica l'indirizzo di posta elettronica di un utente.
Usa questo parametro per filtrare i risultati dell'elenco processi in processi inviati da un utente specificato.

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Inizio pagina
Un valore facoltativo che indica il numero di processi da restituire. Il valore predefinito è 500

```yaml
Type: Int32
Parameter Sets: GetAllInResourceGroupAndAccount
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

### GUID
Il parametro "JobId" accetta il valore di tipo "GUID" dalla pipeline

## OUTPUT

### JobInformation
Dettagli delle informazioni sui processi specificati

### Elenco<PSJobInformationBasic>
L'elenco dei processi nell'account di analisi dei dati del lago specificato.

## Note

## COLLEGAMENTI CORRELATI

[Stop-AzureRmDataLakeAnalyticsJob](./Stop-AzureRmDataLakeAnalyticsJob.md)

[Invia-AzureRmDataLakeAnalyticsJob](./Submit-AzureRmDataLakeAnalyticsJob.md)

[Wait-AzureRmDataLakeAnalyticsJob](./Wait-AzureRmDataLakeAnalyticsJob.md)


