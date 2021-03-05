---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 85a35fe4c6b988ce6f5320d308582fb722cc5791
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964094"
---
# New-AzVpnClientRevokedCertificate

## SYNOPSIS
Crea un nuovo certificato di revoca client VPN.

## SINTASSI

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzVpnClientRevokedCertificate** crea un nuovo certificato di revoca client di rete privata virtuale (VPN) da usare in un gateway di rete virtuale.
I certificati di revoca client impediscono ai computer client di usare il certificato specificato per l'autenticazione.
Questo cmdlet crea un certificato autonomo non assegnato a un gateway virtuale.
Il certificato creato da **New-AzVpnClientRevokedCertificate** viene invece usato insieme al cmdlet New-AzVirtualNetworkGateway quando crea un nuovo gateway.
Si supponga, ad esempio, di creare un nuovo certificato e di archiviarlo in una variabile denominata $Certificate.
È quindi possibile usare tale oggetto certificato quando si crea un nuovo gateway virtuale.
Ad esempio, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`
Per altre informazioni, vedere la documentazione del cmdlet New-AzVirtualNetworkGateway.

## ESEMPI

### Esempio 1: Creare un nuovo certificato revocato dal client
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Questo comando crea un nuovo certificato revocato dal client e archivia l'oggetto certificato in una variabile denominata $Certificate.
Questa variabile può quindi essere usata dal cmdlet **New-AzVirtualNetworkGateway** per aggiungere il certificato a un nuovo gateway di rete virtuale.

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

### -Name
Specifica un nome univoco per il nuovo certificato di revoca client.

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

### -Thumbprint
Specifica l'identificatore univoco del certificato da aggiungere.
È possibile restituire informazioni sull'impronta digitale per i certificati usando un comando di Windows PowerShell simile al seguente: `Get-ChildItem -Path Cert:\LocalMachine\Root`
Il comando precedente restituisce le informazioni per tutti i certificati del computer locale trovati nell'archivio certificati radice.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate

## NOTE

## COLLEGAMENTI CORRELATI

[Add-AzVpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[Get-AzVpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[Remove-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


