---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: c1bf608c76c547360d9d7a48f4ba74c1713ee049
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674346"
---
# Get-AzVMGuestPolicyStatus

## Sinossi
Ottiene gli Stati dei criteri di configurazione Guest (dettagliati) per un'iniziativa di tipo "configurazione Guest" assegnata a una VM.
Un'iniziativa è un criterio di tipo definizione "iniziativa".

## SINTASSI

### VmScope (impostazione predefinita)
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeNameScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ReportIdScope
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet Get-AzVMGuestPolicyStatus ottiene gli Stati dei criteri di configurazione Guest per un'iniziativa di tipo "configurazione Guest" assegnata a una VM.
Un'iniziativa è un criterio di tipo definizione "iniziativa".
Questo cmdlet ottiene gli Stati di conformità della VM e i motivi per cui non è conforme ai singoli criteri dell'iniziativa.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

Ottenere tutti gli ultimi stati dei criteri di configurazione Guest per una VM.
Lo stato include lo stato di conformità della VM per ogni criterio in tutte le iniziative di tipo "configurazione Guest", motivi di conformità, ora del controllo di conformità, informazioni sulle risorse controllate per la conformità.
I risultati includono gli ultimi Stati, non includono gli Stati storici precedenti.

### Esempio 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Ottenere gli ultimi stati dei criteri di configurazione Guest per ID iniziativa. Lo stato include lo stato di conformità della VM per ogni criterio nell'iniziativa, i motivi di conformità, l'ora del controllo di conformità, le informazioni sulle risorse controllate per la conformità.
I risultati non includono gli stati precedenti generati, ma include solo lo stato più recente per ogni criterio nell'iniziativa.

### Esempio 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Ottenere gli ultimi stati dei criteri di configurazione Guest per nome iniziativa.
Lo stato include lo stato di conformità della VM per ogni criterio nell'iniziativa, i motivi di conformità, l'ora del controllo di conformità, le informazioni sulle risorse controllate per la conformità.
I risultati non includono gli stati precedenti generati, ma include solo lo stato più recente per ogni criterio nell'iniziativa.

### Esempio 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

Ottenere lo stato dei criteri di configurazione Guest in ReportId.
ReportId è la proprietà ReportId che si trova nei risultati di Get-AzVMGuestPolicyStatus in base a initiativeId o nome dell'iniziativa (vedere altri esempi)

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

Required: True
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

### -ReportId
ID di uno stato dei criteri di configurazione Guest.
Un criterio in cui il tipo di definizione è iniziativa e la categoria è la configurazione Guest deve essere assegnata a un ambito per ottenere gli Stati.

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
Nome VM.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
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

### Microsoft. Azure. Commands. GuestConfiguration. Models. PolicyStatusDetailed
## Note

## COLLEGAMENTI CORRELATI
