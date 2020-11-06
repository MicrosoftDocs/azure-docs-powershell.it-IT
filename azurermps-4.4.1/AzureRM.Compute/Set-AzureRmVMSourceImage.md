---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
ms.openlocfilehash: 88b8af8cd16ab4868a10c5ff1aa3759a6d771a6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508608"
---
# Set-AzureRmVMSourceImage

## Sinossi
Specifica l'immagine per una macchina virtuale.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### ImageReferenceSkuParameterSet (impostazione predefinita)
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ImageReferenceIdParameterSet
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureRmVMSourceImage** specifica l'immagine della piattaforma da usare per una macchina virtuale.

## ESEMPI

### Esempio 1: impostare i valori per un'immagine
```
PS C:\> AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

Il primo comando ottiene il set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.

Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.
Il comando assegna un nome e una dimensione alla macchina virtuale.
La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.

Il comando Final imposta i valori per nome editore, offerta, SKU e versione.
I cmdlet Get- **AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** e **Get-AzureRmVMImage** possono individuare queste impostazioni.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Specifica l'ID.

```yaml
Type: System.String
Parameter Sets: ImageReferenceIdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Offerta
Specifica il tipo di offerta VMImage.
Per ottenere un'offerta di immagine, usare il cmdlet Get-AzureRmVMImageOffer.

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublisherName
Specifica il nome di un autore di un VMImage.
Per ottenere un autore, usare il cmdlet Get-AzureRmVMImagePublisher.

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Specifica una SKU di VMImage.
Per ottenere SKU, usare il cmdlet Get-AzureRmVMImageSku.

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Versione
Specifica una versione di VMImage.
Per usare la versione più recente, specificare il valore più recente invece di una determinata versione.

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Specifica l'oggetto macchina virtuale locale da configurare.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
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

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmAvailabilitySet](./Get-AzureRmAvailabilitySet.md)

[Get-AzureRmVMImage](./Get-AzureRmVMImage.md)

[Get-AzureRmVMImageOffer](./Get-AzureRmVMImageOffer.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[Get-AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[New-AzureRmVMConfig](./New-AzureRmVMConfig.md)


