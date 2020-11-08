---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029876"
---
# Set-AzureVNetGateway

## Sinossi
Abilita o Disabilita un gateway VPN per una rete virtuale di Azure.

## SINTASSI

### Connect (impostazione predefinita)
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Disconnettere
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureVNetGateway** Abilita o Disabilita un gateway VPN (Virtual Private Network) per una rete virtuale di Azure.
Un gateway di rete virtuale è un endpoint VPN per la connessione a una rete virtuale.
Specificare il parametro *Connect* o *Disconnect* per abilitare o disabilitare la connessione VPN tra un sito di rete locale e una rete virtuale.

## ESEMPI

### Esempio 1: abilitare un gateway di rete virtuale per una rete virtuale
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

Questo comando Abilita il gateway di rete virtuale tra la rete virtuale di Azure denominata ContosoProdNet e il dispositivo VPN per il sito di rete locale denominato ContosoBranchOffice.

### Esempio 2: disabilitare un gateway di rete virtuale per una rete virtuale
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

Questo comando Disabilita il gateway di rete virtuale tra la rete virtuale di Azure denominata ContosoProdNet e il dispositivo VPN per il sito di rete locale denominato ContosoBranchOffice.

## PARAMETRI

### -Connect
Indica che questo cmdlet Abilita la connessione VPN tra una rete virtuale e un sito di rete locale.

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Disconnetti
Indica che questo cmdlet disabilita la connessione VPN tra una rete virtuale e un sito di rete locale.

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalNetworkSiteName
Specifica il nome del sito di rete locale locali per cui questo cmdlet Abilita o Disabilita la connessione VPN.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet. Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
Specifica la rete virtuale per cui questo cmdlet Abilita o Disabilita la connessione VPN.

```yaml
Type: String
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

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureVNetGateway](./Get-AzureVNetGateway.md)

[New-AzureVNetGateway](./New-AzureVNetGateway.md)

[Remove-AzureVNetGateway](./Remove-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[Ridimensionare-AzureVNetGateway](./Resize-AzureVNetGateway.md)


