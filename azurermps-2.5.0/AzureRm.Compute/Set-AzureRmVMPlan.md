---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmplan
schema: 2.0.0
ms.openlocfilehash: ce0101140bc353eb52ee8d1af7f2878735da73db
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867136"
---
# Set-AzureRmVMPlan

## Sinossi
Imposta le informazioni sul piano Marketplace in una macchina virtuale.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureRmVMPlan** imposta le informazioni sul piano di Azure Marketplace per una macchina virtuale.

Prima di poter distribuire un'immagine Marketplace tramite la riga di comando, l'accesso a livello di codice deve essere abilitato o la macchina virtuale deve essere distribuita usando il portale di Azure.

## ESEMPI

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

### -Nome
Specifica il nome dell'immagine dal Marketplace.
Si tratta dello stesso valore restituito dal cmdlet Get-AzureRmVMImageSku.
Per altre informazioni su come trovare informazioni sulle immagini, vedere Spostamento e selezione di immagini di macchine virtuali di Azure con PowerShell e la https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) di Azure (nella documentazione di Microsoft Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Prodotto
Specifica il prodotto dell'immagine dal Marketplace.
Queste sono le stesse informazioni del valore **offer** dell'elemento **imageReference** .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PromotionCode
Specifica un codice promozionale.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Publisher
Specifica l'autore dell'immagine.
Queste informazioni possono essere trovate usando il cmdlet Get-AzureRmVMImagePublisher.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Specifica l'oggetto macchina virtuale per cui impostare un piano per Marketplace.
Puoi usare il cmdlet Get-AzureRmVM per ottenere un oggetto macchina virtuale.
Puoi usare il cmdlet New-AzureRmVMConfig per creare un oggetto macchina virtuale.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### PSVirtualMachine
Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline

## OUTPUT

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[Get-AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[New-AzureRmVMConfig](./New-AzureRmVMConfig.md)
