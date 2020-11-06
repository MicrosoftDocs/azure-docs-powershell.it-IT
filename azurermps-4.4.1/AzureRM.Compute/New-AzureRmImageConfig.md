---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
ms.openlocfilehash: a18fe089cba54f6cbf0d70469a17f2d8f797b2e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508711"
---
# New-AzureRmImageConfig

## Sinossi
Crea un oggetto Image configurabile.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureRmImageConfig** crea un oggetto Image configurabile.

## ESEMPI

### Esempio 1
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

Il primo comando crea un oggetto Image e lo archivia nella variabile $imageConfig.

I tre comandi seguenti assegnano percorsi del disco del sistema operativo e due dischi di dati alle variabili $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.
Questo approccio è solo per la leggibilità dei comandi seguenti.

I tre comandi seguenti aggiungono un disco del sistema operativo e due dischi di dati all'immagine archiviata in $imageConfig.
L'URI di ogni disco è archiviato in $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.

Il comando finale crea un'immagine denominata "ImageName01" nel gruppo di risorse "ResourceGroup01".

## PARAMETRI

### -DataDisk
Specifica l'oggetto disco dati.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]
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

### -Posizione
Specifica una posizione.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsDisk
Specifica il disco del sistema operativo.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageOSDisk
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceVirtualMachineId
Specifica l'ID della macchina virtuale di origine.

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

### -Tag
Specifica che le risorse e i gruppi di risorse possono essere contrassegnati con un set di coppie nome/valore.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System. String
System. Collections. Hashtable Microsoft. Azure. Management. Compute. Models. ImageOSDisk Microsoft. Azure. Management. Compute. Models. ImageDataDisk []

## OUTPUT

### Microsoft. Azure. Management. Compute. Models. image

## Note

## COLLEGAMENTI CORRELATI

