---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: 9f5927905e492fd93998e12f97a97a0380755905
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516080"
---
# Set-AzureRmRoleDefinition

## Sinossi
Modifica un ruolo personalizzato in Azure RBAC.
Fornisci la definizione di ruolo modificata sia come file JSON che come PSRoleDefinition.
Prima di tutto, usare il comando Get-AzureRmRoleDefinition per recuperare il ruolo personalizzato che si vuole modificare.
Modificare quindi le proprietà che si desidera modificare.
Infine, salva la definizione del ruolo usando questo comando.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### InputFileParameterSet
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet Set-AzureRmRoleDefinition aggiorna un ruolo personalizzato esistente in Azure Role-Based controllo di accesso.
Fornisci la definizione di ruolo aggiornata come input per il comando come file JSON o un oggetto PSRoleDefinition.
La definizione del ruolo per il ruolo personalizzato aggiornato deve contenere l'ID e tutte le altre proprietà necessarie del ruolo anche se non vengono aggiornate: DisplayName, Description, actions, AssignableScopes.
I notactings sono facoltativi.

Di seguito è riportato un esempio di codice JSON di definizione del ruolo aggiornato per Set-AzureRmRoleDefinition

{"ID": "52a6cc13-ff92-47a8-A39B-2a8205c3087e", "nome": "ruolo aggiornato", "Descrizione": "può monitorare tutte le risorse e avviare e riavviare le macchine virtuali", "azioni": \[ "*/Read", "Microsoft. ClassicCompute/VirtualMachines/restart/Action", "Microsoft. ClassicCompute/VirtualMachines/Start/Action" \] "AssignableScopes": \[ "/subscriptions/4004a9fd-d58e-48DC-aeb2-4a4aec58606f" \] }

## ESEMPI

### --------------------------Aggiornamento tramite PSRoleDefinitionObject--------------------------
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/eb910d4f-edbf-429b-94F6-d76bae7ff401", "/subscriptions/a846d197-5eac-45c7-b885-a6227fe6d388")

          PS C:\> New-AzureRmRoleDefinition -Role $roleDef
```

### --------------------------Creare l'uso di file JSON--------------------------
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## PARAMETRI

### -InputFile
Nome file che contiene una singola definizione di ruolo JSON da aggiornare.
Includi solo le proprietà che devono essere aggiornate in JSON.
La proprietà ID è obbligatoria.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ruolo
Oggetto definizione ruolo da aggiornare

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### PSRoleDefinition
Il parametro "ruolo" accetta il valore di tipo "PSRoleDefinition" dalla pipeline

## OUTPUT

### Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition

## Note
Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment

## COLLEGAMENTI CORRELATI

[Get-AzureRmProviderOperation](./Get-AzureRmProviderOperation.md)

[Get-AzureRmRoleDefinition](./Get-AzureRmRoleDefinition.md)

[New-AzureRmRoleDefinition](./New-AzureRmRoleDefinition.md)

[Remove-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)

