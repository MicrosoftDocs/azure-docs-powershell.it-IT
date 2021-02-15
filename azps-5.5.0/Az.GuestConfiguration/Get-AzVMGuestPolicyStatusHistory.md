---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204035"
---
# Get-AzVMGuestPolicyStatusHistory

## SYNOPSIS
Recupera la cronologia dello stato di conformità dei criteri di configurazione guest per un'iniziativa di tipo "Configurazione guest" assegnata a una macchina virtuale.
Un'iniziativa è una politica di definizione di tipo "Iniziativa".

## SINTASSI

### InitiativeNameScope (impostazione predefinita)
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il Get-AzVMGuestPolicyStatusHistory cmdlet ottiene la cronologia dello stato di conformità dei criteri di configurazione guest per un'iniziativa di tipo "Configurazione guest" assegnata a una macchina virtuale.
Un'iniziativa è una politica di definizione di tipo "Iniziativa".
Usare Get-AzVMGuestPolicyStatus cmdlet per ottenere dettagli su un singolo stato di conformità usando ReportId, disponibile nell'output del cmdlet Get-AzVMGuestPolicyStatusHistory.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

Recupera la cronologia dello stato di conformità in base all'ID dell'iniziativa. L'opzione ShowOnlyChange mostra solo le modifiche cronologiche apportate allo stato.
Ignora gli stati che non sono stati modificati tra due controlli di conformità.

### Esempio 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

Recupera la cronologia dello stato di conformità in base al nome dell'iniziativa.
L'opzione ShowOnlyChange mostra solo le modifiche cronologiche apportate allo stato.
Ignora gli stati che non sono stati modificati tra due controlli di conformità.

### Esempio 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

Recupera la cronologia dello stato di conformità per tutti i criteri di configurazione guest assegnati alla macchina virtuale.
L'opzione ShowOnlyChange mostra solo le modifiche cronologiche apportate allo stato.
Ignora gli stati che non sono stati modificati tra due controlli di conformità.

### Esempio 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Recupera la cronologia dello stato di conformità in base all'ID iniziativa.

### Esempio 5
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Recupera la cronologia dello stato di conformità in base al nome dell'iniziativa.

### Esempio 6
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
Recupera la cronologia dello stato di conformità per tutti i criteri di configurazione guest assegnati alla macchina virtuale.

### Esempio 7
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

Ottenere lo stato dei criteri di configurazione guest in base a ReportId.
ReportId è la proprietà ReportId che è possibile trovare nei risultati di Get-AzVMGuestPolicyStatusHistory. (fai riferimento ad altri esempi)

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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

### -InitiativeId
ID definizione di un criterio in cui il tipo di definizione è Initiative e la categoria è Guest Configuration

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InitiativeName
Nome di un criterio in cui il tipo di definizione è Iniziativa e la categoria è Configurazione guest

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowOnlyChange
Mostra le modifiche dello stato cronologiche solo per i criteri di configurazione guest.
Ignora gli stati che non sono stati modificati tra due controlli dello stato di conformità.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
Nome della macchina virtuale.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Nessuno
## OUTPUT

### Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus
## NOTE

## COLLEGAMENTI CORRELATI
