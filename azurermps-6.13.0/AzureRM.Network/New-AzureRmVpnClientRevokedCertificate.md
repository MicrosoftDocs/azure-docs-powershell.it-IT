---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 9f20b0540481c40326bc3656e3f65534c22f9b24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513680"
---
# New-AzureRmVpnClientRevokedCertificate

## Sinossi
Crea un nuovo client VPN-certificato di revoca.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
New-AzureRmVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureRmVpnClientRevokedCertificate** crea un nuovo client di rete privata virtuale (VPN)-certificato di revoca per l'uso in un gateway di rete virtuale.
I certificati di revoca client impediscono ai computer client di usare il certificato specificato per l'autenticazione.
Questo cmdlet crea un certificato autonomo che non è assegnato a un gateway virtuale.
Il certificato creato da **New-AzureRmVpnClientRevokedCertificate** viene invece usato insieme al cmdlet New-AzureRmVirtualNetworkGateway quando crea un nuovo gateway.
Supponiamo, ad esempio, di creare un nuovo certificato e archiviarlo in una variabile denominata $Certificate.
Puoi quindi usare l'oggetto certificato quando crei un nuovo gateway virtuale.
Ad esempio, `New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`
Per altre informazioni, vedere la documentazione relativa al cmdlet New-AzureRmVirtualNetworkGateway.

## ESEMPI

### Esempio 1: creare un nuovo certificato revocato dal client
```
PS C:\>$Certificate = New-AzureRmVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Questo comando crea un nuovo certificato revocato dal client e archivia l'oggetto certificato in una variabile denominata $Certificate.
Questa variabile può quindi essere usata dal cmdlet **New-AzureRmVirtualNetworkGateway** per aggiungere il certificato a un nuovo gateway di rete virtuale.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica un nome univoco per il nuovo certificato di revoca del client.

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

### -Identificazione personale
Specifica l'identificatore univoco del certificato aggiunto.
Puoi restituire informazioni sulle identificazioni personali per i certificati usando un comando di Windows PowerShell simile al seguente: `Get-ChildItem -Path Cert:\LocalMachine\Root`
Il comando precedente restituisce informazioni per tutti i certificati del computer locale presenti nell'archivio certificati radice.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureRmVpnClientRevokedCertificate](./Add-AzureRmVpnClientRevokedCertificate.md)

[Get-AzureRmVpnClientRevokedCertificate](./Get-AzureRmVpnClientRevokedCertificate.md)

[Remove-AzureRmVpnClientRevokedCertificate](./Remove-AzureRmVpnClientRevokedCertificate.md)


