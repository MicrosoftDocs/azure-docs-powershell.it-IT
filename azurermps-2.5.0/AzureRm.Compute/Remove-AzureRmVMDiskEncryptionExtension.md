---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiskencryptionextension
schema: 2.0.0
ms.openlocfilehash: 6c580b862ed2c8a420e8f203131ff9d18d187443
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866560"
---
# Remove-AzureRmVMDiskEncryptionExtension

## Sinossi
Rimuove l'estensione di crittografia disco da una macchina virtuale.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Remove-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzureRmVMDiskEncryptionExtension** rimuove l'estensione di crittografia disco da una macchina virtuale.
Se non viene specificato alcun nome di estensione, questo cmdlet rimuove l'estensione con il nome predefinito AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows o AzureDiskEncryptionForLinux per macchine virtuali basate su Linux.
Questo cmdlet non disabilita la crittografia nella macchina virtuale.
Rimuove l'estensione e la configurazione dell'estensione associata dalla macchina virtuale.

## ESEMPI

### Esempio 1: rimuovere l'estensione di crittografia disco da una macchina virtuale.
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

Questo comando rimuove l'estensione con il nome predefinito AzureDiskEncryption per una macchina virtuale che esegue il sistema operativo Windows o AzureDiskEncryptionForLinux per la macchina virtuale basata su Linux denominata MyTestVM.

### Esempio 2: rimuovere un'estensione di crittografia disco specifica da una macchina virtuale.
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

Questo comando rimuove l'estensione di crittografia denominata MyDiskEncryptionExtension dalla macchina virtuale denominata MyTestVM.

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

### -Nome
Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.
Il cmdlet Set-AzureRmVMDiskEncryptionExtension imposta questo nome su AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows e le macchine virtuali AzureDiskEncryptionForLinux per Linux.
Specifica questo parametro solo se il nome predefinito è stato modificato nel cmdlet **set-AzureRmVMDiskEncryptionExtension** o si usa un nome di risorsa diverso in un modello di gestione risorse.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse per la macchina virtuale.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Specifica il nome della macchina virtuale.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
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

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmVMDiskEncryptionStatus](./Get-AzureRmVMDiskEncryptionStatus.md)

[Set-AzureRmVMDiskEncryptionExtension](./Set-AzureRmVMDiskEncryptionExtension.md)


