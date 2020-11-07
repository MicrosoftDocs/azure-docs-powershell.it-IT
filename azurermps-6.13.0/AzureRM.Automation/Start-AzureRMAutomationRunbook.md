---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
ms.openlocfilehash: 46544d42cb28f5fca046586696b95286cdd7f3ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686943"
---
# Start-AzureRmAutomationRunbook

## Sinossi
Avvia un processo di Runbook.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### ByAsynchronousReturnJob (impostazione predefinita)
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### BySynchronousReturnJobOutput
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Start-AzureRmAutomationRunbook** avvia un processo di Runbook di automazione di Azure.
Specificare l'ID o il nome di un Runbook.

## ESEMPI

### Esempio 1: avviare un processo di Runbook
```
PS C:\>Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

Questo comando avvia un processo Runbook per la runbook denominata Runbk01 nell'account di automazione di Azure denominato Contoso17.

### Esempio 2: avviare un processo di Runbook e attendere i risultati
```
Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

Questo comando avvia un processo Runbook per la runbook denominata Runbk01 nell'account di automazione di Azure denominato Contoso17.
Questo comando specifica il parametro _wait_ .
Di conseguenza, restituisce i risultati dopo il completamento del processo.
Il cmdlet attende fino a 1000 secondi per i risultati.

## PARAMETRI

### -AutomationAccountName
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

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -MaxWaitSeconds
Specifica il numero di secondi in cui il cmdlet attende che un processo finisca prima di abbandonare il processo.
Il valore predefinito è 10800 o tre ore.

```yaml
Type: System.Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parameters
```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: JobParameters

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
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

### -RunOn
Specifica il gruppo di lavoro ibrido su cui eseguire Runbook.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Wait
Indica che il cmdlet attende che il processo venga completato, sospeso o fallito e quindi restituirà il controllo a Azure PowerShell.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
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

### System. String

## OUTPUT

### Microsoft. Azure. Commands. Automation. Model. job
-Questo cmdlet restituisce un oggetto **processo** , a meno che tu non specifichi il parametro _wait_ .
-Se non specifichi _wait_ , Azure PowerShell restituisce immediatamente un oggetto **processo** .
-Se si specifica _wait_ , Azure PowerShell completa il processo e quindi restituisce il risultato.
-Il risultato non è un oggetto **processo** .

### System. Management. Automation. PSObject

## Note

## COLLEGAMENTI CORRELATI

[Export-AzureRmAutomationRunbook](./Export-AzureRMAutomationRunbook.md)

[Get-AzureRmAutomationRunbook](./Get-AzureRMAutomationRunbook.md)

[Import-AzureRmAutomationRunbook](./Import-AzureRMAutomationRunbook.md)

[New-AzureRmAutomationRunbook](./New-AzureRMAutomationRunbook.md)

[New-AzureRmAutomationRunbook](./New-AzureRMAutomationRunbook.md)

[Publish-AzureRmAutomationRunbook](./Publish-AzureRMAutomationRunbook.md)

[Remove-AzureRmAutomationRunbook](./Remove-AzureRMAutomationRunbook.md)

[Set-AzureRmAutomationRunbook](./Set-AzureRMAutomationRunbook.md)
