---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: a97379fb3cf59658c3f0822fc08fa65c0614021d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678203"
---
# New-AzVpnClientIpsecPolicy

## Sinossi
Questo comando consente agli utenti di creare l'oggetto criteri IPSec VPN specificando uno o tutti i valori, ad esempio IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, per impostare il gateway VPN. Questo comando consente di usare l'oggetto output per impostare i criteri IPSec VPN per il gateway New/esistenti.

## SINTASSI

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Questo comando consente agli utenti di creare l'oggetto criteri IPSec VPN specificando uno o tutti i valori, ad esempio IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, per impostare il gateway VPN. Questo comando consente di usare l'oggetto output per impostare i criteri IPSec VPN per il gateway New/esistenti.

## ESEMPI

### Definire l'oggetto criteri IPSec VPN:
```
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

Questo cmdlet viene usato per creare l'oggetto criteri IPSec VPN usando i valori passati di uno o tutti i parametri che l'utente può passare a param: VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (nuova creazione di gateway VPN)/Set-AzVirtualNetworkGateway (aggiornamento del gateway VPN esistente) in ResourceGroup:

### Creare un nuovo gateway di rete virtuale con l'impostazione di criteri IPSec personalizzati VPN:
```
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Questo cmdlet restituisce l'oggetto gateway di rete virtuale dopo la creazione. 

### Impostare i criteri IPSec personalizzati VPN nel gateway di rete virtuale esistente:
```
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Questo cmdlet restituisce un oggetto gateway di rete virtuale dopo l'impostazione dei criteri IPSec personalizzati VPN.

### Ottenere gateway di rete virtuale per verificare se i criteri personalizzati di VPN sono impostati correttamente:
```
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

Questo cmdlet restituisce l'oggetto gateway di rete virtuale.

## PARAMETRI

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

### -DhGroup
I gruppi di vpnclient DH usati nella fase 1 IKE per la SA iniziale

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
Algoritmo di crittografia IKE vpnclient (fase 2 IKE)

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
Algoritmo di integrità IKE di vpnclient (fase 2 IKE)

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
Algoritmo di crittografia IPSec vpnclient (fase 1 IKE)

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
Algoritmo di integrità IPSec di vpnclient (fase 1 IKE)

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
Gruppi PFS vpnclient usati nella fase 2 IKE per New Child SA

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
Associazione di sicurezza IPSec vpnclient (denominata anche modalità rapida o fase 2 SA) dimensione del payload in KB

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
Associazione di sicurezza IPSec vpnclient (chiamata anche modalità rapida o fase 2 SA) durata in secondi

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy

## Note

## COLLEGAMENTI CORRELATI
