---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180750"
---
# Remove-AzDnsRecordSet

## SYNOPSIS
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

## DESCRIZIONE
Il cmdlet **Remove-AzDnsRecordSet** elimina il set di record specificato dall'area specificata.
Non è possibile eliminare record SOA o server dei nomi (NS) creati automaticamente in corrispondenza dell'apice di zona.
È possibile passare un **oggetto RecordSet** a questo cmdlet usando l'operatore pipeline o come parametro.
Per identificare un record in base al nome e al tipo senza usare un oggetto **RecordSet,** è necessario passare l'area come oggetto **DnsZone** a questo cmdlet usando l'operatore della pipeline o come parametro oppure in alternativa è possibile specificare i parametri *ZoneName* e *ResourceGroupName.*
È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.
Quando si specifica il set di record con un oggetto **RecordSet,** il set di record non viene eliminato se è stato modificato nel DNS di Azure dopo il recupero dell'oggetto **RecordSet** locale.
Questo fornisce protezione per le modifiche simultanee.
È possibile eliminare questa operazione usando il parametro *Overwrite,* che elimina il set di record indipendentemente dalle modifiche simultanee.

## ESEMPI

### Esempio 1: Rimuovere un set di record
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

Il primo comando ottiene il set di record specificato e quindi lo archivia nella $RecordSet variabile. Il secondo comando rimuove il set di record in $RecordSet.

### Esempio 2: Rimuovere un set di record ed eliminare tutte le conferme
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

Il primo comando ottiene il set di record specificato.
Il secondo comando elimina il set di record, anche se è stato modificato nel frattempo.
Le richieste di conferma vengono visualizzate.

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

### -Name
Specifica il nome del **recordSet** da rimuovere.
Quando si specifica il set di record in base al nome, è necessario specificare l'area DNS usando il parametro *Zone* o *i parametri ZoneName* e *ResourceGroupName.*
In alternativa, è possibile specificare il set di record usando un **oggetto RecordSet,** passato con il *parametro RecordSet.*

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

### -Overwrite
Quando si specifica il set di record con un oggetto **RecordSet,** il set di record non viene eliminato se è stato modificato nel DNS di Azure dopo il recupero dell'oggetto **RecordSet** locale.
Questo fornisce protezione per le modifiche simultanee.
Questa operazione può essere soppressa con il parametro *Overwrite,* che elimina il set di record indipendentemente dalle modifiche simultanee.

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
passthru

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
Specifica **l'oggetto RecordSet** da rimuovere.
In alternativa, è possibile specificare il set di record usando i parametri *Name* e *Zone* oppure i parametri *Name,* *ZoneName* e *ResourceGroupName.*

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
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- I record TXT SOA vengono eliminati automaticamente quando l'area viene eliminata.
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
Specifica il gruppo di risorse che contiene l'area DNS che contiene il **RecordSet** da eliminare.
Questo parametro è valido solo quando il set di record e l'area DNS vengono specificati usando i *parametri Name* e *ZoneName.*
In alternativa, è possibile specificare il set di record usando il parametro *RecordSet* o i *parametri Name* e *Zone.*

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
Specifica l'area DNS che contiene il **RecordSet** da eliminare.
Questo parametro è applicabile solo quando si specifica il set di record usando il *parametro Name.*
In alternativa, è possibile specificare il set di record usando il parametro *RecordSet* o i parametri *Name,* *ZoneName* e *ResourceGroupName.*

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

### -ZoneName
Specifica il nome dell'area che contiene il **recordSet** da eliminare.
È anche necessario specificare i *parametri Name* *e ResourceGroupName.*
In alternativa, è possibile specificare il set di record usando il parametro *RecordSet* o i *parametri Name* e *Zone.*

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

### Microsoft.Azure.Management.Dns.Models.RecordType

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## OUTPUT

### System.Boolean

## NOTE
È possibile usare il *parametro Confirm* per controllare se il cmdlet richiede conferma.
Per impostazione predefinita, il cmdlet chiede conferma se la variabile $ConfirmPreference Windows PowerShell ha un valore medio o inferiore.
Se si specifica *Conferma* o *Conferma:$True,* questo cmdlet richiede conferma prima dell'esecuzione.
Se si specifica *Conferma:$False,* il cmdlet non richiede conferma.

## COLLEGAMENTI CORRELATI

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
