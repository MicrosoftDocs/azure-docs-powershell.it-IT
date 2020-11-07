---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 2e2474b784d66c3c3c34bc9ea9abc2b0959ea500
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836099"
---
# Get-AzVMGuestPolicyStatusHistory

## Sinossi
Ottiene la cronologia dello stato di conformità dei criteri di configurazione Guest per un'iniziativa di tipo "Guest Configuration" assegnata a una VM.
Un'iniziativa è un criterio di tipo definizione "iniziativa".

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

## Descrizione
Il cmdlet Get-AzVMGuestPolicyStatusHistory ottiene la cronologia dello stato di conformità dei criteri di configurazione Guest per un'iniziativa di tipo "configurazione Guest" assegnata a una VM.
Un'iniziativa è un criterio di tipo definizione "iniziativa".
USA Get-AzVMGuestPolicyStatus cmdlet per ottenere informazioni dettagliate su un singolo stato di conformità usando ReportId che puoi trovare nell'output del cmdlet Get-AzVMGuestPolicyStatusHistory.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

Ottiene la cronologia dello stato di conformità per iniziativa ID. ShowOnlyChange l'opzione Mostra solo le modifiche dello stato cronologico.
Ignora gli Stati che non sono stati modificati tra due controlli di conformità.

### Esempio 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

Ottiene la cronologia dello stato di conformità per nome dell'iniziativa.
L'opzione ShowOnlyChange Mostra solo le modifiche dello stato cronologico.
Ignora gli Stati che non sono stati modificati tra due controlli di conformità.

### Esempio 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

Ottiene la cronologia dello stato di conformità per tutti i criteri di configurazione guest assegnati alla VM.
L'opzione ShowOnlyChange Mostra solo le modifiche dello stato cronologico.
Ignora gli Stati che non sono stati modificati tra due controlli di conformità.

### Esempio 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Ottiene la cronologia dello stato di conformità per ID iniziativa.

### Esempio 5
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Ottiene la cronologia dello stato di conformità per nome dell'iniziativa.

### Esempio 6
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
Ottiene la cronologia dello stato di conformità per tutti i criteri di configurazione guest assegnati alla VM.

### Esempio 7
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

Ottenere lo stato dei criteri di configurazione Guest in ReportId.
ReportId è la proprietà ReportId che si trova nei risultati di Get-AzVMGuestPolicyStatusHistory. (fare riferimento ad altri esempi)

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

### -InitiativeId
ID definizione di un criterio in cui il tipo di definizione è Initiative e Category è la configurazione Guest

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

### -Initiativename
Nome di un criterio in cui il tipo di definizione è Initiative e Category è la configurazione Guest

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
Mostra le modifiche dello stato cronologico solo per i criteri di configurazione Guest.
Ignora gli Stati che non sono stati modificati tra due esecuzioni di controllo dello stato di conformità.

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
Nome VM.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
## OUTPUT

### Microsoft. Azure. Commands. GuestConfiguration. Models. PolicyStatus
## Note

## COLLEGAMENTI CORRELATI
