---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
ms.openlocfilehash: 4ceba6333d382b48e8e93ce6c63bde9e02b8f7ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522135"
---
# New-AzureRmDnsRecordSet

## Sinossi
Crea un set di record DNS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### Campi
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Oggetto
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureRmDnsRecordSet** crea un nuovo record DNS (Domain Name System) impostato con il nome e il tipo specificati nella zona specificata.
Un oggetto **Recordset** è un set di record DNS con lo stesso nome e tipo.
Tieni presente che il nome è relativo all'area e non il nome completo.

Il parametro *DnsRecords* specifica i record nel set di record.
Questo parametro accetta una matrice di record DNS, costruita con New-AzureRmDnsRecordConfig.

Puoi usare l'operatore pipeline per passare un oggetto **dnsZone** a questo cmdlet oppure puoi passare un oggetto **dnsZone** come parametro *zone* oppure puoi specificare la zona per nome.

Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.

Se un **oggetto recordset** corrispondente esiste già (stesso nome e tipo di record), è necessario specificare il parametro *overwrite* , altrimenti il cmdlet non creerà un nuovo **Recordset** .

## ESEMPI

### Esempio 1: creare un RecordSet di tipo A
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzureRmDnsRecordConfig to add each record to the $Records array,
# then call New-AzureRmDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.
Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).
Contiene un singolo record DNS.

### Esempio 2: creare un RecordSet di tipo AAAA
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.
Il set di record è di tipo AAAA e ha un TTL di 1 ora (3600 secondi).
Contiene un singolo record DNS.

Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 3: creare un RecordSet di tipo CNAME
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.
Il set di record è di tipo CNAME e ha un TTL di 1 ora (3600 secondi).
Contiene un singolo record DNS.

Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 4: creare un RecordSet di tipo MX
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Questo comando crea un **Recordset** denominato www nella zona MyZone.com.
Il set di record è di tipo MX e ha un TTL di 1 ora (3600 secondi).
Contiene un singolo record DNS.

Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 5: creare un RecordSet di tipo NS
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Questo comando crea un **Recordset** denominato NS1 nella zona MyZone.com.
Il set di record è di tipo NS e ha un TTL di 1 ora (3600 secondi).
Contiene un singolo record DNS.

Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 6: creare un RecordSet di tipo PTR
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

Questo comando crea un **Recordset** denominato 4 nella zona 3.2.1.in-addr. arpa.
Il set di record è di tipo PTR e ha un TTL di 1 ora (3600 secondi).
Contiene un singolo record DNS.

Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 7: creare un RecordSet di tipo SRV
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Questo comando crea un **Recordset** denominato _sip. _tcp nella zona MyZone.com.
Il set di record è di tipo SRV e ha un TTL di 1 ora (3600 secondi).
Contiene un singolo record DNS, che punta all'indirizzo IP 2001.2.3.4.

Il servizio (SIP) e il protocollo (TCP) vengono specificati come parte del nome del set di record, non come parte dei dati del record.

Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 8: creare un RecordSet di tipo TXT
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Questo comando crea un **Recordset** denominato Text nella zona MyZone.com.
Il set di record è di tipo TXT e ha un TTL di 1 ora (3600 secondi).
Contiene un singolo record DNS.

Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 9: creare un RecordSet nella zona Apex
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Questo comando crea un **Recordset** all'apice (o radice) della zona MyZone.com.
A tale scopo, il nome del set di record viene specificato come "@" (incluse le virgolette doppie).

Non è possibile creare record CNAME all'apice di una zona.
Questo è un vincolo degli standard DNS; non si tratta di una limitazione di Azure DNS.

Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 10: creare un set di record con caratteri jolly
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Questo comando crea un **Recordset** denominato * nella zona MyZone.com.
Si tratta di un set di record con caratteri jolly.

Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 11: creare un set di record vuoto
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

Questo comando crea un **Recordset** denominato www nella zona MyZone.com.
Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).
Si tratta di un set di record vuoto, che funge da segnaposto a cui è possibile aggiungere più tardi i record.

### Esempio 12: creare un set di record ed eliminare tutte le conferme
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

Questo comando crea un **Recordset**.
Il *parametro overwrite garantisce* che questo set di record sovrascriva qualsiasi set di record preesistente con lo stesso nome e tipo (i record esistenti in tale set di record andranno perduti).
Il parametro *Confirm* con un valore di $false Elimina la richiesta di conferma.

## PARAMETRI

### -DnsRecords
Specifica la matrice di record DNS da includere nel set di record.
Puoi usare il cmdlet New-AzureRmDnsRecordConfig per creare oggetti record DNS.
Per altre informazioni, vedere gli esempi.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Questo parametro è deprecato per questo cmdlet.
Verrà rimosso in una versione futura.

Per controllare se questo cmdlet richiede la confirmazione, usare il parametro *Confirm* .

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

### -Metadata
Specifica una matrice di metadati da associare al RecordSet.
I metadati vengono specificati usando coppie nome/valore rappresentate come tabelle hash, ad esempio @ (@ {"Name" = "Dept"; "Value" = "shopping"}, @ {"Name" = "ENV"; "Value" = "Production"}).

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Specifica il nome del **Recordset** da creare.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sovrascrivere
Indica che questo cmdlet sovrascrive il **Recordset** specificato se esiste già.

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

### -RecordType
Specifica il tipo di record DNS da creare.

I valori validi sono:

- Un
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- TXT

I record SOA vengono creati automaticamente quando la zona viene creata e non può essere creata manualmente.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il gruppo di risorse che contiene la zona DNS.
Devi anche specificare il parametro *zonename* per specificare il nome della zona.

In alternativa, puoi specificare il gruppo zona e risorse passando un oggetto zona DNS usando il parametro *zone* .

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

### -TTL
Specifica il TTL (time to Live) per il RecordSet DNS.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zona
Specifica il DnsZone in cui creare il **Recordset**.
In alternativa, puoi specificare la zona usando i parametri *zonename* e *ResourceGroupName* .

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Zonename
Specifica il nome dell'area in cui creare il **Recordset**.
Devi anche specificare il gruppo di risorse che contiene la zona usando il parametro *ResourceGroupName* .

In alternativa, puoi specificare il gruppo zona e risorse passando un oggetto zona DNS usando il parametro *zone* .

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

### Microsoft. Azure. Commands. DNS. DnsZone
Puoi reindirizzare un oggetto DnsZone a questo cmdlet.

## OUTPUT

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Questo cmdlet restituisce un oggetto **Recordset** .

## Note
Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.
Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.

Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.
Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.

## COLLEGAMENTI CORRELATI

[Add-AzureRmDnsRecordConfig](./Add-AzureRmDnsRecordConfig.md)

[Get-AzureRmDnsRecordSet](./Get-AzureRmDnsRecordSet.md)

[New-AzureRmDnsRecordConfig](./New-AzureRmDnsRecordConfig.md)

[Remove-AzureRmDnsRecordSet](./Remove-AzureRmDnsRecordSet.md)

[Set-AzureRmDnsRecordSet](./Set-AzureRmDnsRecordSet.md)
