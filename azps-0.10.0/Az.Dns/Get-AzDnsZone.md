---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: fe650e87635d16d3768bd527bf7422fe644c885e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863173"
---
# Get-AzDnsZone

## Sinossi
Ottiene una zona DNS.

## SINTASSI

### Predefinito (impostazione predefinita)
```
Get-AzDnsZone [<CommonParameters>]
```

### ResourceGroup
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzDnsZone** ottiene una zona DNS (Domain Name System) dal gruppo di risorse specificato.
Se specifichi il parametro *Name* , viene restituito un singolo oggetto **dnsZone** .
Se non specifichi il parametro *Name* , viene restituita una matrice contenente tutte le aree del gruppo di risorse specificato.
Puoi usare l'oggetto **dnsZone** per aggiornare la zona, ad esempio puoi aggiungere oggetti **Recordset** .

## ESEMPI

### Esempio 1: ottenere una zona
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

Questo esempio recupera la zona DNS denominata myzone.com dal gruppo di risorse specificato e la archivia nella variabile $Zone.

### Esempio 2: ottenere tutte le aree di un gruppo di risorse
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

Questo esempio recupera tutte le aree DNS nel gruppo di risorse specificato e lo archivia nella variabile $Zones.

### Esempio 3: ottenere tutte le aree di un abbonamento
```
PS C:\> $Zones = Get-AzDnsZone
```

Questo esempio consente di ottenere tutte le aree DNS nell'abbonamento Azure corrente e quindi di archiviarle nella variabile $Zones.

## PARAMETRI

### -Nome
Specifica il nome della zona DNS da ottenere.

Se non specifichi un valore per il parametro *Name* , questo cmdlet ottiene tutte le aree DNS nel gruppo di risorse specificato.
Se si omette anche il parametro *ResourceGroupName* , questo cmdlet recupera tutte le aree DNS nell'abbonamento Azure corrente.

```yaml
Type: String
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
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non consente di reindirizzare l'input.

## OUTPUT

### Microsoft. Azure. Commands. DNS. DnsZone
Questo cmdlet restituisce un oggetto che rappresenta la zona DNS.
Se il nome della zona non è specificato, viene restituita una matrice di oggetti zone.

## Note

## COLLEGAMENTI CORRELATI

[New-AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
