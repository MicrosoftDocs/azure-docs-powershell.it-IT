---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7766E3D-D8C2-42F1-840A-8EA633E98500
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8a85934deb617b4f0d8e85ee3162222f16dd294
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030869"
---
# Remove-WAPackVMSubnet

## Sinossi
Rimuove gli oggetti subnet della macchina virtuale.

## SINTASSI

```
Remove-WAPackVMSubnet -VMSubnet <VMSubnet> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Descrizione
Questi argomenti sono deprecati e verranno rimossi in futuro.
Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.
Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Il cmdlet **Remove-WAPackVMSubnet** rimuove gli oggetti subnet della macchina virtuale.

## ESEMPI

### Esempio 1: rimuovere una subnet della macchina virtuale
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet01"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet
```

Il primo comando ottiene la subnet della macchina virtuale denominata ContosoVMSubnet01 usando il cmdlet **Get-WAPackVMSubnet** e quindi archivia tale oggetto nella variabile $VMSubnet.

Il secondo comando rimuove la subnet della macchina virtuale archiviata in $VMSubnet.
Il comando richiede la conferma.

### Esempio 2: rimuovere una macchina virtuale senza conferma
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet02"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet -Force
```

Il primo comando ottiene il servizio cloud denominato ContosoVMSubnet02 usando il cmdlet **Get-WAPackVMSubnet** e quindi archivia tale oggetto nella variabile $VMSubnet.

Il secondo comando rimuove la subnet della macchina virtuale archiviata in $VMSubnet.
Questo comando include il parametro *Force* .
Il comando non chiede conferma.

## PARAMETRI

### -Force
Impone l'esecuzione del comando senza richiedere la conferma dell'utente.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.
Per impostazione predefinita, questo cmdlet non genera alcun output.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -VMSubnet
Specifica una subnet della macchina virtuale.
Per ottenere una subnet della macchina virtuale, usare il cmdlet **Get-WAPackVMSubnet** .

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-WAPackVMSubnet](./Get-WAPackVMSubnet.md)

[New-WAPackVMSubnet](./New-WAPackVMSubnet.md)


