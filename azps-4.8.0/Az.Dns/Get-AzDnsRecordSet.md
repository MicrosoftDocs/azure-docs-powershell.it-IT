---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: b64432364b9c86a1153ba9a535d70645cf15d4d1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033112"
---
# Get-AzDnsRecordSet

## Sinossi
Ottiene un set di record DNS.

## SINTASSI

### Campi
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Oggetto
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzDnsRecordSet** ottiene il record DNS (Domain Name System) impostato con il nome e il tipo specificati nella zona specificata.
Se non specifichi i parametri *Name* o *RecordType* , questo cmdlet restituisce tutti i set di record del tipo specificato nella zona.
Se specifichi il parametro *RecordType* ma non il parametro *Name* , questo cmdlet restituisce tutti i set di record del tipo di record specificato.
Puoi usare l'operatore pipeline per passare un oggetto **dnsZone** a questo cmdlet oppure puoi passare un oggetto **dnsZone** come parametro di *zona* o in alternativa puoi specificare il gruppo zona e risorsa per nome.

## ESEMPI

### Esempio 1: ottenere set di record con un nome e un tipo specificati
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

Questo comando ottiene il set di record del tipo di record un nome www nel gruppo di risorse e nella zona specificati e lo archivia nella variabile $RecordSet.
Poiché vengono specificati i parametri *Name* e *RecordType* , viene restituito un solo oggetto **Recordset** .

### Esempio 2: ottenere set di record di un tipo specificato
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

Questo comando ottiene una matrice di tutti i set di record del tipo di record a nella zona denominata myzone.com nel gruppo di risorse denominato MyResourceGroup e li archivia nella variabile $RecordSets.

### Esempio 3: ottenere tutti i set di record in una zona
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

Questo comando consente di ottenere una matrice di tutti i set di record nella zona denominata myzone.com nel gruppo di risorse denominato MyResourceGroup e quindi di archiviarli nella variabile $RecordSets.

### Esempio 4: ottenere tutti i set di record in una zona usando un oggetto DnsZone
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

Questo esempio equivale all'esempio 3 precedente.
Questa volta, la zona viene specificata usando un oggetto zone.

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
Specifica il nome del **Recordset** da ottenere.
Se non specifichi il parametro *Name* , verranno restituiti tutti i set di record del tipo specificato.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecordType
Specifica il tipo di record DNS ottenuto da questo cmdlet.
I valori validi sono: 
- Un
- AAAA
- CNAME
- MX
- NS
- PTR
- SOA
- SRV
- TXT se non specifichi il parametro *RecordType* , devi anche omettere il parametro *Name* . Questo cmdlet restituisce quindi tutti i set di record nella zona (di tutti i nomi e i tipi).

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il gruppo di risorse che contiene la zona DNS.
Il nome della zona deve essere specificato anche usando il parametro *zonename* .
In alternativa, puoi specificare il gruppo zona e risorsa passando un oggetto **dnsZone** usando il parametro *zone* .

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
Specifica la zona DNS che contiene il set di record ottenuto da questo cmdlet.
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
Specifica il nome della zona DNS che contiene il record impostato per ottenere.
Il gruppo di risorse che contiene la zona deve essere specificato anche usando il parametro *ResourceGroupName* .
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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

### Microsoft. Azure. Commands. DNS. DnsZone

### System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. Models. RecordType, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

## OUTPUT

### Microsoft. Azure. Commands. DNS. DnsRecordSet

## Note

## COLLEGAMENTI CORRELATI

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)


