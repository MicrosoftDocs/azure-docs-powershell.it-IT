---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: 1ab2d10800648d04c9e8dcb2cf8907d426bd2d48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984743"
---
# Set-AzDnsRecordSet

## SYNOPSIS
Aggiorna un set di record DNS.

## SINTASSI

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Set-AzDnsRecordSet** aggiorna un set di record nel servizio DNS di Azure da un oggetto **RecordSet** locale.
È possibile passare un **oggetto RecordSet** come parametro o usando l'operatore pipeline.
È possibile usare il *parametro Confirm* $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.
Il set di record non viene aggiornato se è stato modificato nel DNS di Azure dopo il recupero **dell'oggetto RecordSet** locale.
Questo fornisce protezione per le modifiche simultanee.
È possibile disattivare questo comportamento usando il *parametro Overwrite,* che aggiorna il set di record indipendentemente dalle modifiche simultanee.

## ESEMPI

### Esempio 1: Aggiornare un set di record
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

Il primo comando usa il cmdlet Get-AzDnsRecordSet per ottenere il set di record specificato e quindi lo archivia nella $RecordSet variabile.
Il secondo e il terzo comando sono operazioni non in linea per aggiungere due record A al set di record.
Il comando finale usa il cmdlet **Set-AzDnsRecordSet** per eseguire il commit dell'aggiornamento.

### Esempio 2: Aggiornare un record SOA
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

Il primo comando usa il cmdlet **Get-AzDnsRecordset** per ottenere il set di record specificato e quindi lo archivia nella $RecordSet variabile.
Il secondo comando aggiorna il record SOA specificato in $RecordSet.
Il comando finale usa il cmdlet **Set-AzDnsRecordSet** per propagare l'aggiornamento in $RecordSet.

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

### -Overwrite
Indica di aggiornare il set di record indipendentemente dalle modifiche simultanee.
Il set di record non verrà aggiornato se è stato modificato nel DNS di Azure dopo il recupero **dell'oggetto RecordSet** locale.
Questo fornisce protezione per le modifiche simultanee.
Per disattivare questo comportamento, è possibile usare il parametro *Overwrite,* che comporta l'aggiornamento del set di record indipendentemente dalle modifiche simultanee.

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
Specifica il **RecordSet da** aggiornare.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Mostra cosa accadrebbe se il cmdlet viene eseguito. Il cmdlet non viene eseguito. Mostra cosa accadrebbe se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

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

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## OUTPUT

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## NOTE
È possibile usare il *parametro Confirm* per controllare se il cmdlet richiede conferma.
Per impostazione predefinita, il cmdlet chiede conferma se la $ConfirmPreference Windows PowerShell ha un valore medio o inferiore.
Se si specifica *Conferma* o *Conferma:$True,* questo cmdlet richiede conferma prima dell'esecuzione.
Se si specifica *Conferma:$False,* il cmdlet non richiede conferma. 

## COLLEGAMENTI CORRELATI

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)
