---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201709"
---
# New-AzVpnClientRootCertificate

## Sinossi
Crea un nuovo certificato radice del client VPN.

## SINTASSI

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzVpnClientRootCertificate** crea un nuovo certificato radice VPN da usare in un gateway di rete virtuale.
I certificati radice sono certificati X. 509 che identificano l'autorità di certificazione radice: tutti gli altri certificati usati nel gateway considerano attendibile il certificato radice.
Questo cmdlet crea un certificato autonomo che non è assegnato a un gateway virtuale.
Il certificato creato da **New-AzVpnClientRootCertificate** viene invece usato insieme al cmdlet New-AzVirtualNetworkGateway quando si crea un nuovo gateway.
Supponiamo ad esempio di creare un nuovo certificato e archiviarlo in una variabile denominata $Certificate.
Puoi quindi usare l'oggetto certificato durante la creazione di un nuovo gateway virtuale.
Ad esempio, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`
Per altre informazioni, vedere la documentazione relativa al cmdlet New-AzVirtualNetworkGateway.

## ESEMPI

### Esempio 1: creare un certificato radice client
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

Questo esempio crea un certificato radice client e archivia l'oggetto Certificate in una variabile denominata $Certificate.
Questa variabile può quindi essere usata dal cmdlet **New-AzVirtualNetworkGateway** per aggiungere un certificato radice a un nuovo gateway di rete virtuale.
Il primo comando usa il cmdlet **Get-Content** per ottenere una rappresentazione di testo esportata in precedenza del certificato radice; i dati di testo vengono archiviati in una variabile denominata $Text.
Il secondo comando usa quindi un ciclo for per estrarre tutto il testo ad eccezione della prima riga e dell'ultima riga, archiviando il testo estratto in una variabile denominata $CertificateText.
Il terzo comando usa il cmdlet **New-AzVpnClientRootCertificate** per creare il certificato, archiviando l'oggetto creato in una variabile denominata $certificate.

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

### -Nome
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
Per ottenere la rappresentazione di testo, esportare il certificato in formato CER (usando la codifica Base64), quindi aprire il file risultante in un editor di testo.
Dovrebbe essere visualizzato l'output simile a questo (si noti che l'output effettivo conterrà molte più righe di testo rispetto all'esempio abbreviato illustrato qui):-----iniziare il certificato-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----certificato finale-----PublicCertData è costituito da tutte le linee tra la prima riga (-----iniziare il certificato-----) e l'ultima riga (-----certificato di fine-----) nel file.
Puoi recuperare PublicCertData usando i comandi di Windows PowerShell in modo simile al seguente: $Text = Get-Content-path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate

## Note

## COLLEGAMENTI CORRELATI

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


