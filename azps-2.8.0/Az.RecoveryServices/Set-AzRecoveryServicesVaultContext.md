---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 6a611017b2effa4733b75f56e6799f6857dcdfa8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856617"
---
# Set-AzRecoveryServicesVaultContext

## Sinossi

Imposta il contesto del Vault.

## SINTASSI

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione

Il cmdlet **set-AzRecoveryServicesVaultContext** imposta il contesto del Vault per i servizi di ripristino del sito Azure.

Avviso: questo cmdlet è deprecato in una versione futura per le modifiche alle interruzioni. Non saranno disponibili sostituzioni. Usare il parametro-VaultId in tutti i comandi per i servizi di recupero in corso.

## ESEMPI

### Esempio 1

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

Imposta il contesto del Vault.

## PARAMETRI

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

### -Vault

Specifica il nome del Vault.
Il Vault deve essere un oggetto **AzureRmRecoveryServicesVault** .

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CommonParameters

Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. Commands. RecoveryServices. ARSVault

## OUTPUT

### System. void

## Note

## COLLEGAMENTI CORRELATI
