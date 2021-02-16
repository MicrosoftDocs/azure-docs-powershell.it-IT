---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: ec91fecd41138238bc4d89fa81d77bae4730c770
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406843"
---
# Get-AzVpnClientPackage

## SYNOPSIS
Recupera informazioni su un pacchetto client VPN.

## SINTASSI

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzVpnClientPackage** ottiene informazioni sui pacchetti del client VPN disponibili da un gateway di rete virtuale.
I pacchetti client contengono dati di configurazione che consentono a un computer client di effettuare una connessione VPN a una rete virtuale di Azure; Per effettuare una connessione VPN, nei computer client deve essere installato il pacchetto di configurazione corretto.
Pacchetti di configurazione diversi sono disponibili in base alla versione di Windows del computer client (ad esempio, Windows 7 o Windows 10) e all'architettura del processore del computer client (AMD64 o x86).
È necessario specificare il tipo di architettura quando si esegue **Get-AzVpnClientPackage.**

## ESEMPI

### Esempio 1: Ottenere informazioni su un pacchetto client VPN con architettura processore
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

Questo comando recupera informazioni sui pacchetti del client VPN AMD64 archiviati nel gateway di rete virtuale denominato ContosoVirtualNetworkGateway.
Per ottenere informazioni sui pacchetti client x86, impostare il valore del parametro *ProcessorArchitecture* su x86.

## PARAMETERS

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

### -ProcessorArchitecture
Specifica il tipo di architettura della CPU per cui è progettato il pacchetto client.
I valori validi sono Amd64 e X86.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse a cui è assegnato il gateway di rete virtuale.
I gruppi di risorse categorizzano gli articoli per semplificare la gestione dell'inventario e l'amministrazione generale di Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Specifica il nome del gateway di rete virtuale in cui sono archiviate le informazioni sul pacchetto del client.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

## OUTPUT

### System.String

## NOTE

## COLLEGAMENTI CORRELATI

[Resize-AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)



