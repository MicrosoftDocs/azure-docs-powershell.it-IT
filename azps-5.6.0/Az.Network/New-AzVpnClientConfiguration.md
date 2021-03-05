---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: e5dd9da25bfa2c27bd605dc80b04f8e47fb7f95b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964125"
---
# New-AzVpnClientConfiguration

## SYNOPSIS
Questo comando consente agli utenti di creare il pacchetto di profili Vpn in base alle impostazioni VPN preconfigurato nel gateway VPN, oltre ad alcune impostazioni aggiuntive che gli utenti potrebbero dover configurare, ad esempio alcuni certificati radice.

## SINTASSI

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIZIONE
in questo modo gli utenti possono creare il pacchetto di profili Vpn in base alle impostazioni VPN preconfigurte nel gateway VPN, oltre ad alcune impostazioni aggiuntive che gli utenti potrebbero dover configurare, ad esempio alcuni certificati radice.

## ESEMPI

### Esempio 1
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

Questo cmdlet viene usato per creare un file ZIP del profilo client VPN per "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup". Il profilo viene generato per un server di raggio preconfigurato configurato per l'uso del metodo di autenticazione "EAPTLS" con il file di certificato VpnProfileRadiusCert.

## PARAMETERS

### -AuthenticationMethod
Il metodo di autenticazione può assumere valori EAPMSCHAPv2 o EAPTLS. Quando si specifica EAPMSCHAPv2, il cmdlet genera un programma di installazione di configurazione client per l'autenticazione nome utente/password che usa EAP-MSCHAPv2 di autenticazione. Se si specifica EAPTLS, il cmdlet genera un programma di installazione della configurazione client per l'autenticazione del certificato che usa il protocollo EAP-TLS. L'opzione "EapTls" può essere usata sia per l'autenticazione basata su certificato basata su RADIUS che per l'autenticazione della certificazione eseguita da Gateway di rete virtuale caricando la radice attendibile. Il cmdlet rileva automaticamente ciò che è configurato.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientRootCertificateFileList
Elenco dei percorsi dei certificati radice client

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Name
Nome della risorsa.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProcessorArchitecture
ProcessorArchitecture

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RadiusRootCertificateFile
Percorso certificato radice del server di raggio. Questo è un parametro obbligatorio che deve essere specificato quando si usa EAP-TLS con autenticazione RADIUS. Nome percorso completo del file CER contenente il certificato radice RADIUS utilizzato dal client per convalidare il server RADIUS durante l'autenticazione.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

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
Mostra cosa accadrebbe se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

### System.String[]

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSVpnProfile

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzVpnClientConfiguration](./Get-AzVpnClientConfiguration.md)
