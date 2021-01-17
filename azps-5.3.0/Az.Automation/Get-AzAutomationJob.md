---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 31390ccb19574b6b88c26828bf504dbc8ac5d924
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478707"
---
# Get-AzAutomationJob

## Sinossi
Ottiene i processi di automazione Runbook.

## SINTASSI

### ByAll (impostazione predefinita)
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByJobId
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzAutomationJob** ottiene i processi Runbook in Azure Automation.

## ESEMPI

### Esempio 1: ottenere un processo di Runbook specifico
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

Questo comando ottiene il processo con il GUID specificato.

### Esempio 2: ottenere tutti i processi per un Runbook
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

Questo comando consente di ottenere tutti i processi associati a un Runbook denominato Runbook02.

### Esempio 3: ottenere tutti i processi in uso
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

Questo comando consente di ottenere tutti i processi in uso nell'account di automazione denominato Contoso17.

## PARAMETRI

### -AutomationAccountName
Specifica il nome di un account di automazione per cui questo cmdlet ottiene i processi.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndTime
Specifica l'ora di fine di un processo come oggetto **DateTimeOffset** .
Puoi specificare una stringa che può essere convertita in un valore **DateTimeOffset** valido.
Questo cmdlet ottiene i processi che hanno un'ora di fine in corrispondenza o prima del valore specificato da questo parametro.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Specifica l'ID di un processo ottenuto da questo cmdlet.

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome di un gruppo di risorse in cui il cmdlet ottiene i processi.

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

### -RunbookName
Specifica il nome di un Runbook per cui questo cmdlet ottiene i processi.

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Specifica l'ora di inizio di un processo come oggetto **DateTimeOffset** .
Questo cmdlet ottiene i processi che hanno un'ora di inizio o dopo il valore specificato da questo parametro.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Stato
Specifica lo stato di un processo.
Questo cmdlet ottiene i processi che hanno uno stato corrispondente a questo parametro.
I valori validi sono: 
- L'attivazione
- Completato
- Fallito
- Accodati
- Ripresa
- Esecuzione
- Iniziale
- Ha smesso
- Arresto
- Sospeso
- Sospensione

```yaml
Type: System.String
Parameter Sets: ByAll, ByRunbookName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. Guid

### System. String

## OUTPUT

### Microsoft. Azure. Commands. Automation. Model. job

## Note

## COLLEGAMENTI CORRELATI

[Get-AzAutomationJobOutput](./Get-AzAutomationJobOutput.md)

[Curriculum vitae-AzAutomationJob](./Resume-AzAutomationJob.md)

[Stop-AzAutomationJob](./Stop-AzAutomationJob.md)

[Suspend-AzAutomationJob](./Suspend-AzAutomationJob.md)


