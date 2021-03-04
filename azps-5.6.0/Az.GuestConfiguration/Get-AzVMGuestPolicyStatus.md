---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 3edb92ae8c46ab67e0e22ee808e38dad7101bfdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990204"
---
# Get-AzVMGuestPolicyStatus

## SYNOPSIS
Recupera gli stati dei criteri di configurazione guest (dettagliati) per un'iniziativa di tipo "Configurazione guest" assegnata a una macchina virtuale.
Un'iniziativa è una politica di definizione di tipo "Iniziativa".

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

## DESCRIZIONE
Il cmdlet Get-AzVMGuestPolicyStatus ottiene gli stati dei criteri di configurazione guest per un'iniziativa di tipo "Configurazione guest" assegnata a una macchina virtuale.
Un'iniziativa è una politica di definizione di tipo "Iniziativa".
Questo cmdlet ottiene gli stati di conformità della macchina virtuale e i motivi per cui non è conforme ai singoli criteri nell'iniziativa.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

Ottenere tutti gli stati più recenti dei criteri di configurazione guest per una macchina virtuale.
Lo stato include lo stato di conformità della macchina virtuale per ogni criterio in tutte le iniziative di tipo "Configurazione guest", motivi di conformità, tempo del controllo di conformità, informazioni sulle risorse verificate per conformità.
I risultati includono gli stati più recenti, non includono gli stati cronologici precedenti.

### Esempio 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Ottenere gli stati più recenti dei criteri di configurazione guest in base all'ID iniziativa. Lo stato include lo stato di conformità della macchina virtuale per ogni criterio nell'iniziativa, motivi di conformità, tempo del controllo di conformità, informazioni sulle risorse verificate per conformità.
I risultati non includono gli stati generati in precedenza, ma solo lo stato più recente per ogni criterio dell'iniziativa.

### Esempio 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Ottenere gli stati più recenti dei criteri di configurazione guest in base al nome dell'iniziativa.
Lo stato include lo stato di conformità della macchina virtuale per ogni criterio nell'iniziativa, motivi di conformità, tempo del controllo di conformità, informazioni sulle risorse verificate per conformità.
I risultati non includono gli stati generati in precedenza, ma solo lo stato più recente per ogni criterio dell'iniziativa.

### Esempio 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

Ottenere lo stato dei criteri di configurazione guest in base a ReportId.
ReportId è la proprietà ReportId che è possibile trovare nei risultati dell'Get-AzVMGuestPolicyStatus per initiativeId o Initiative Name (vedere altri esempi)

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

Required: True
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

### -ReportId
ID dello stato dei criteri di configurazione guest.
Un criterio in cui il tipo di definizione è Iniziativa e la categoria è Configurazione guest deve essere assegnato a un ambito per ottenere gli stati.

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
Nome della macchina virtuale.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Nessuno
## OUTPUT

### Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed
## NOTE

## COLLEGAMENTI CORRELATI
