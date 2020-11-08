---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 68df4cd7dc1149b7bb62a148ff7c649ed2418db8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018973"
---
# New-AzVpnSiteLink

## Sinossi
Crea un oggetto VpnSiteLink di Azure.

## SINTASSI

### ByVpnSiteLinkIpAddress
```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByVpnSiteLinkFqdn
```
New-AzVpnSiteLink -Name <String> -Fqdn <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Crea un oggetto VpnSiteLink di Azure.

## ESEMPI

### Esempio 1
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

Il precedente creerà un gruppo di risorse, una WAN virtuale e un VpnSite con 1 VpnSiteLinks in West US nel gruppo di risorse "testRG" in Azure.

## PARAMETRI

### -BGPAsn
BGP ASN per questo VpnSiteLink.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BGPPeeringAddress
Indirizzo di peering BGP per questo VpnSiteLink.

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

### -FQDN
Nome di dominio completo dell'hop successivo.

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddress
L'hop successivo IpAddress.

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinkProviderName
Nome del provider di collegamenti.

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

### -LinkSpeedInMbps
Velocità di collegamento in Mbps.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSVpnSiteLink

## Note

## COLLEGAMENTI CORRELATI

[New-AzVpnSite](./New-AzVpnSite.md)