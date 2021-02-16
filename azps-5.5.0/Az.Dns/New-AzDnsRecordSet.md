---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: bb2e9a9729ed911902e493422109cae764ad6d5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209618"
---
# New-AzDnsRecordSet

## SYNOPSIS
Crea un set di record DNS.

## SINTASSI

### Campi (impostazione predefinita)
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasFields
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Oggetto
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasObject
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzDnsRecordSet** crea un nuovo record DNS (Domain Name System) con il nome specificato e digita nell'area specificata.
Un **oggetto RecordSet** è un set di record DNS con lo stesso nome e tipo.
Si noti che il nome è relativo all'area e non al nome completo.
Il *parametro DnsRecords* specifica i record nel set di record.
Questo parametro accetta una matrice di record DNS, costruita con New-AzDnsRecordConfig.
È possibile usare l'operatore della pipeline per passare un oggetto **DnsZone** a questo cmdlet oppure passare un oggetto **DnsZone** come parametro *Zone* oppure, in alternativa, è possibile specificare l'area in base al nome.
È possibile usare il *parametro Confirm* $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.
Se esiste già **un RecordSet** corrispondente (stesso nome e tipo di record), è necessario specificare il parametro *Overwrite,* altrimenti il cmdlet non creerà un nuovo **RecordSet.**

## ESEMPI

### Esempio 1: Creare un recordSet di tipo A
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

In questo esempio viene **creato un recordSet** denominato www nell'area myzone.com.
Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).
Contiene un singolo record DNS.

### Esempio 2: Creare un recordSet di tipo AAAA
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

In questo esempio viene **creato un recordSet** denominato www nell'area myzone.com.
Il set di record è di tipo AAAA e ha un TTL di 1 ora (3600 secondi).
Contiene un singolo record DNS.
Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 3: Creare un recordSet di tipo CNAME
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

In questo esempio viene **creato un recordSet** denominato www nell'area myzone.com.
Il set di record è di tipo CNAME e ha un TTL di 1 ora (3600 secondi).
Contiene un singolo record DNS.
Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 4: Creare un recordSet di tipo MX
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Questo comando crea un **recordSet** denominato www nell'area myzone.com.
Il set di record è di tipo MX e ha un TTL di 1 ora (3600 secondi).
Contiene un singolo record DNS.
Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 5: Creare un recordSet di tipo NS
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Questo comando crea un **recordSet** denominato ns1 nell'area myzone.com.
Il set di record è di tipo NS e ha un TTL di 1 ora (3600 secondi).
Contiene un singolo record DNS.
Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 6: Creare un RecordSet di tipo PTR
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

Questo comando crea un **recordSet** denominato 4 nell'3.2.1.in-addr.arpa.
Il set di record è di tipo PTR e ha un TTL di 1 ora (3600 secondi).
Contiene un singolo record DNS.
Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 7: Creare un recordSet di tipo SRV
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Questo comando crea un **recordSet** denominato _sip._tcp nell'area myzone.com.
Il set di record è di tipo SRV e ha un TTL di 1 ora (3600 secondi).
Contiene un singolo record DNS che punta all'indirizzo IP 2001.2.3.4.
Il servizio (sip) e il protocollo (tcp) vengono specificati come parte del nome del set di record, non come parte dei dati del record.
Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 8: Creare un recordSet di tipo TXT
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Questo comando crea un **recordSet denominato** testo nell'area myzone.com.
Il set di record è di tipo TXT e ha un TTL di 1 ora (3600 secondi).
Contiene un singolo record DNS.
Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 9: Creare un recordSet nell'apice zone
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Questo comando crea un **recordSet** in corrispondenza dell'apice (o radice) della myzone.com.
A questo scopo, il nome del set di record viene specificato come "@" (incluse le virgolette doppie).
Non è possibile creare record CNAME nell'apice di un'area.
Questo è un vincolo degli standard DNS; non è una limitazione del DNS di Azure.
Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 10: Creare un set di record con caratteri jolly
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Questo comando crea un **recordSet** denominato * nell'area myzone.com.
Si tratta di un set di record con caratteri jolly.
Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.

### Esempio 11: Creare un set di record vuoto
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

Questo comando crea un **recordSet** denominato www nell'area myzone.com.
Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).
Si tratta di un set di record vuoto, che funge da segnaposto a cui è possibile aggiungere in seguito i record.

### Esempio 12: Creare un set di record ed eliminare tutte le conferme
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

Questo comando crea un **recordSet.**
Il *parametro Overwrite* assicura che questo set di record sovrascriva qualsiasi set di record pre-esistente con lo stesso nome e lo stesso tipo. I record esistenti in tale set di record andranno persi.
Il *parametro Confirm* con valore $False elimina la richiesta di conferma.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure

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

### -DnsRecords
Specifica la matrice di record DNS da includere nel set di record.
È possibile usare il cmdlet New-AzDnsRecordConfig per creare oggetti record DNS.
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

### -Metadata
Specifica una matrice di metadati da associare al recordSet.
I metadati vengono specificati usando coppie nome-valore rappresentate come tabelle hash, ad esempio @{"dept"="shopping";" env"="production"}.

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

### -Name
Specifica il nome del **recordSet** da creare.

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

### -Overwrite
Indica che questo cmdlet sovrascrive il **recordSet** specificato, se esiste già.

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
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- I record TXT SOA vengono creati automaticamente al momento della creazione dell'area e non possono essere creati manualmente.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il gruppo di risorse che contiene l'area DNS.
È anche necessario specificare il *parametro ZoneName* per specificare il nome dell'area.
In alternativa, è possibile specificare l'area e il gruppo di risorse passando un oggetto Dns Zone usando il *parametro Zone.*

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceId
ID risorsa di destinazione alias.

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ttl
Specifica il valore Time to Live (TTL) per il recordSet DNS.

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Specifica il valore DnsZone in cui creare il **recordSet.**
In alternativa, è possibile specificare l'area usando *i parametri ZoneName* e *ResourceGroupName.*

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
Specifica il nome dell'area in cui creare il **recordSet.**
È anche necessario specificare il gruppo di risorse che contiene l'area usando *il parametro ResourceGroupName.*
In alternativa, è possibile specificare l'area e il gruppo di risorse passando un oggetto Dns Zone usando il *parametro Zone.*

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

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
Mostra cosa accadrebbe se il cmdlet viene eseguito.
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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### System.UInt32

### Microsoft.Azure.Management.Dns.Models.RecordType

### System.Collections.Hashtable

### Microsoft.Azure.Commands.Dns.DnsRecordBase[]

## OUTPUT

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## NOTE
È possibile usare il *parametro Confirm* per controllare se il cmdlet richiede conferma.
Per impostazione predefinita, il cmdlet chiede conferma se la variabile $ConfirmPreference Windows PowerShell ha un valore medio o inferiore.
Se si specifica *Conferma* o *Conferma:$True,* questo cmdlet richiede conferma prima dell'esecuzione.
Se si specifica *Conferma:$False,* il cmdlet non richiede conferma.

## COLLEGAMENTI CORRELATI

[Add-AzDnsRecordConfig](./Add-AzDnsRecordConfig.md)

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordConfig](./New-AzDnsRecordConfig.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
