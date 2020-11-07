---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: c1a7a9bdf961838d5cf209b5a4c570e0b7874af3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677854"
---
# New-AzNotificationHubsNamespaceAuthorizationRule

## Sinossi
Crea una regola di autorizzazione e assegna la regola a uno spazio dei nomi dell'hub di notifica.

## SINTASSI

### InputFileParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule** crea una regola di autorizzazione della firma di accesso condiviso (SAS) e la assegna a uno spazio dei nomi dell'hub di notifica.
Le regole di autorizzazione gestiscono i diritti degli utenti allo spazio dei nomi e agli hub di notifica contenuti in tale spazio dei nomi.
Questo cmdlet offre due modi per creare una nuova regola di autorizzazione e assegnarla a uno spazio dei nomi.
Puoi creare un'istanza dell'oggetto **SharedAccessAuthorizationRuleAttributes** e quindi configurare l'oggetto con i valori della proprietà che vuoi che la nuova regola possieda.
Questa operazione può essere eseguita usando .NET Framework.
Puoi quindi copiare questi valori di proprietà nella nuova regola usando il parametro *SASRule* .
In alternativa, puoi creare un file JSON (JavaScript Object Notation) che contiene i valori di configurazione rilevanti e quindi applicare tali valori usando il parametro *inputfile* .
Un file JSON è un file di testo che usa una sintassi simile alla seguente: {  
    "Nome": "ContosoAuthorizationRule",  
    "PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",  
    "Diritti": \[  
        "Ascolta",  
        Inviare  
    \]  
} Se usato insieme al cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule** , l'esempio JSON precedente crea una regola di autorizzazione denominata ContosoAuthorizationRule che consente agli utenti di ascoltare e inviare diritti allo spazio dei nomi.
Il *PrimaryKey* usato per l'autenticazione può essere generato in modo casuale tramite il comando di Windows PowerShell seguente: \[ Convert \] :: ToBase64String ((1.. 32 |% { \[ byte/] (Get-Random-Minimum 0-Maximum 255)}))

## ESEMPI

### Esempio 1: creare una regola di autorizzazione e assegnarla a uno spazio dei nomi
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

Questo comando crea una regola di autorizzazione e assegna la regola allo spazio dei nomi ContosoNamespace.
Quando si crea questa regola è necessario specificare lo spazio dei nomi appropriato e il gruppo di risorse a cui è assegnato lo spazio dei nomi.
Tuttavia, non è necessario specificare alcuna informazione sulla regola stessa: le informazioni sulle regole verranno ricavate dal file di input C:\Configuration\NamespaceAuthorizationRules.jsattivato.

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

### -InputFile
Specifica il percorso di un file JSON contenente le informazioni di configurazione per la nuova regola di autorizzazione.

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
Specifica lo spazio dei nomi a cui verranno assegnate le regole di autorizzazione.
Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.
Le nuove regole devono essere assegnate a uno spazio dei nomi esistente.
Il cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule** non può creare un nuovo spazio dei nomi.

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
Devi usare un gruppo di risorse esistente.
Questo cmdlet non può creare un nuovo gruppo di risorse.

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
Specifica l'oggetto **SharedAccessAuthorizationRuleAttributes** che contiene le informazioni di configurazione per le nuove regole.

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

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


