---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: ''
schema: 2.0.0
ms.openlocfilehash: c12c5532a85bacb5cd854f4f2ad87ad0d8b68178
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867116"
---
# Remove-AzureRmDnsZone

## Sinossi
Rimuove una zona DNS da un gruppo di risorse.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### Campi
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Oggetto
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzureRmDnsZone** Elimina definitivamente una zona DNS (Domain Name System) da un gruppo di risorse specificato.
Vengono eliminati anche tutti i set di record contenuti nella zona.

Puoi passare un oggetto **dnsZone** usando il parametro *Name* oppure usando l'operatore pipeline o in alternativa puoi specificare i parametri *zonename* e *ResourceGroupName* .

Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.

Quando specifichi la zona usando un oggetto **dnsZone** (passato tramite il parametro pipeline o *zone* ), la zona non viene eliminata se è stata modificata in Azure DNS poiché l'oggetto **dnsZone** locale è stato recuperato (solo le operazioni direttamente nel conteggio delle risorse di zona DNS come le modifiche, le operazioni sui set di record all'interno della zona non).
Ciò offre protezione per le modifiche di zona simultanee.
Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina la zona indipendentemente dalle modifiche simultanee.

## ESEMPI

### Esempio 1: rimuovere un'area
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Questo comando rimuove la zona denominata myzone.com dal gruppo di risorse denominato MyResourceGroup.

## PARAMETRI

### -Force
Questo parametro è deprecato per questo cmdlet.
Verrà rimosso in una versione futura.

Per verificare se questo cmdlet richiede la conferma, usare il parametro *Confirm* .

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

### -Nome
Specifica il nome dell'area DNS rimossa da questo cmdlet.
Devi anche specificare il parametro *ResourceGroupName* .

In alternativa, puoi specificare la zona DNS usando il parametro *zone* .

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sovrascrivere
Quando specifichi la zona usando un oggetto **dnsZone** (passato tramite il parametro pipeline o *zone* ), la zona non viene eliminata se è stata modificata in Azure DNS poiché l'oggetto **dnsZone** locale è stato recuperato (solo le operazioni direttamente nel conteggio delle risorse di zona DNS come le modifiche, le operazioni sui set di record all'interno della zona non).
Ciò offre protezione per le modifiche di zona simultanee.

Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina la zona indipendentemente dalle modifiche simultanee.

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
PassThru

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

### -ResourceGroupName
Specifica il nome del gruppo di risorse che contiene la zona da rimuovere.
Devi anche specificare il parametro *zonename* .

In alternativa, puoi specificare la zona DNS usando un oggetto **dnsZone** , passato tramite il parametro pipeline o *zone* .

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zona
Specifica la zona DNS da eliminare.
L'oggetto **dnsZone** passato può essere passato anche tramite la pipeline.

In alternativa, puoi specificare la zona DNS da eliminare usando i parametri *zonename* e *ResourceGroupName* .

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. DNS. DnsZone
Puoi reindirizzare un oggetto **dnsZone** a questo cmdlet.

## OUTPUT

### Nessuno
Questo cmdlet non genera alcun output.

## Note
A causa dell'impatto potenzialmente elevato dell'eliminazione di una zona DNS, per impostazione predefinita, questo cmdlet richiede la conferma se la $ConfirmPreference variabile di Windows PowerShell contiene un valore diverso da None.

Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.
Se si specifica *Confirm: $false* , il cmdlet non chiede conferma. 

## COLLEGAMENTI CORRELATI

[Get-AzureRmDnsZone](./Get-AzureRmDnsZone.md)

[New-AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Set-AzureRmDnsZone](./Set-AzureRmDnsZone.md)
