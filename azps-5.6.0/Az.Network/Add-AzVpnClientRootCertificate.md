---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: 38a6abb631a77d41e38026edd3bef5abe9c70c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979661"
---
# Add-AzVpnClientRootCertificate

## SYNOPSIS
Aggiunge un certificato radice del client VPN.

## SINTASSI

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Add-AzVpnClientRootCertificate aggiunge** un certificato radice a un gateway di rete virtuale.
I certificati radice sono certificati X.509 che identificano l'Autorità di certificazione radice.
Per impostazione predefinita, tutti i certificati usati nel gateway considera attendibile il certificato radice.
Questo cmdlet assegna un certificato esistente come certificato radice del gateway.
Se non è disponibile un certificato X.509, è possibile generarne uno tramite l'infrastruttura della chiave pubblica o usare un generatore di certificati, ad esempio makecert.exe.
Per aggiungere un certificato radice, è necessario specificare il nome del certificato e fornire una rappresentazione solo testuale del certificato (per altre informazioni, vedere il parametro *PublicCertData).*
Azure consente di assegnare più certificati radice a un gateway.
Più certificati radice vengono spesso distribuiti da organizzazioni che includono utenti di più aziende.

## ESEMPI

### Esempio 1: Aggiungere un certificato radice client a un gateway virtuale
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

Questo esempio aggiunge un certificato radice client a un gateway virtuale denominato ContosoVirtualGateway.
Il primo comando usa il cmdlet **Get-Content** per ottenere una rappresentazione di testo esportata in precedenza del certificato radice e archivia i dati di testo la variabile denominata $Text.
Il secondo comando usa quindi un ciclo for per estrarre tutto il testo ad eccezione della prima e dell'ultima riga.
Il testo estratto viene archiviato in una variabile denominata $CertificateText.
Il terzo comando usa quindi il testo archiviato in $CertificateText con il cmdlet **Add-AzVpnClientRootCertificate** per aggiungere il certificato radice al gateway.

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
Specifica la rappresentazione testuale del certificato radice da aggiungere.
Per ottenere la rappresentazione di testo, esportare il certificato in formato CER (con codifica Base64), quindi aprire il file risultante in un editor di testo.
In questo caso, l'output sarà simile al seguente (si noti che l'output effettivo conterrà molte più righe di testo rispetto all'esempio abbreviato illustrato di seguito): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData è costituito da tutte le righe tra la prima riga (----- BEGIN CERTIFICATE -----) e l'ultima riga (----- END CERTIFICATE -----) del file.
È possibile recuperare questi dati usando Windows PowerShell comandi simili ai seguenti: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`

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
Specifica il nome del gruppo di risorse a cui è assegnato il certificato radice.
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
Specifica il nome del gateway di rete virtuale in cui viene aggiunto il certificato.

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
Specifica il nome del certificato radice client aggiunto da questo cmdlet.

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

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


