---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f80dc6e4ea41f85464860415faa0c04dbeee3d07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674507"
---
# Remove-AzDnsRecordSet

## Sinossi
Elimina un set di record.

## SINTASSI

### Campi
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Misto
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Oggetto
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzDnsRecordSet** Elimina il set di record specificato dalla zona specificata.
Non è possibile eliminare i record SOA o Name Server (NS) creati automaticamente nella zona Apex.
Puoi passare un oggetto **Recordset** a questo cmdlet usando l'operatore pipeline o come parametro.
Per identificare un record impostato per nome e tipo senza usare un oggetto **Recordset** , devi passare la zona come oggetto **dnsZone** a questo cmdlet usando l'operatore della pipeline o come parametro oppure puoi specificare i parametri *zonename* e *ResourceGroupName* .
Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.
Quando specifichi il set di record usando un oggetto **Recordset** , il set di record non viene eliminato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **Recordset** locale.
In questo articolo viene fornita la protezione delle modifiche simultanee.
Puoi eliminarlo usando il parametro *overwrite* , che elimina il set di record indipendentemente dalle modifiche simultanee.

## ESEMPI

### Esempio 1: rimuovere un set di record
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

Il primo comando ottiene il set di record specificato e lo archivia nella variabile $RecordSet. Il secondo comando rimuove il set di record in $RecordSet.

### Esempio 2: rimuovere un set di record ed eliminare tutte le conferme
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

Il primo comando ottiene il set di record specificato.
Il secondo comando Elimina il set di record, anche se è stato modificato nel frattempo.
Le richieste di conferma vengono soppresse.

## PARAMETRI

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome del **Recordset** da rimuovere.
Quando specifichi il record impostato per nome, la zona DNS deve essere specificata usando il parametro *zone* o i parametri *zonename* e *ResourceGroupName* .
In alternativa, il set di record può essere specificato usando un oggetto **Recordset** , passato usando il parametro *Recordset* .

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sovrascrivere
Quando specifichi il set di record usando un oggetto **Recordset** , il set di record non viene eliminato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **Recordset** locale.
In questo articolo viene fornita la protezione delle modifiche simultanee.
Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina il set di record indipendentemente dalle modifiche simultanee.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecordSet
Specifica l'oggetto **Recordset** da rimuovere.
In alternativa, il set di record può essere specificato usando i parametri *Name* e *zone* oppure usando i parametri *Name* , *zonename* e *ResourceGroupName* .

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecordType
Specifica il tipo di record DNS.
I valori validi sono:
- Un
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- I record SOA TXT vengono eliminati automaticamente quando la zona viene eliminata.
Non è possibile eliminare manualmente i record SOA.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il gruppo di risorse che contiene la zona DNS che contiene il **Recordset** da eliminare.
Questo parametro è applicabile solo quando il set di record e la zona DNS vengono specificati usando i parametri *Name* e *zonename* .
In alternativa, puoi specificare il set di record usando il parametro *Recordset* oppure i parametri *Name* e *zone* .

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zona
Specifica la zona DNS che contiene il **Recordset** da eliminare.
Questo parametro è applicabile solo quando specifichi il set di record usando il parametro *Name* .
In alternativa, puoi specificare il set di record usando il parametro *Recordset* oppure i parametri *Name* , *zonename* e *ResourceGroupName* .

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Zonename
Specifica il nome della zona che contiene il **Recordset** da eliminare.
Devi anche specificare i parametri *Name* e *ResourceGroupName* .
In alternativa, il set di record può essere specificato usando il parametro *Recordset* oppure i parametri *Name* e *zone* .

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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

### Microsoft. Azure. Management. DNS. Models. RecordType

### System. String

### Microsoft. Azure. Commands. DNS. DnsZone

### Microsoft. Azure. Commands. DNS. DnsRecordSet

## OUTPUT

### System. Boolean

## Note
Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.
Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.
Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.
Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.

## COLLEGAMENTI CORRELATI

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
