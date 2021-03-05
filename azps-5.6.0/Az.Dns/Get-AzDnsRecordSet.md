---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 447b1e32473d00504446478a9efaa5634e3b1c65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984828"
---
# Get-AzDnsRecordSet

## SYNOPSIS
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

## DESCRIZIONE
Il cmdlet **Get-AzDnsRecordSet** ottiene il set di record DNS (Domain Name System) con il nome e il tipo specificati nell'area specificata.
Se non si specificano i parametri *Name* o *RecordType,* questo cmdlet restituisce tutti i set di record del tipo specificato nell'area.
Se si specifica il *parametro RecordType* ma non il *parametro Name,* questo cmdlet restituisce tutti i set di record del tipo di record specificato.
È possibile usare l'operatore della pipeline per passare un oggetto **DnsZone** a questo cmdlet oppure passare un oggetto **DnsZone** come parametro *Zone* oppure, in alternativa, è possibile specificare l'area e il gruppo di risorse in base al nome.

## ESEMPI

### Esempio 1: Ottenere set di record con un nome e un tipo specificati
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

Questo comando recupera il set di record di tipo A denominato www nel gruppo di risorse e nell'area specificati e quindi lo archivia nella $RecordSet variabile.
Poiché sono *specificati i* parametri Name e *RecordType,* viene restituito un solo **oggetto RecordSet.**

### Esempio 2: Ottenere set di record di un tipo specificato
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

Questo comando recupera una matrice di tutti i set di record di tipo A nell'area denominata myzone.com nel gruppo di risorse denominato MyResourceGroup e quindi li archivia nella variabile $RecordSets variabile.

### Esempio 3: Ottenere tutti i set di record in un'area
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

Questo comando recupera una matrice di tutti i set di record nell'area denominata myzone.com nel gruppo di risorse denominato MyResourceGroup e quindi li archivia nella $RecordSets variabile.

### Esempio 4: Ottenere tutti i set di record in un'area, usando un oggetto DnsZone
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

Questo esempio equivale all'esempio 3 riportato sopra.
Questa volta, il fuso viene specificato usando un oggetto zona.

## PARAMETERS

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

### -Name
Specifica il nome del **recordSet** da ottenere.
Se non si specifica il parametro *Name,* vengono restituiti tutti i set di record del tipo specificato.

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
Specifica il tipo di record DNS che riceve questo cmdlet.
I valori validi sono: 
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SOA
- SRV
- TXT Se non si specifica il *parametro RecordType,* è necessario omettere *anche il parametro Name.* Questo cmdlet restituisce quindi tutti i set di record nell'area (di tutti i nomi e i tipi).

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
Specifica il gruppo di risorse che contiene l'area DNS.
È necessario specificare anche il nome dell'area, usando il *parametro ZoneName.*
In alternativa, è possibile specificare l'area e il gruppo di risorse passando un **oggetto DnsZone** usando il *parametro Zone.*

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

### -Zone
Specifica l'area DNS che contiene il set di record che riceve questo cmdlet.
In alternativa, è possibile specificare l'area usando *i parametri ZoneName* *e ResourceGroupName.*

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

### -ZoneName
Specifica il nome dell'area DNS che contiene il set di record da ottenere.
È necessario specificare anche il gruppo di risorse che contiene l'area, usando il *parametro ResourceGroupName.*
In alternativa, è possibile specificare l'area e il gruppo di risorse passando un oggetto Dns Zone usando il *parametro Zone.*

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## OUTPUT

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## NOTE

## COLLEGAMENTI CORRELATI

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)


