---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: b6052172ecca2821b1373d93a8de870969a6b4f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002206"
---
# Invoke-AzStorageSyncCompatibilityCheck

## SYNOPSIS
Verifica la presenza di potenziali problemi di compatibilità tra il sistema e Azure File Sync.

## SINTASSI

### PathBased (impostazione predefinita)
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Invoke-AzStorageSyncCompatibilityCheck** verifica la presenza di potenziali problemi di compatibilità tra il sistema e Azure File Sync. In base a un percorso locale o remoto, esegue una serie di convalide sullo spazio dei nomi di sistema e file e quindi restituisce gli eventuali problemi di compatibilità rilevati.
Controlli di sistema:
- Controlli dello spazio dei nomi del file di compatibilità del sistema operativo:
- Caratteri non supportati
- Dimensioni massime del file
- Lunghezza massima del percorso
- Lunghezza massima dei file
- Dimensione massima del set di dati
- Profondità massima della directory

## ESEMPI

### Esempio 1
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

Questo comando verifica la compatibilità del sistema e anche dei file e delle cartelle in C:\DATA.

### Esempio 2
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Questo comando verifica la compatibilità dei file e delle cartelle in C:\DATA, ma non esegue un controllo della compatibilità del sistema.

### Esempio 3
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

Questo comando verifica la compatibilità del sistema e anche dei file e delle cartelle in C:\DATA e quindi esporta i risultati in un file CSV in C:\results.

## PARAMETERS

### -ComputerName
Computer in cui si sta eseguendo il controllo.

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

### -Credential
Le credenziali della condivisione che si sta convalidando.

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
Percorso UNC della condivisione da convalidare.

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

### -SkipCheckChecks
Impostare questo flag per ignorare le convalide degli spazi dei nomi file ed eseguire solo le convalide di sistema.

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
Impostare questo flag per ignorare le convalide di sistema ed eseguire solo le convalide degli spazi dei nomi file.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult

## NOTE
* Parole chiave: azure, Az, arm, risorsa, gestione, storagesync, filesync

## COLLEGAMENTI CORRELATI
