---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 1795216cbc18da2d503a1e0056d614337cd12785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398241"
---
# Set-AzVMSqlServerExtension

## SYNOPSIS
Imposta l'estensione SQL Server azure in una macchina virtuale.

## SINTASSI

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Set-AzVMSqlServerExtension** imposta l'estensione del server AzureSQL in una macchina virtuale.

## ESEMPI

### Esempio 1: Configurare le impostazioni automatiche di applicazione delle patch in una macchina virtuale
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

Il primo comando crea un oggetto configurazione usando il cmdlet **New-AzureVMSqlServerAutoPatchingConfig.**
Il comando archivia la configurazione nella $AutoPatchingConfig variabile.

Il secondo comando recupera la macchina virtuale denominata VirtualMachine11 nel servizio denominato Service02 usando il cmdlet Get-AzVM.
Il comando passa l'oggetto al cmdlet corrente usando l'operatore della pipeline.

Il cmdlet corrente configura le impostazioni di applicazione automatica delle patch in $AutoPatchingConfig per la macchina virtuale.
Il comando passa la macchina virtuale al cmdlet Update-AzVM cmdlet.

### Esempio 2: Configurare le impostazioni di backup automatico in una macchina virtuale
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

Il primo comando crea un oggetto configurazione usando il cmdlet **New-AzureVMSqlServerAutoBackupConfig.**
Il comando archivia la configurazione nella $AutoBackupConfig variabile.

Il secondo comando recupera la macchina virtuale denominata VirtualMachine11 nel servizio denominato Service02 e quindi la passa al cmdlet corrente.

Il cmdlet corrente configura le impostazioni di backup automatico in $AutoBackupConfig per la macchina virtuale.
Il comando passa la macchina virtuale al cmdlet Update-AzVM cmdlet.

### Esempio 3: Disabilitare un'estensione SQL Server in una macchina virtuale
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

Questo comando ottiene una macchina virtuale denominata VirtualMachine08 in Service03 e la passa al cmdlet corrente.
Il comando disabilita SQL Server'estensione della macchina virtuale in tale macchina virtuale.

### Esempio 4: Disinstallare un'estensione SQL Server in una macchina virtuale specifica
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

Questo comando ottiene una macchina virtuale denominata VirtualMachine08 in Service03 e la passa al cmdlet corrente.
Il comando disinstalla un'SQL Server di macchina virtuale specifica in tale macchina virtuale.

## PARAMETERS

### -AutoBackupSettings
Specifica le impostazioni di SQL Server di backup automatico.
Per creare un **oggetto AutoBackupSettings,** usare il cmdlet New-AzureVMSqlServerAutoBackupConfig.

```yaml
Type: AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoPatchingSettings
Specifica le impostazioni di SQL Server di distribuzione automatica delle patch.
Per creare un **oggetto AutoPatchingSettings,** usare il cmdlet New-AzureVMSqlServerAutoPatchingConfig AutoPatchingSettings.

```yaml
Type: AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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

### -KeyVaultCredentialSettings
```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Specifica la posizione della macchina virtuale.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifica il nome della SQL Server'estensione.

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

### -ResourceGroupName
Specifica il nome del gruppo di risorse della macchina virtuale.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Specifica la versione dell'estensione SQL Server versione.

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Specifica il nome della macchina virtuale in cui questo cmdlet imposta l SQL Server estensione.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMSqlServerExtension](./Get-AzVMSqlServerExtension.md)

[New-AzureVMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[New-AzureVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Remove-AzVMSqlServerExtension](./Remove-AzVMSqlServerExtension.md)

[Update-AZVM](./Update-AzVM.md)


