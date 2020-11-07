---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/publish-azurermvmdscconfiguration
schema: 2.0.0
ms.openlocfilehash: c9a778638a0ca86198079227cfa0021a96ac138b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866736"
---
# Publish-AzureRmVMDscConfiguration

## Sinossi
Carica uno script DSC in archiviazione BLOB di Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### UploadArchive (impostazione predefinita)
```
Publish-AzureRmVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateArchive
```
Publish-AzureRmVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Publish-AzureRmVMDscConfiguration** carica uno script DSC (Desired state Configuration) in Azure BLOB Storage, che in seguito può essere applicato alle macchine virtuali di Azure usando il cmdlet Set-AzureRmVMDscExtension.

## ESEMPI

### Esempio 1: creare un pacchetto zip per caricarlo in Azure Storage
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1"
```

Questo comando crea un pacchetto zip per lo script specifico e tutti i moduli di risorse dipendenti e lo carica in Azure Storage.

### Esempio 2: creare un pacchetto zip e archiviarlo in un file locale
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

Questo comando crea un pacchetto zip per lo script specifico e tutti i moduli di risorse dipendenti e lo archivia nel file locale denominato .\MyConfiguration.ps1.zip.

### Esempio 3: aggiungere la configurazione all'archivio e quindi caricarla nello spazio di archiviazione
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

Questo comando aggiunge la configurazione denominata Sample.ps1 all'archivio di configurazione per caricare in Azure Storage e ignora i moduli delle risorse dipendenti.

### Esempio 4: aggiungere dati di configurazione e configurazione all'archivio e quindi caricarli in archiviazione
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

Questo comando aggiunge la configurazione denominata Sample.ps1 e i dati di configurazione denominati SampleData.psd1 nell'archivio di configurazione per caricare in Azure Storage.

### Esempio 5: aggiungere configurazione, dati di configurazione e contenuto aggiuntivo all'archivio e quindi caricarlo nello spazio di archiviazione
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

Questo comando aggiunge la configurazione denominata Sample.ps1, i dati di configurazione SampleData.psd1 e il contenuto aggiuntivo all'archivio di configurazione per caricare in Azure Storage.

## PARAMETRI

### -AdditionalPath
Specifica il percorso di un file o di una directory da includere nell'archivio di configurazione.
Viene scaricata nella macchina virtuale insieme alla configurazione.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
Specifica il percorso di un file con estensione psd1 che specifica i dati per la configurazione.
Questa operazione viene aggiunta all'archivio di configurazione e quindi passata alla funzione di configurazione.
Viene sovrascritto dal percorso dei dati di configurazione fornito tramite il cmdlet Set-AzureRmVMDscExtension

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

### -ConfigurationPath
Specifica il percorso di un file che contiene una o più configurazioni.
Il file può essere un file di script di Windows PowerShell (con estensione ps1) o un file di modulo di Windows PowerShell (con estensione psm1).

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ContainerName
Specifica il nome del contenitore di archiviazione di Azure a cui è stata caricata la configurazione.

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -OutputArchivePath
Specifica il percorso di un file con estensione zip locale in cui scrivere l'archivio di configurazione.
Quando questo parametro viene usato, lo script di configurazione non viene caricato nell'archiviazione BLOB di Azure.

```yaml
Type: String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipDependencyDetection
Indica che questo cmdlet esclude le dipendenze delle risorse DSC dall'archivio di configurazione.

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

### -StorageAccountName
Specifica il nome dell'account di archiviazione di Azure usato per caricare lo script di configurazione nel contenitore specificato dal parametro *containerName* .

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
Specifica il suffisso per il punto finale dello spazio di archiviazione.

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.

Il cmdlet non viene eseguito.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Stringa
Il parametro ' ConfigurationPath ' accetta il valore di tipo ' String ' dalla pipeline

## OUTPUT

### System. String

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmVMDscExtension](./Get-AzureRmVMDscExtension.md)

[Remove-AzureRmVMDscExtension](./Remove-AzureRmVMDscExtension.md)

[Set-AzureRmVMDscExtension](./Set-AzureRmVMDscExtension.md)


