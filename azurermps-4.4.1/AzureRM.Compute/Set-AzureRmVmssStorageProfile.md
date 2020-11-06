---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: 60d525cc50b62350853755ae46698cbecb358654
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508584"
---
# Set-AzureRmVmssStorageProfile

## Sinossi
Imposta le proprietà del profilo di archiviazione per VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-ManagedDisk <StorageAccountTypes>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureRmVmssStorageProfile** imposta le proprietà del profilo di archiviazione per il set di scale della macchina virtuale (VMSS).

## ESEMPI

### Esempio 1: impostare le proprietà del profilo di archiviazione per VMSS
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

Questo comando imposta le proprietà del profilo di archiviazione per il VMSS denominato ContosoVMSS.

## PARAMETRI

### -DataDisk
Specifica l'oggetto disco dati.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Immagine
Specifica l'URI BLOB per l'immagine utente.
VMSS crea un disco del sistema operativo nello stesso contenitore dell'immagine utente.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageReferenceId
Specifica l'ID riferimento immagine.

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

### -ImageReferenceOffer
Specifica il tipo di offerta VMImage (Virtual Machine Image).
Per ottenere un'offerta di immagine, usare il cmdlet Get-AzureRmVMImageOffer.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageReferencePublisher
Specifica il nome di un autore di un VMImage.
Per ottenere un autore, usare il cmdlet Get-AzureRmVMImagePublisher.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageReferenceSku
Specifica la SKU VMImage.
Per ottenere SKU, usare il cmdlet Get-AzureRmVMImageSku.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageReferenceVersion
Specifica la versione di VMImage.
Per usare la versione più recente, specificare il valore più recente invece di una determinata versione.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDisk
Specifica il disco gestito.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsDiskCaching
Specifica la modalità di memorizzazione nella cache del disco del sistema operativo. I valori accettabili per questo parametro sono i seguenti:

- ReadOnly
- ReadWrite

Il valore predefinito è ReadWrite.
Se si modifica il valore di memorizzazione nella cache, il cmdlet riavvia la macchina virtuale.

Questa impostazione influenza la coerenza e le prestazioni del disco.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsDiskCreateOption
Specifica il modo in cui questo cmdlet crea le macchine virtuali VMSS.

I valori accettabili per questo parametro sono i seguenti:

- Allega: questo valore viene usato quando si usa un disco specializzato per creare la macchina virtuale VMSS. 
- FromImage: questo valore viene usato quando si usa un'immagine per creare la macchina virtuale VMSS.
Se si usa un'immagine della piattaforma, si userà anche il parametro *imageReference* .

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsDiskName
Specifica il nome del disco del sistema operativo.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsDiskOsType
Specifica il tipo di sistema operativo sul disco.
Questa operazione è necessaria solo per scenari di immagini utente e non per un'immagine della piattaforma.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VhdContainer
Specifica gli URL del contenitore usati per archiviare i dischi del sistema operativo per VMSS.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Specifica l'oggetto VMSS.
Per ottenere l'oggetto, usa l'oggetto New-AzureRmVmssConfig.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

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
Mostra cosa succede se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

###  
Questo cmdlet non genera alcun output.

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmVMImageOffer](./Get-AzureRmVMImageOffer.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[Get-AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md)


