---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191831"
---
# New-AzVpnClientRootCertificate

## SYNOPSIS
Crea un nuovo certificato radice del client VPN.

## SINTASSI

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzVpnClientRootCertificate** crea un nuovo certificato radice VPN da usare in un gateway di rete virtuale.
I certificati radice sono certificati X.509 che identificano l'Autorità di certificazione radice: tutti gli altri certificati usati nel gateway considera attendibili il certificato radice.
Questo cmdlet crea un certificato autonomo non assegnato a un gateway virtuale.
Il certificato creato da **New-AzVpnClientRootCertificate** viene usato in combinazione con il cmdlet New-AzVirtualNetworkGateway durante la creazione di un nuovo gateway.
Si supponga, ad esempio, di creare un nuovo certificato e di archiviarlo in una variabile denominata $Certificate.
È quindi possibile usare tale oggetto certificato durante la creazione di un nuovo gateway virtuale.
Ad esempio, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`
Per altre informazioni, vedere la documentazione del cmdlet New-AzVirtualNetworkGateway.

## ESEMPI

### Esempio 1: Creare un certificato radice client
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

Questo esempio crea un certificato radice client e archivia l'oggetto certificato in una variabile denominata $Certificate.
Questa variabile può quindi essere usata dal cmdlet **New-AzVirtualNetworkGateway** per aggiungere un certificato radice a un nuovo gateway di rete virtuale.
Il primo comando usa il cmdlet **Get-Content** per ottenere una rappresentazione testuale esportata in precedenza del certificato radice; che i dati di testo vengono archiviati in una variabile denominata $Text.
Il secondo comando usa quindi un ciclo for per estrarre tutto il testo ad eccezione della prima e dell'ultima riga, archiviando il testo estratto in una variabile denominata $CertificateText.
Il terzo comando usa il cmdlet **New-AzVpnClientRootCertificate** per creare il certificato, archiviando l'oggetto creato in una variabile denominata $Certificate.

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
Specifica un nome per il nuovo certificato radice client.

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

### -PublicCertData
Specifica una rappresentazione testuale del certificato radice da aggiungere.
Per ottenere la rappresentazione di testo, esportare il certificato in formato CER (con codifica Base64), quindi aprire il file risultante in un editor di testo.
L'output dovrebbe essere simile al seguente (si noti che l'output effettivo conterrà molte più righe di testo rispetto all'esempio abbreviato illustrato di seguito): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData è costituito da tutte le righe tra la prima riga (----- BEGIN CERTIFICATE -----) e l'ultima riga (----- END CERTIFICATE -----) nel file.
È possibile recuperare PublicCertData usando comandi di Windows PowerShell simili ai seguenti: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }

```yaml
Type: System.String
Parameter Sets: (All)
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

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## NOTE

## COLLEGAMENTI CORRELATI

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


