---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: 1b2ee31c136c24478ddd69d58c264ce44886c057
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861538"
---
# Set-AzDnsRecordSet

## Sinossi
Aggiorna un set di record DNS.

## SINTASSI

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzDnsRecordSet** aggiorna un set di record nel servizio Azure DNS da un oggetto **Recordset** locale.

Puoi passare un oggetto **Recordset** come parametro o usando l'operatore pipeline.

Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.

Il set di record non viene aggiornato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **Recordset** locale.
In questo articolo viene fornita la protezione delle modifiche simultanee.
Puoi eliminare questo comportamento usando il parametro *overwrite* , che aggiorna il set di record indipendentemente dalle modifiche simultanee.

## ESEMPI

### Esempio 1: aggiornare un set di record
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

Il primo comando usa il cmdlet Get-AzDnsRecordSet per ottenere il set di record specificato e lo archivia nella variabile $RecordSet.

Il secondo e il terzo comando sono operazioni off-line per aggiungere due record al set di record.

Il comando finale usa il cmdlet **set-AzDnsRecordSet** per eseguire il commit dell'aggiornamento.

### Esempio 2: aggiornare un record SOA
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

Il primo comando usa il cmdlet **Get-AzDnsRecordset** per ottenere il set di record specificato e lo archivia nella variabile $recordset.

Il secondo comando Aggiorna il record SOA specificato in $RecordSet.

Il comando Final usa il cmdlet **set-AzDnsRecordSet** per propagare l'aggiornamento in $recordset.

## PARAMETRI

### -Sovrascrivere
Indica di aggiornare il set di record indipendentemente dalle modifiche simultanee.

Il set di record non verrà aggiornato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **Recordset** locale.
In questo articolo viene fornita la protezione delle modifiche simultanee.
Per eliminare questo comportamento, puoi usare il parametro *overwrite* , che determina l'aggiornamento del set di record indipendentemente dalle modifiche simultanee.

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

### -RecordSet
Specifica il **Recordset** da aggiornare.

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
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
Mostra cosa succede se il cmdlet viene eseguito. Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Puoi passare un oggetto **Recordset** a questo cmdlet.

## OUTPUT

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Questo cmdlet restituisce un oggetto che rappresenta l'oggetto **Recordset** aggiornato.

## Note
Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.
Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.

Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.
Se si specifica *Confirm: $false* , il cmdlet non chiede conferma. 

## COLLEGAMENTI CORRELATI

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)
