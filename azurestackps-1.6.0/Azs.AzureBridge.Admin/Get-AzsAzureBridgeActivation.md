---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 811a69b8d18c5e723702f73873188961f2739360
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2020
ms.locfileid: "93522194"
---
# Get-AzsAzureBridgeActivation

## Sinossi
Restituisce l'attivazione di Azure Bridge.

## SINTASSI

### Elenco (impostazione predefinita)
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### Ottieni
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### ResourceId
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## Descrizione
Una volta registrata la pila di Azure, l'oggetto di attivazione contiene informazioni che collegano una distribuzione di Azure stack alla relativa registrazione in Azure, ad esempio la data di scadenza della registrazione, il nome e così via.

## ESEMPI

### --------------------------ESEMPIO 1--------------------------
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

Ottenere un elenco delle attivazioni di Azure Bridge nel gruppo risorse "activationRG"

### --------------------------ESEMPIO 2--------------------------
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

Ottenere un'attivazione di Azure Bridge per nome "attivazione" situata in "activationRG"

## PARAMETRI

### -Nome
Nome dell'attivazione.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gruppo di risorse usato durante la registrazione di Azure stack; è anche possibile visualizzare i nomi dei gruppi di risorse nel portale.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
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

### Microsoft. AzureStack. Management. AzureBridge. admin. Models. ActivationResource

## Note

## COLLEGAMENTI CORRELATI

