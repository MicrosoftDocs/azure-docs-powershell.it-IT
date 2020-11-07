---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
ms.openlocfilehash: eabf0809aebf50458d15b195a5ec9afc4f0b9cf1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687527"
---
# Get-AzureRmDnsZone

## Sinossi
Ottiene una zona DNS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### Predefinito (impostazione predefinita)
```
Get-AzureRmDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroup
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmDnsZone** ottiene una zona DNS (Domain Name System) dal gruppo di risorse specificato.
Se specifichi il parametro *Name* , viene restituito un singolo oggetto **dnsZone** .
Se non specifichi il parametro *Name* , viene restituita una matrice contenente tutte le aree del gruppo di risorse specificato.
Puoi usare l'oggetto **dnsZone** per aggiornare la zona, ad esempio puoi aggiungere oggetti **Recordset** .

## ESEMPI

### Esempio 1: ottenere una zona
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

Questo esempio recupera la zona DNS denominata myzone.com dal gruppo di risorse specificato e la archivia nella variabile $Zone.

### Esempio 2: ottenere tutte le aree di un gruppo di risorse
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

Questo esempio recupera tutte le aree DNS nel gruppo di risorse specificato e lo archivia nella variabile $Zones.

### Esempio 3: ottenere tutte le aree di un abbonamento
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

Questo esempio consente di ottenere tutte le aree DNS nell'abbonamento Azure corrente e quindi di archiviarle nella variabile $Zones.

## PARAMETRI

### -Nome
Specifica il nome della zona DNS da ottenere.

Se non specifichi un valore per il parametro *Name* , questo cmdlet ottiene tutte le aree DNS nel gruppo di risorse specificato.
Se si omette anche il parametro *ResourceGroupName* , questo cmdlet recupera tutte le aree DNS nell'abbonamento Azure corrente.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse che contiene la zona DNS da ottenere.

Se non specifichi *ResourceGroupName* , devi anche omettere il parametro *Name* .
In questo caso, questo cmdlet ottiene tutte le aree DNS nell'abbonamento Azure corrente.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non consente di reindirizzare l'input.

## OUTPUT

### Microsoft. Azure. Commands. DNS. DnsZone
Questo cmdlet restituisce un oggetto che rappresenta la zona DNS.
Se il nome della zona non è specificato, viene restituita una matrice di oggetti zone.

## Note

## COLLEGAMENTI CORRELATI

[New-AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Remove-AzureRmDnsZone](./Remove-AzureRmDnsZone.md)

[Set-AzureRmDnsZone](./Set-AzureRmDnsZone.md)
