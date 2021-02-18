---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 720b81b858799e2930ed3d2cdd45e25220697e6a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202408"
---
# Start-AzVpnConnectionPacketCapture

## SYNOPSIS
Avvia l'operazione di acquisizione pacchetti in una connessione Vpn.

## SINTASSI

### ByVpnConnectionName (Impostazione predefinita)
```
Start-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-FilterData <String>] -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByVpnConnectionObject
```
Start-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-FilterData <String>]
 -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByVpnConnectionResourceId
```
Start-AzVpnConnectionPacketCapture -ResourceId <String> [-FilterData <String>] -LinkConnectionName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Avvia l'operazione di acquisizione pacchetti in una connessione Vpn.

## ESEMPI

### Esempio 1
```powershell
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1"
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```

### Esempio 2
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1" -FilterData $a 
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```

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

### -FilterData
Opzioni di filtro per avviare l'acquisizione di pacchetti nella connessione Vpn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Oggetto connessione Vpn in cui iniziare l'acquisizione dei pacchetti.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LinkConnectionName
Nomi di SiteLinkConnection.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Nome della connessione Vpn in cui iniziare l'acquisizione dei pacchetti.

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentResourceName
Nome della vpngateway padre.

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID della risorsa Azure di VpnConnection da cui iniziare l'acquisizione dei pacchetti.

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.Network.Models.PSVpnConnection

### System.String

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult

## NOTE

## COLLEGAMENTI CORRELATI

[Stop-AzVpnConnectionPacketCapture](./Stop-AzVpnConnectionPacketCapture.md)