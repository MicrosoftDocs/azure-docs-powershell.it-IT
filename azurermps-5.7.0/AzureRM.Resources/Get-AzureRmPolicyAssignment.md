---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 0604c7bd8f4f016f908eb7e9c93ff6b9d95db979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687014"
---
# Get-AzureRmPolicyAssignment

## Sinossi
Ottiene le assegnazioni dei criteri.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### GetAllPolicyAssignments (impostazione predefinita)
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### GetPolicyAssignmentName
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### GetPolicyAssignmentId
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmPolicyAssignment** ottiene tutte le assegnazioni dei criteri o le assegnazioni particolari.
Identificare un'assegnazione di criteri per ottenere il nome e l'ambito o l'ID.

## ESEMPI

### Esempio 1: ottenere tutte le assegnazioni dei criteri
```
PS C:\>Get-AzureRmPolicyAssignment
```

Questo comando ottiene tutte le assegnazioni dei criteri.

### Esempio 2: ottenere una specifica assegnazione di criteri
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzureRMResourceGroup.
Il comando Archivia l'oggetto nella variabile $ResourceGroup.

Il secondo comando consente di ottenere l'assegnazione di criteri denominata PolicyAssignment07 per l'ambito che identifica la proprietà **resourceId** di $ResourceGroup.

## PARAMETRI

### -ApiVersion
Specifica la versione dell'API del provider di risorse da usare.
Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -ID
Specifica l'ID di risorsa completo per l'assegnazione di criteri ottenuta da questo cmdlet.

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
Specifica il modo in cui questo cmdlet risponde a un evento informativo.

I valori accettabili per questo parametro sono i seguenti:

- Continuare
- Ignora
- Informarsi
- SilentlyContinue
- Stop
- Sospensione

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifica una variabile di informazioni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome dell'assegnazione di criteri ottenuta da questo cmdlet.

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinitionId
Specifica l'ID della definizione di criteri delle assegnazioni dei criteri ottenute da questo cmdlet.

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName, GetPolicyAssignmentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.

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

### -Ambito
Specifica l'ambito in cui viene applicato il criterio per l'assegnazione ottenuta da questo cmdlet.

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### System. Management. Automation. PSObject

## Note

## COLLEGAMENTI CORRELATI

[New-AzureRmPolicyAssignment](./New-AzureRmPolicyAssignment.md)

[Remove-AzureRmPolicyAssignment](./Remove-AzureRmPolicyAssignment.md)

[Set-AzureRmPolicyAssignment](./Set-AzureRmPolicyAssignment.md)


