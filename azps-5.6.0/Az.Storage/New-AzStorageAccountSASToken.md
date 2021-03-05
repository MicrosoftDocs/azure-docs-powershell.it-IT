---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 6d399c7ed7c074cd5adaf0579097c0706f46192d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002606"
---
# New-AzStorageAccountSASToken

## SYNOPSIS
Crea un token di firma di accesso condiviso a livello di account.

## SINTASSI

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzStorageSASToken** crea un token di firma di accesso condiviso (SAS) a livello di account per un account di archiviazione di Azure.
È possibile usare il token di firma di accesso condiviso per delegare le autorizzazioni per più servizi o per delegare autorizzazioni per i servizi non disponibili con un token di firma di accesso condiviso a livello di oggetto.

## ESEMPI

### Esempio 1: Creare un token di firma di accesso condiviso a livello di account con autorizzazione completa
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

Questo comando crea un token di firma di accesso condiviso a livello di account con autorizzazioni complete.

### Esempio 2: Creare un token di firma di accesso condiviso a livello di account per un intervallo di indirizzi IP
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

Questo comando crea un token di firma di accesso condiviso a livello di account per le richieste solo HTTPS dall'intervallo specificato di indirizzi IP.

## PARAMETERS

### -Context
Specifica il contesto di archiviazione di Azure.
È possibile usare il cmdlet New-AzStorageContext per ottenere un **oggetto AzureStorageContext.**

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryTime
Specifica l'ora in cui la firma di accesso condiviso diventa non valida.

```yaml
Type: System.Nullable`1[System.DateTime]
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
L'intervallo è inclusivo.

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

### -Permission
Specifica le autorizzazioni per l'account di archiviazione.
Le autorizzazioni sono valide solo se corrispondono al tipo di risorsa specificato.
È importante notare che si tratta di una stringa, ad esempio `rwd` (per Lettura, Scrittura ed Elimina).
Per altre informazioni sui valori di autorizzazione accettabili, vedere Creazione di una firma di accesso condiviso per un account http://go.microsoft.com/fwlink/?LinkId=799514

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

### -Protocol
Specifica il protocollo consentito per una richiesta effettuata con la firma di accesso condiviso dell'account.
I valori accettabili per questo parametro sono:
- HttpsOnly
- HttpsOrHttp Il valore predefinito è HttpsOrHttp.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
Specifica i tipi di risorse disponibili con il token di firma di accesso condiviso.
I valori accettabili per questo parametro sono:
- Nessuno
- Servizio
- Contenitore
- Oggetto

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Service
Specifica il servizio.
I valori accettabili per questo parametro sono:
- Nessuno
- BLOB
- File
- Coda
- tavolo

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Specifica l'ora, come oggetto **DateTime,** in cui la firma di accesso condiviso diventa valida.
Per ottenere un **oggetto DateTime,** usare il cmdlet Get-Date.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## OUTPUT

### System.String

## NOTE

## COLLEGAMENTI CORRELATI

[New-AzStorageBlobSASToken](./New-AzStorageBlobSASToken.md)

[New-azStorageContainersASToken](./New-AzStorageContainerSASToken.md)

[New-azStorageFilesASToken](./New-AzStorageFileSASToken.md)

[New-azStorageQueuesASToken](./New-AzStorageQueueSASToken.md)

[New-azStorageShareSASToken](./New-AzStorageShareSASToken.md)

[New-azStorageTableSASToken](./New-AzStorageTableSASToken.md)


