---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193351"
---
# Set-AzPublicIpAddress

## SYNOPSIS
Aggiorna un indirizzo IP pubblico.

## SINTASSI

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il **cmdlet Set-AzPublicIpAddress** aggiorna un indirizzo IP pubblico.

## ESEMPI

### 1: modificare il metodo di assegnazione di un indirizzo IP pubblico
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 Il primo comando ottiene la risorsa indirizzo IP pubblico con nome $publicIPName nel gruppo di $rgName.
Il secondo comando imposta il metodo di allocazione dell'oggetto indirizzo IP pubblico su "Statico".
Set-AzPublicIPAddress aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato e modifica il metodo di assegnazione in "Statico". Un indirizzo IP pubblico viene allocato immediatamente.

### 2: Aggiungere l'etichetta del dominio DNS di un indirizzo IP pubblico
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Il primo comando ottiene la risorsa indirizzo IP pubblico con nome $publicIPName nel gruppo di $rgName.
Il secondo comando imposta la proprietà DomainNameLabel sul prefisso dns obbligatorio.
Set-AzPublicIPAddress comando aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato. DomainNameLabel & fqdn vengono modificati nel modo previsto.
    
### 3: Modificare l'etichetta del dominio DNS di un indirizzo IP pubblico
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Il primo comando ottiene la risorsa indirizzo IP pubblico con nome $publicIPName nel gruppo di $rgName.
Il secondo comando imposta la proprietà DomainNameLabel sul prefisso dns obbligatorio.
Set-AzPublicIPAddress comando aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato. DomainNameLabel & fqdn vengono modificati nel modo previsto.

## PARAMETERS

### -AsJob
Eseguire il cmdlet in background

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

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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

### -PublicIpAddress
Specifica un oggetto indirizzo IP pubblico che rappresenta lo stato su cui deve essere impostato l'indirizzo IP pubblico.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[New-AzPublicIpAddress](./New-AzPublicIpAddress.md)

[Remove-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)


