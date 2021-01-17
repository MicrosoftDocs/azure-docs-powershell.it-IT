---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 007142cb854e2e428983f95d7bb7397c5a0ace39
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373869"
---
# Get-AzAutomationDscOnboardingMetaconfig

## Sinossi
Crea file MOF di meta-configurazione.

## SINTASSI

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzAutomationDscOnboardingMetaconfig** crea i file MOF (Managed state Configuration) APS (DSC).
Questo cmdlet crea un file con estensione MOF per ogni nome di computer specificato.
Il cmdlet crea una cartella per i file con estensione MOF.
Puoi eseguire il cmdlet Set-DscLocalConfigurationManager per questa cartella in modo che questi computer vengano imbarcati in un account di automazione di Azure come nodi DSC.

## ESEMPI

### Esempio 1: server onboard per l'automazione DSC
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

Il primo comando crea file di configurazione di meta DSC per due server per l'account di automazione denominato Contoso17.
Il comando Salva questi file su un desktop.
Il secondo comando usa il cmdlet **set-DscLocalConfigurationManager** per applicare la meta-configurazione ai computer specificati per inserirli come nodi DSC.

## PARAMETRI

### -AutomationAccountName
Specifica il nome di un account di automazione.
È possibile imbarcare i computer che il parametro *nomecomputer* specifica per l'account specificato da questo parametro.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nomecomputer
Specifica una matrice di nomi di computer per cui questo cmdlet genera file con estensione MOF.
Se non specifichi questo parametro, il cmdlet genera un file con estensione MOF per il computer corrente (localhost).

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

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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
Impone l'esecuzione del comando senza richiedere conferma e per sostituire i file MOF esistenti con lo stesso nome.

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

### -CartellaOutput
Specifica il nome di una cartella in cui questo cmdlet archivia i file MOF.

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

### -ResourceGroupName
Specifica il nome di un gruppo di risorse.
Questo cmdlet crea file MOF in computer di bordo nel gruppo di risorse specificato da questo parametro.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

### System. String []

## OUTPUT

### Microsoft. Azure. Commands. Automation. Model. DscOnboardingMetaconfig

## Note

## COLLEGAMENTI CORRELATI
