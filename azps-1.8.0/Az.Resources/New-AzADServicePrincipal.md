---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: aa46a09eec134797f1dcacfeb0541769c4569e9e
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251742"
---
# New-AzADServicePrincipal

## SYNOPSIS
Crea una nuova entità servizio Azure Active Directory.

## SINTASSI

### SimpleParameterSet (Impostazione predefinita)
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithoutCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ApplicationWithPasswordPparamParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithPasswordCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyPparamParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithoutCredentialParameterSet
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DisplayNameWithPasswordPparamSet
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithPasswordCredentialParameterSet
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyPparameterSet
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyCredentialParameterSet
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithoutCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordPparameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyPparamParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Crea una nuova entità servizio Azure Active Directory. Se l'utente non ne fornisce uno, il set di parametri predefinito usa i valori predefiniti per i parametri. Per altre informazioni sui valori predefiniti usati, vedere la descrizione dei parametri specificati di seguito.
Questo cmdlet ha la possibilità di assegnare un ruolo all'entità servizio con i parametri e. Se nessuno di questi parametri viene fornito, non verrà assegnato alcun ruolo `Role` `Scope` all'entità servizio. I valori predefiniti per i parametri e sono rispettivamente "Collaboratore" e la sottoscrizione corrente (nota: i valori predefiniti vengono utilizzati solo quando l'utente fornisce un valore per uno dei due parametri, ma non `Role` `Scope` l'altro).
Il cmdlet crea anche un'applicazione in modo implicito e ne imposta le proprietà, se non viene fornito il valore ApplicationId. Per aggiornare i parametri specifici dell'applicazione, usare Set-AzADApplication cmdlet.

> [!WARNING]
> Quando si crea un'entità servizio con il comando **New-AzADServicePrincipal,** l'output include le credenziali che è necessario proteggere. In alternativa, è consigliabile usare le identità [gestite](/azure/active-directory/managed-identities-azure-resources/overview) per evitare l'uso delle credenziali.
>
> Per impostazione predefinita, **New-AzADServicePrincipal** assegna il ruolo [Collaboratore](/azure/role-based-access-control/built-in-roles#contributor) all'entità servizio nell'ambito della sottoscrizione. Per ridurre il rischio di un'entità servizio compromessa, assegnare un ruolo più specifico e restringere l'ambito a una risorsa o a un gruppo di risorse. Per [altre informazioni, vedere La procedura per aggiungere un'assegnazione](/azure/role-based-access-control/role-assignments-steps) di ruolo.

## ESEMPI

### Esempio 1 - Creazione di entità servizio Active Directory semplice

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

Il comando precedente crea un'entità servizio Active Directory usando i valori predefiniti per i parametri non forniti. Poiché non è stato fornito un ID applicazione, è stata creata un'applicazione per l'entità servizio. Poiché non sono stati forniti valori per `Role` o `Scope` , l'entità servizio creata non ha autorizzazioni.

### Esempio 2 - Creazione semplice di un'entità servizio Active Directory con un ruolo specificato e un ambito predefinito

```
PS C:\> New-AzADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

Il comando precedente crea un'entità servizio Active Directory usando i valori predefiniti per i parametri non forniti. Poiché l'ID applicazione non è stato fornito, è stata creata un'applicazione per l'entità servizio. L'entità servizio è stata creata con le autorizzazioni "Lettore" per la sottoscrizione corrente, poiché non è stato fornito alcun valore per il `Scope` parametro.

### Esempio 3 - Creazione semplice di un'entità servizio Active Directory con un ambito e un ruolo predefiniti specificati

```
PS C:\> New-AzADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

Il comando precedente crea un'entità servizio Active Directory usando i valori predefiniti per i parametri non forniti. Poiché l'ID applicazione non è stato fornito, è stata creata un'applicazione per l'entità servizio. L'entità servizio è stata creata con autorizzazioni "Collaboratore" (poiché per il parametro non è stato fornito alcun `Role` valore) sull'ambito del gruppo di risorse fornito.

### Esempio 4 - Creazione semplice di un'entità servizio Active Directory con un ambito e un ruolo specificati

```
PS C:\> New-AzADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

Il comando precedente crea un'entità servizio Active Directory usando i valori predefiniti per i parametri non forniti. Poiché l'ID applicazione non è stato fornito, è stata creata un'applicazione per l'entità servizio. L'entità servizio è stata creata con autorizzazioni "Lettore" sull'ambito del gruppo di risorse fornito.

### Esempio 5 - Creare una nuova entità servizio Active Directory usando l'ID applicazione con l'assegnazione di ruoli

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

Crea una nuova entità servizio Active Directory per l'applicazione con ID applicazione '34a28ad2-dec4-4a41-bc3b-d22ddf900000e'. Poiché non sono stati forniti valori per `Role` o `Scope` , l'entità servizio creata non ha autorizzazioni.

### Esempio 6 - Creare una nuova entità servizio Active Directory tramite piping

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

Ottiene l'applicazione con ID oggetto '3ede3c26-b443-4e0b-9efc-b05e68338dc3' e pipe al cmdlet di New-AzADServicePrincipal per creare una nuova entità servizio Active Directory per l'applicazione.

## PARAMETERS

### -ApplicationId
ID applicazione univoco per un'entità servizio in un tenant.
Una volta creata, questa proprietà non può essere modificata.
Se non si specifica un ID applicazione, ne viene generato uno.

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationObject
Oggetto che rappresenta l'applicazione per cui viene creata l'entità servizio.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertValue
Valore del tipo di credenziali "asimmetrico".
Rappresenta il certificato codificato base 64.

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
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

### -DisplayName
Nome descrittivo dell'entità servizio. Se non viene fornito un nome visualizzato, questo valore predefinito sarà "azure-powershell-MM-dd-yyyy-HH-mm-ss", dove il suffisso è l'ora di creazione dell'applicazione.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndDate
Data di fine effettiva dell'utilizzo delle credenziali.
Il valore predefinito per la data di fine è a un anno dalla data odierna. Per le credenziali di tipo "asimmetrico", questa deve essere impostata su o prima della data in cui il certificato X509 è valido.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyCredential
Raccolta delle credenziali chiave associate all'applicazione.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PasswordCredential
Raccolta delle credenziali password associate all'applicazione.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Role
Ruolo dell'entità servizio nell'ambito. Se viene fornito un valore per, ma per questo non viene fornito alcun valore, per impostazione predefinita viene utilizzato il `Scope` `Role` ruolo `Role` "Collaboratore".

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope
Ambito per cui l'entità servizio ha le autorizzazioni. Se viene fornito un valore per, ma non per , verrà utilizzato per impostazione predefinita `Role` `Scope` la sottoscrizione `Scope` corrente.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipAssignment
Se è impostata, non verrà creata l'assegnazione di ruolo predefinita per l'entità servizio.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartDate
Data di inizio effettivo dell'utilizzo delle credenziali.
Il valore predefinito per la data di inizio è oggi. Per le credenziali di tipo "asimmetrico", questa deve essere impostata su o dopo la data da cui il certificato X509 è valido.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

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
Mostra cosa accadrebbe se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.Guid

### System.String

### Microsoft.Azure.Commands.ActiveDirectory.PSADApplication

### Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]

### Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]

### System.DateTime

## OUTPUT

### Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper

## NOTE
Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, risorsa, gruppo, modello, distribuzione

## COLLEGAMENTI CORRELATI

[Remove-AzADServicePrincipal](./Remove-AzADServicePrincipal.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

[New-AzADApplication](./New-AzADApplication.md)

[Remove-AzADApplication](./Remove-AzADApplication.md)

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

[New-AzADSpCredential](./New-AzADSpCredential.md)

[Remove-AzADSpCredential](./Remove-AzADSpCredential.md)

