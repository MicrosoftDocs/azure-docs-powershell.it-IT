---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 715fc15fbafe2f0ba1b4c6782bed607f9878bd55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974126"
---
# Set-AzStorageServiceMetricsProperty

## SYNOPSIS
Modifica le proprietà delle metriche per il servizio archiviazione di Azure.

## SINTASSI

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Set-AzStorageServiceMetricsProperty** modifica le proprietà delle metriche per il servizio di archiviazione di Azure.

## ESEMPI

### Esempio 1: Modificare le proprietà delle metriche per il servizio BLOB
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

Questo comando modifica le metriche della versione 1.0 per l'archiviazione BLOB a un livello di servizio.
Le metriche del servizio Archiviazione di Azure conservano le voci per 10 giorni.
Poiché questo comando specifica il *parametro PassThru,* il comando visualizza le proprietà modificate per le metriche.

## PARAMETERS

### -Context
Specifica un contesto di archiviazione di Azure.
Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.

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

### -MetricsLevel
Specifica il livello di metriche che viene utilizzato da Archiviazione di Azure per il servizio.
I valori accettabili per questo parametro sono:
- Nessuno
- Servizio
- ServiceAndApi

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MetricsType
Specifica un tipo di metriche.
Questo cmdlet imposta il tipo di metriche del servizio di archiviazione di Azure sul valore specificato da questo parametro.
I valori accettabili per questo parametro sono: Ora e Minuto.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Indica che questo cmdlet restituisce le proprietà aggiornate delle metriche.
Se non si specifica questo parametro, questo cmdlet non restituisce un valore.

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

### -RetentionDays
Specifica il numero di giorni per cui il servizio di archiviazione di Azure conserva le informazioni sulle metriche.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Specifica il tipo di servizio di archiviazione.
Questo cmdlet modifica le proprietà delle metriche per il tipo di servizio specificato da questo parametro.
I valori accettabili per questo parametro sono:
- BLOB 
- tavolo
- Coda
- File Il valore di File non è attualmente supportato.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Specifica la versione delle metriche di Archiviazione di Azure.
Il valore predefinito è 1,0.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## OUTPUT

### Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzStorageServiceMetricsProperty](./Get-AzStorageServiceMetricsProperty.md)

[New-AzStorageContext](./New-AzStorageContext.md)


