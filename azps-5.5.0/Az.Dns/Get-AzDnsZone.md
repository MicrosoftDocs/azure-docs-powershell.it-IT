---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204155"
---
# Get-AzDnsZone

## SYNOPSIS
Ottiene un'area DNS.

## SINTASSI

### Predefinito (impostazione predefinita)
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroup
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzDnsZone** ottiene un'area DNS (Domain Name System) dal gruppo di risorse specificato.
Se si specifica il *parametro Name,* viene restituito **un singolo oggetto DnsZone.**
Se non si specifica il *parametro Name,* verrà restituita una matrice contenente tutte le aree del gruppo di risorse specificato.
È possibile usare **l'oggetto DnsZone** per aggiornare l'area, ad esempio è possibile aggiungervi oggetti **RecordSet.**

## ESEMPI

### Esempio 1: Ottenere un'area
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

Questo esempio recupera l'area DNS myzone.com denominata dns dal gruppo di risorse specificato e quindi la archivia nella $Zone variabile.

### Esempio 2: Recuperare tutte le aree in un gruppo di risorse
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

Questo esempio recupera tutte le zone DNS del gruppo di risorse specificato e quindi le archivia nella $Zones variabile.

### Esempio 3: Ottenere tutte le aree in un abbonamento
```
PS C:\> $Zones = Get-AzDnsZone
```

Questo esempio recupera tutte le aree DNS nella sottoscrizione di Azure corrente e quindi le archivia nella variabile $Zones dominio.

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
Specifica il nome dell'area DNS da ottenere.
Se non si specifica un valore per il parametro *Name,* questo cmdlet ottiene tutte le zone DNS del gruppo di risorse specificato.
Se si omette anche il *parametro ResourceGroupName,* questo cmdlet ottiene tutte le zone DNS nella sottoscrizione di Azure corrente.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse che contiene l'area DNS da ottenere.
Se non si specifica *ResourceGroupName,* è necessario omettere anche il *parametro Name.*
In questo caso, questo cmdlet ottiene tutte le aree DNS nella sottoscrizione di Azure corrente.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
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

## OUTPUT

### Microsoft.Azure.Commands.Dns.DnsZone

## NOTE

## COLLEGAMENTI CORRELATI

[New-AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
