---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023802"
---
# Update-AzureApplicationGateway

## Sinossi
Aggiorna un gateway dell'applicazione.

## SINTASSI

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Update-AzureApplicationGateway** aggiorna un gateway applicazione esistente.

## ESEMPI

### Esempio 1: modificare un gateway dell'applicazione usando il relativo nome
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

Il primo comando Arresta il gateway dell'applicazione denominato ApplicationGateway06.
Per poter modificare la rete virtuale o le subnet, è necessario arrestare un gateway dell'applicazione.

Il secondo comando consente di modificare la subnet virtuale e le subnet per il gateway dell'applicazione denominato ApplicationGateway06.

### Esempio 2: modificare altre proprietà di un gateway applicazione
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

Questo comando modifica il conteggio delle istanze, le dimensioni del gateway e la descrizione per il gateway dell'applicazione denominato ApplicationGateway06.
Questo comando non modifica la rete virtuale o le subnet per il gateway dell'applicazione.
Non è pertanto necessario arrestare il gateway dell'applicazione prima di eseguire questo comando.

### Esempio 3: modificare un gateway dell'applicazione usando la pipeline
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway06 usando il cmdlet **Get-AzureApplicationGateway** .
Il comando lo archivia nella variabile $ApplicationGateway.

Il secondo comando assegna la proprietà **GatewaySize** il valore Medium.

Il comando finale passa la $ApplicationGateway aggiornata al cmdlet corrente.

## PARAMETRI

### -Descrizione
Specifica una descrizione che questo cmdlet assegna al gateway dell'applicazione.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GatewaySize
Specifica le dimensioni assegnate dal cmdlet al gateway dell'applicazione.
I valori validi sono:

- Small
- Medio
- Grande

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceCount
Specifica il numero di istanze assegnate dal cmdlet al gateway dell'applicazione.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Specifica il nome del gateway dell'applicazione che questo cmdlet aggiorna.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet.
Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

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

### -Subnet
Specifica una matrice di subnet in cui questo cmdlet distribuisce il gateway dell'applicazione.

Non è possibile aggiornare le subnet mentre il gateway dell'applicazione è in esecuzione.
Per arrestare il gateway dell'applicazione, usare il cmdlet Stop-AzureApplicationGateway.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VnetName
Specifica la rete virtuale in cui questo cmdlet distribuisce il gateway dell'applicazione.

Non è possibile aggiornare una rete virtuale mentre il gateway dell'applicazione è in esecuzione.
Per arrestare il gateway dell'applicazione, usare **Stop-AzureApplicationGateway**.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

## OUTPUT

### Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureApplicationGateway](./Get-AzureApplicationGateway.md)

[New-AzureApplicationGateway](./New-AzureApplicationGateway.md)

[Remove-AzureApplicationGateway](./Remove-AzureApplicationGateway.md)

[Start-AzureApplicationGateway](./Start-AzureApplicationGateway.md)

[Stop-AzureApplicationGateway](./Stop-AzureApplicationGateway.md)
