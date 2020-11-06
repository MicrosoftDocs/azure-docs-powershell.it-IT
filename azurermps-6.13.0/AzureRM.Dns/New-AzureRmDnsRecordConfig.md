---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
ms.openlocfilehash: 6c2acfe611a8b2c5ef9ecb11173ca9e5210e00e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507459"
---
# New-AzureRmDnsRecordConfig

## Sinossi
Crea un nuovo oggetto local record DNS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### Un
```
New-AzureRmDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Aaaa
```
New-AzureRmDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### NS
```
New-AzureRmDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MX
```
New-AzureRmDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PTR
```
New-AzureRmDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Txt
```
New-AzureRmDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SRV
```
New-AzureRmDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CName
```
New-AzureRmDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CAA
```
New-AzureRmDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureRmDnsRecordConfig** crea un oggetto **DnsRecord** locale.
Una matrice di questi oggetti viene passata al cmdlet New-AzureRmDnsRecordSet usando il parametro *DnsRecords* per specificare i record da creare nel set di record.

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

## PARAMETRI

### -CaaFlags
I contrassegni per il record CAA da aggiungere. Deve essere un numero compreso tra 0 e 255.

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CaaTag
Campo tag del record CAA da aggiungere.

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CaaValue
Campo valore per il record CAA da aggiungere.

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CNAME
Specifica il nome di dominio per un record di nome canonico (CNAME).

```yaml
Type: System.String
Parameter Sets: CName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -Exchange
Specifica il nome del server di posta Exchange per un record MX (mail Exchange).

```yaml
Type: System.String
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Indirizzoipv4
Specifica un indirizzo IPv4 per un record A.

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Indirizzoipv6
Specifica un indirizzo IPv6 per un record AAAA.

```yaml
Type: System.String
Parameter Sets: Aaaa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nsdname
Specifica il nome del server dei nomi per un record NS (Name Server).

```yaml
Type: System.String
Parameter Sets: Ns
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Porta
Specifica la porta per un record di servizio (SRV).

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Preferenza
Specifica la preferenza per un record MX.

```yaml
Type: System.UInt16
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priorità
Specifica la priorità per un record SRV.

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ptrdname
Specifica il nome di dominio di destinazione di un record di risorsa puntatore (PTR).

```yaml
Type: System.String
Parameter Sets: Ptr
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Destinazione
Specifica la destinazione per un record SRV.

```yaml
Type: System.String
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Valore
Specifica il valore per un record TXT.

```yaml
Type: System.String
Parameter Sets: Txt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Peso
Specifica il peso per un record SRV.

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

### System. UInt16

### System. byte

## OUTPUT

### Microsoft. Azure. Commands. DNS. DnsRecordBase

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureRmDnsRecordConfig](./Add-AzureRmDnsRecordConfig.md)

[New-AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[Remove-AzureRmDnsRecordConfig](./Remove-AzureRmDnsRecordConfig.md)
