---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: AzureRM.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storagesync/invoke-azurermstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 73e0f00fe184a5462141b060717ca64567d4a67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517280"
---
# Invoke-AzureRmStorageSyncCompatibilityCheck

## Sinossi
Controlla i potenziali problemi di compatibilità tra il sistema e la sincronizzazione di file Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### PathBased (impostazione predefinita)
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [-Quiet] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [-Quiet] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Invoke-AzureRmStorageSyncCompatibilityCheck** controlla i potenziali problemi di compatibilità tra il sistema e la sincronizzazione di file di Azure. Assegnato un percorso locale o remoto, esegue un set di convalide nello spazio dei nomi System e file e quindi restituisce i problemi di compatibilità che trova.
Controlli di sistema:
- Controlli dello spazio dei nomi del file di compatibilità OS:
- Caratteri non supportati
- Dimensione massima del file
- Lunghezza massima del percorso
- Lunghezza massima del file
- Dimensioni massime del set di dati
- Profondità massima della directory

## ESEMPI

### Esempio 1
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
```

Questo comando controlla la compatibilità del sistema e anche di file e cartelle in C:\DATA.

### Esempio 2
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Questo comando controlla la compatibilità di file e cartelle in C:\DATA, ma non esegue un controllo di compatibilità del sistema.

### Esempio 3
```powershell
PS C:\> $errors = Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
PS C:\> $errors | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results
```

Questo comando controlla la compatibilità del sistema e anche di file e cartelle in C:\DATA e quindi Esporta i risultati come file CSV in C:\results.

## PARAMETRI

### -Nomecomputer
Il computer in cui si esegue l'archiviazione.

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credenziale
Le credenziali per la condivisione che si sta convalidando.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Percorso UNC della condivisione che si sta convalidando.

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Silenzioso
Elimina la scrittura di report di output in console.

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

### -SkipNamespaceChecks
Imposta questo contrassegno per ignorare le convalide dello spazio dei nomi file e eseguire solo le convalide di sistema.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipSystemChecks
Imposta questo contrassegno per ignorare le convalide di sistema e eseguire solo le convalide dello spazio dei nomi file.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. StorageSync. Evaluation. Models. PSValidationResult

## Note
* Parole chiave: Azure, azurerm, ARM, Resource, Management, StorageSync, filesync

## COLLEGAMENTI CORRELATI
