---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 7556a2d23d4c4969c3037d6b49dbd482bcdea207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964110"
---
# New-AzVpnClientIpsecPolicy

## SYNOPSIS
Questo comando consente agli utenti di creare l'oggetto criterio Vpn ipsec specificando uno o tutti i valori come IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup da impostare nel gateway VPN. Questo comando consente di usare l'oggetto di output per impostare il criterio ipsec vpn per un gateway nuovo o esistente.

## SINTASSI

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Questo comando consente agli utenti di creare l'oggetto criterio Vpn ipsec specificando uno o tutti i valori come IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup da impostare nel gateway VPN. Questo comando consente di usare l'oggetto di output per impostare il criterio ipsec vpn per un gateway nuovo o esistente.

## ESEMPI

### Esempio 1: Definire l'oggetto criterio IPSec vpn:
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

Questo cmdlet viene usato per creare l'oggetto criterio ipsec vpn usando i valori passati per uno o tutti i parametri che l'utente può passare al param:VpnClientIpsecPolicy del comando PS let: New-AzVirtualNetworkGateway (creazione nuovo gateway VPN) / Set-AzVirtualNetworkGateway (aggiornamento del Gateway VPN esistente) in ResourceGroup:

### Esempio 2: Creare un nuovo gateway di rete virtuale con l'impostazione del criterio ipsec personalizzato vpn:
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Questo cmdlet restituisce l'oggetto gateway di rete virtuale dopo la creazione. 

### Esempio 3: Impostare i criteri IPSec personalizzati della vpn in un gateway di rete virtuale esistente:
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Questo cmdlet restituisce l'oggetto gateway di rete virtuale dopo l'impostazione del criterio ipsec personalizzato vpn.

### Esempio 4: Ottenere il gateway di rete virtuale per verificare se il criterio personalizzato vpn è impostato correttamente:
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

Questo cmdlet restituisce l'oggetto gateway di rete virtuale.

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

### -DhGroup
Gruppi VpnClient DH usati nella fase 1 di IKE per l'accesso condiviso iniziale

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IkeEncryption
Algoritmo di crittografia IKE per VpnClient (Fase IKE 2)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IkeIntegrity
Algoritmo di integrità IKE per VpnClient (Fase IKE 2)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpsecEncryption
Algoritmo di crittografia IPSec VpnClient (Fase IKE 1)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpsecIntegrity
Algoritmo di integrità IPSec di VpnClient (Fase IKE 1)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PfsGroup
Gruppi PFS VpnClient usati nella fase 2 di IKE per la nuova sa figlio

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SADataSize
Dimensioni del payload della modalità rapida o sa della fase 2 in KB dell'associazione di sicurezza IPSec vpnclient

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SALifeTime
Durata in secondi dell'associazione di sicurezza IPSec VpnClient (chiamata anche modalità rapida o SA di fase 2)

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy

## NOTE

## COLLEGAMENTI CORRELATI
