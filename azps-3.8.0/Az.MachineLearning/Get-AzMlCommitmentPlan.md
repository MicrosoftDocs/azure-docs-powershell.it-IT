---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 2eeaf4d4c1f0a2cf97359610d34963e32b50d1c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022204"
---
# Get-AzMlCommitmentPlan

## Sinossi
Recupera le informazioni di riepilogo per uno o più piani di impegno.

## SINTASSI

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Recupera le informazioni sul piano di impegno.
A seconda dei parametri passati, il cmdlet restituisce il piano di impegno specifico, una raccolta di piani di impegno per un gruppo di risorse specificato nell'abbonamento corrente o una raccolta di piani di impegno nell'ambito dell'abbonamento corrente.

## ESEMPI

### Esempio 1: ottenere un piano di impegno specifico
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### Esempio 2: ottenere tutte le risorse del piano di impegno nell'abbonamento corrente
```
Get-AzMlCommitmentPlan
```

### Esempio 3: ottenere tutti i piani di impegno nell'abbonamento corrente e nel gruppo di risorse specifico
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## PARAMETRI

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

### -Nome
Nome del piano di impegno.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse per il piano di impegni di Azure ML.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan

## Note
Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml

## COLLEGAMENTI CORRELATI
