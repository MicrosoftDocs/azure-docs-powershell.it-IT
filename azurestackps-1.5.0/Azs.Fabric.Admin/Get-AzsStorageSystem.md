---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 362eb6a8d688aab2276fa1166f65474dab488952
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490901"
---
# Get-AzsStorageSystem

## Sinossi
Restituisce un elenco di tutti i sottosistemi di archiviazione per una posizione.

## SINTASSI

### Elenco (impostazione predefinita)
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### Ottieni
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## Descrizione
Restituisce un elenco di tutti i sottosistemi di archiviazione per una posizione.

## ESEMPI

### --------------------------ESEMPIO 1--------------------------
```
Get-AzsStorageSystem
```

Ottenere tutti i sottosistemi di archiviazione da una posizione.

### --------------------------ESEMPIO 2--------------------------
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

Ottenere un sottosistema di archiviazione assegnato un percorso e un nome.

## PARAMETRI

### -Filtro
Parametro di filtro OData.

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Posizione
Posizione della risorsa.

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

### -Nome
Gruppo di risorse in cui è stato registrato il provider di risorse.

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

### -ResourceGroupName
Gruppo di risorse in cui è stato registrato il provider di risorse.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. AzureStack. Management. Fabric. admin. Models. StorageSystem

## Note

## COLLEGAMENTI CORRELATI

