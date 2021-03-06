---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
ms.openlocfilehash: 7faa179ae8c8c43d750e4f042f7bc925b772f4e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514535"
---
# Add-AzureRmVhd

## Sinossi
Carica un disco rigido virtuale da una macchina virtuale locale a un BLOB in un account di archiviazione cloud in Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Add-AzureRmVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Add-AzureRmVhd** carica i dischi rigidi virtuali locali, in formato file VHD, in un account di archiviazione BLOB come dischi rigidi virtuali fissi.
Puoi configurare il numero di thread di Uploader che verranno usati o sovrascriveranno un BLOB esistente nell'URI di destinazione specificato.
È anche supportata la possibilità di caricare una versione con patch di un file VHD locale.
Quando è già stato caricato un disco rigido virtuale di base, è possibile caricare dischi differenze che usano l'immagine di base come padre.
Anche l'URI della firma di accesso condiviso (SAS) è supportato.

## ESEMPI

### Esempio 1: aggiungere un file VHD
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

Questo comando aggiunge un file con estensione VHD a un account di archiviazione.

### Esempio 2: aggiungere un file VHD e sovrascrivere la destinazione
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

Questo comando aggiunge un file con estensione VHD a un account di archiviazione.
Il comando sovrascrive un file esistente.

### Esempio 3: aggiungere un file VHD e specificare il numero di thread
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

Questo comando aggiunge un file con estensione VHD a un account di archiviazione.
Il comando specifica il numero di thread da usare per caricare il file.

### Esempio 4: aggiungere un file VHD e specificare l'URI SAS
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

Questo comando aggiunge un file con estensione VHD a un account di archiviazione e specifica l'URI SAS.

## PARAMETRI

### -BaseImageUriToPatch
Specifica l'URI per un BLOB di immagini di base nell'archiviazione BLOB di Azure.
Un SAS può essere specificato come valore per questo parametro.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Destinazione
Specifica l'URI di un BLOB nell'archiviazione BLOB.
Il parametro supporta l'URI SAS, anche se la destinazione degli scenari di correzione non può essere un URI SAS.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LocalFilePath
Specifica il percorso del file con estensione VHD locale.

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberOfUploaderThreads
Specifica il numero di thread di Uploader da usare durante il caricamento del file con estensione vhd.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sovrascrivere
Indica che questo cmdlet sovrascrive un BLOB esistente nell'URI di destinazione specificato, se disponibile.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse della macchina virtuale.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Salva-AzureRmVhd](./Save-AzureRmVhd.md)


