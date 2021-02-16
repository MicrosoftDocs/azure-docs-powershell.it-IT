---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: 5cb4a57994ad8b15048bfc22dadefbbee031aaf7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179406"
---
# Remove-AzVpnClientRootCertificate

## SYNOPSIS
Rimuove un certificato radice del client VPN esistente.

## SINTASSI

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Remove-AzVpnClientRootCertificate rimuove** il certificato radice specificato da un gateway di rete virtuale.
I certificati radice sono certificati X.509 che identificano l'Autorità di certificazione radice: tutti gli altri certificati usati nel gateway considera attendibili il certificato radice.
Se si rimuove un certificato radice che usa il certificato a scopo di autenticazione, non sarà più possibile connettersi al gateway.
Quando si usa **Remove-AzVpnClientRootCertificate,** è necessario specificare sia il nome del certificato che una rappresentazione testuale dei dati del certificato.
Per altre informazioni sulla rappresentazione testuale di un certificato, vedere la *descrizione del parametro PublicCertData.*

## ESEMPI

### Esempio 1: Rimuovere un certificato radice client da un gateway di rete virtuale
```powershell
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoRootCertificate"
```

Questo esempio rimuove un certificato radice client denominato ContosoRootCertificate dal gateway di rete virtuale ContosoVirtualGateway.
Il primo comando usa il cmdlet **Get-Content** per ottenere una rappresentazione testuale esportata in precedenza del certificato; questa rappresentazione di testo è archiviata in una variabile $Text.
Il secondo comando usa quindi un ciclo for per estrarre tutto il testo in $Text ad eccezione della prima e dell'ultima riga.
Questo testo estratto viene archiviato in una variabile denominata $CertificateText.
Il terzo comando usa le informazioni archiviate nella variabile $CertificateText insieme al cmdlet **Remove-AzVpnClientRootCertificate** per rimuovere il certificato dal gateway.

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

### -PublicCertData
Specifica la rappresentazione testuale del certificato radice da rimuovere.
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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Specifica il nome del gateway di rete virtuale da cui viene rimosso il certificato.

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

### -VpnClientRootCertificateName
Specifica il nome del certificato radice client rimosso dal cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

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

### System.Boolean

## NOTE

## COLLEGAMENTI CORRELATI

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)


