---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 5fb832a7a72f0b201ea20660a5e94e67d470ba95
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677836"
---
# Set-AzNotificationHubsNamespaceAuthorizationRule

## Sinossi
Imposta le regole di autorizzazione per uno spazio dei nomi Hub di notifica.

## SINTASSI

### InputFileParameterSet
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SASRuleParameterSet
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzNotificationHubsNamespaceAuthorizationRule** modifica una regola di autorizzazione della firma di accesso condiviso (SAS) assegnata a uno spazio dei nomi dell'hub di notifica.
Le regole di autorizzazione gestiscono i diritti degli utenti allo spazio dei nomi e agli hub di notifica contenuti nello spazio dei nomi.
Questo cmdlet offre due modi per modificare una regola di autorizzazione assegnata a uno spazio dei nomi.
Per uno, puoi creare un'istanza dell'oggetto **SharedAccessAuthorizationRuleAttributes** e quindi configurare l'oggetto con i valori della proprietà che vuoi che la regola possieda.
Puoi usare .NET Framework per eseguire questa operazione.
Puoi quindi copiare questi valori della proprietà nella regola tramite il parametro *SASRule* .
In alternativa, puoi creare un file JSON (JavaScript Object Notation) contenente i valori di configurazione rilevanti e quindi applicare tali valori tramite il parametro *inputfile* .
Un file JSON è un file di testo che usa una sintassi simile alla seguente: {  
    "Nome": "ContosoAuthorizationRule",  
    "PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",  
    "Diritti": \[  
        "Ascolta",  
        Inviare  
    \]  
} Se usato insieme al cmdlet **set-AzNotificationHubsNamespaceAuthorizationRule** , l'esempio JSON precedente modifica una regola di autorizzazione denominata ContosoAuthorizationRule per consentire agli utenti di ascoltare e inviare diritti allo spazio dei nomi.

## ESEMPI

### Esempio 1: modificare una regola di autorizzazione assegnata a uno spazio dei nomi
```
PS C:\>Set-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

Questo comando consente di modificare una regola di autorizzazione assegnata allo spazio dei nomi denominato ContosoNamespace.
Devi specificare il gruppo di risorse a cui è assegnato lo spazio dei nomi.
Le informazioni sulla regola di autorizzazione non sono incluse nel comando stesso.
Queste informazioni vengono invece ottenute dal file di input C:\Configuration\AuthorizationRules.jsattivato.

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

### -Force
Non chiedere conferma.

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

### -InputFile
Specifica il percorso di un file JSON contenente le informazioni di configurazione per la nuova regola.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Spazio dei nomi
Specifica lo spazio dei nomi che contiene le regole di autorizzazione modificate da questo cmdlet.
Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.

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

### -ResourceGroup
Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.
I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.

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

### -SASRule
Specifica l'oggetto **SharedAccessAuthorizationRuleAttributes** che contiene le informazioni di configurazione per le regole di autorizzazione modificate dal cmdlet.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes

## Note

## COLLEGAMENTI CORRELATI

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubsNamespaceAuthorizationRule](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[Remove-AzNotificationHubsNamespaceAuthorizationRule](./Remove-AzNotificationHubsNamespaceAuthorizationRule.md)


