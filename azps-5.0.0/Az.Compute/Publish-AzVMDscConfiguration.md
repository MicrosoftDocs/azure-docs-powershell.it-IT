---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: 94dac11a3c26adaac93b4e36c2dda3df513d4076
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302088"
---
# Publish-AzVMDscConfiguration

## Sinossi
Carica uno script DSC in archiviazione BLOB di Azure.

## SINTASSI

### UploadArchive (impostazione predefinita)
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateArchive
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Publish-AzVMDscConfiguration** carica uno script DSC (Desired state Configuration) in Azure BLOB Storage, che in seguito può essere applicato alle macchine virtuali di Azure usando il cmdlet Set-AzVMDscExtension.

## ESEMPI

### Esempio 1: creare un pacchetto zip per caricarlo in Azure Storage
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

Questo comando crea un pacchetto zip per lo script specifico e tutti i moduli di risorse dipendenti e lo carica in Azure Storage.

### Esempio 2: creare un pacchetto zip e archiviarlo in un file locale
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

Questo comando crea un pacchetto zip per lo script specifico e tutti i moduli di risorse dipendenti e lo archivia nel file locale denominato .\MyConfiguration.ps1.zip.

### Esempio 3: aggiungere la configurazione all'archivio e quindi caricarla nello spazio di archiviazione
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

Questo comando aggiunge la configurazione denominata Sample.ps1 all'archivio di configurazione per caricare in Azure Storage e ignora i moduli delle risorse dipendenti.

### Esempio 4: aggiungere dati di configurazione e configurazione all'archivio e quindi caricarli in archiviazione
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

Questo comando aggiunge la configurazione denominata Sample.ps1 e i dati di configurazione denominati SampleData.psd1 nell'archivio di configurazione per caricare in Azure Storage.

### Esempio 5: aggiungere configurazione, dati di configurazione e contenuto aggiuntivo all'archivio e quindi caricarlo nello spazio di archiviazione
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

Questo comando aggiunge la configurazione denominata Sample.ps1, i dati di configurazione SampleData.psd1 e il contenuto aggiuntivo all'archivio di configurazione per caricare in Azure Storage.

## PARAMETRI

### -AdditionalPath
Specifica il percorso di un file o di una directory da includere nell'archivio di configurazione.
Viene scaricata nella macchina virtuale insieme alla configurazione.

```yaml
Type: System.String[]
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
Viene sovrascritto dal percorso dei dati di configurazione fornito tramite il cmdlet Set-AzVMDscExtension

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

### -ConfigurationPath
Specifica il percorso di un file che contiene una o più configurazioni.
Il file può essere un file di script di Windows PowerShell (con estensione ps1) o un file di modulo di Windows PowerShell (con estensione psm1).

```yaml
Type: System.String
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
Type: System.String
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Impone l'esecuzione del comando senza richiedere la conferma dell'utente.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.String
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
Type: System.String
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.String
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
Type: System.String
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

### System. String []

## OUTPUT

### System. String

## Note

## COLLEGAMENTI CORRELATI

[Get-AzVMDscExtension](./Get-AzVMDscExtension.md)

[Remove-AzVMDscExtension](./Remove-AzVMDscExtension.md)

[Set-AzVMDscExtension](./Set-AzVMDscExtension.md)


