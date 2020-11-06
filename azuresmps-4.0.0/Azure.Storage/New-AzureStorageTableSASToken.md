---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: ''
schema: 2.0.0
ms.openlocfilehash: 39870fe9fe9ac4223bccf15908c960db29d25252
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507227"
---
# New-AzureStorageTableSASToken

## Sinossi
Genera un token SAS per una tabella di archiviazione di Azure.

## SINTASSI

### SasPolicy
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### SasPermission
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureStorageTableSASToken** genera un token SAS (Shared Access Signature) per una tabella di archiviazione di Azure.

## ESEMPI

### Esempio 1: generare un token SAS con autorizzazioni complete per una tabella
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

Questo comando genera un token SAS con autorizzazioni complete per la tabella denominata ContosoResources.
Il token è per le autorizzazioni di lettura, aggiunta, aggiornamento ed eliminazione.

### Esempio 2: generare un token SAS per un intervallo di partizioni
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

Questo comando genera e token SAS con autorizzazioni complete per la tabella denominata ContosoResources.
Il comando limita il token all'intervallo specificato dai parametri *StartPartitionKey* e *EndPartitionKey* .

### Esempio 3: generare un token SAS con criteri di accesso archiviati per una tabella
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

Questo comando genera un token SAS per la tabella denominata ContosoResources.
Il comando specifica i criteri di accesso archiviati denominati ClientPolicy01.

## PARAMETRI

### -Contesto
Specifica un contesto di archiviazione di Azure.
Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -EndPartitionKey
Specifica la chiave di partizione della fine dell'intervallo per il token creato da questo cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndRowKey
Specifica la chiave della riga per la fine dell'intervallo per il token creato da questo cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryTime
Specifica quando scade il token SAS.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullUri
Indica che questo cmdlet restituisce l'URI della coda completa con il token SAS.

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

### -IPAddressOrRange
Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.
L'intervallo è incluso.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome di una tabella di archiviazione di Azure.
Questo cmdlet crea un token SAS per la tabella specificata da questo parametro.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Autorizzazione
Specifica le autorizzazioni per una tabella di archiviazione di Azure.

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Policy
Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS.

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocollo
Specifica il protocollo consentito per una richiesta.
I valori accettabili per questo parametro sono i seguenti:
* HttpsOnly
* HttpsOrHttp

Il valore predefinito è HttpsOrHttp.

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartPartitionKey
Specifica la chiave di partizione dell'inizio dell'intervallo per il token creato da questo cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRowKey
Specifica la chiave di riga per l'inizio dell'intervallo per il token creato da questo cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Specifica quando il token SAS diventa valido.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[New-AzureStorageContext](./New-AzureStorageContext.md)
