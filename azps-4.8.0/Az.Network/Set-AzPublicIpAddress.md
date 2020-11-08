---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192281"
---
# Set-AzPublicIpAddress

## Sinossi
Aggiorna un indirizzo IP pubblico.

## SINTASSI

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzPublicIpAddress** aggiorna un indirizzo IP pubblico.

## ESEMPI

### 1: cambiare il metodo di assegnazione di un indirizzo IP pubblico
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 Il primo comando ottiene la risorsa indirizzo IP pubblico con il nome $publicIPName nel gruppo risorse $rgName.
Secondo comando imposta il metodo di allocazione dell'oggetto indirizzo IP pubblico su "static".
Set-AzPublicIPAddress comando Aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato e modifica il metodo di allocazione in "static". Viene allocato immediatamente un indirizzo IP pubblico.

### 2: aggiungere l'etichetta di dominio DNS di un indirizzo IP pubblico
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Il primo comando ottiene la risorsa indirizzo IP pubblico con il nome $publicIPName nel gruppo risorse $rgName.
Secondo comando imposta la proprietà DomainNameLabel sul prefisso DNS obbligatorio.
Set-AzPublicIPAddress comando Aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato. DomainNameLabel & FQDN vengono modificati come previsto.
    
### 3: modificare l'etichetta del dominio DNS di un indirizzo IP pubblico
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Il primo comando ottiene la risorsa indirizzo IP pubblico con il nome $publicIPName nel gruppo risorse $rgName.
Secondo comando imposta la proprietà DomainNameLabel sul prefisso DNS obbligatorio.
Set-AzPublicIPAddress comando Aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato. DomainNameLabel & FQDN vengono modificati come previsto.

## PARAMETRI

### -AsJob
Esegui cmdlet in background

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
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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
Specifica un oggetto indirizzo IP pubblico che rappresenta lo stato in cui deve essere impostato l'indirizzo IP pubblico.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress

## Note

## COLLEGAMENTI CORRELATI

[Get-AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[New-AzPublicIpAddress](./New-AzPublicIpAddress.md)

[Remove-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)


