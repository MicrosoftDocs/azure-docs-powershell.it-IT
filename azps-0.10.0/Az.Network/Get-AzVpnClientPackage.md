---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: d08f91029940d60440d50be406dbdfe3652934a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860629"
---
# Get-AzVpnClientPackage

## Sinossi
Ottiene informazioni su un pacchetto client VPN.

## SINTASSI

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzVpnClientPackage** ottiene le informazioni sui pacchetti del client VPN disponibili in un gateway di rete virtuale.
I pacchetti client contengono dati di configurazione che consentono a un computer client di creare una connessione VPN a una rete virtuale di Azure; i computer client devono avere installato il pacchetto di configurazione corretto per creare una connessione VPN.
Sono disponibili pacchetti di configurazione diversi basati sulla versione di Windows del computer client, ad esempio Windows 7 o Windows 10, e sull'architettura del processore del computer client (AMD64 o x86).
Devi specificare il tipo di architettura durante l'uso **di Get-AzVpnClientPackage**.

## ESEMPI

### Esempio 1: ottenere informazioni su un pacchetto client VPN per l'architettura del processore
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

Questo comando consente di ottenere informazioni sui pacchetti del client VPN AMD64 archiviati nel gateway di rete virtuale denominato ContosoVirtualNetworkGateway.
Per ottenere informazioni sui pacchetti client x86, imposta il valore del parametro *processorArchitecture* su x86.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProcessorArchitecture
Specifica il tipo di architettura della CPU per cui è progettato il pacchetto client.
I valori validi sono amd64 e x86.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse a cui è assegnato il gateway di rete virtuale.

I gruppi di risorse categorizzano gli elementi per semplificare la gestione delle scorte e l'amministrazione generale di Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Specifica il nome del gateway di rete virtuale in cui sono archiviate le informazioni sul pacchetto client.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Stringa
Il parametro ' ResourceGroupName ' accetta il valore di tipo ' String ' dalla pipeline

### Stringa
Il parametro ' VirtualNetworkGatewayName ' accetta il valore di tipo ' String ' dalla pipeline

## OUTPUT

###  
**Get-AzVpnClientPackage** restituisce le istanze dell'oggetto System. String.

## Note

## COLLEGAMENTI CORRELATI

[Ridimensionare-AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


