---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 687838573459c09ceaf08c0d1c3335caa4a99769
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859753"
---
# Get-AzsStorageQuota

## Sinossi
Restituisce un elenco di quote di archiviazione nella posizione specificata.

## SINTASSI

### Elenco (impostazione predefinita)
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### Ottieni
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## Descrizione
Restituisce un elenco di quote di archiviazione nella posizione specificata.

## ESEMPI

### ESEMPIO 1
```
Get-AzsStorageQuota
```

Ottenere l'elenco delle quote di archiviazione.

### ESEMPIO 2
```
Get-AzsStorageQuota -Name "storagequota1"
```

Ottenere i dettagli della quota di archiviazione specificata per nome.

## PARAMETRI

### -Nome
Nome della quota di archiviazione.

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Posizione
Posizione delle risorse.

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID risorsa.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Skip
Ignorare i primi elementi N specificati dal valore del parametro.

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inizio pagina
Restituisce i primi N elementi come specificato dal valore del parametro.
Si applica dopo il parametro-Skip.

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. AzureStack. Management. storage. admin. Models. StorageQuota consente

## Note

## COLLEGAMENTI CORRELATI
