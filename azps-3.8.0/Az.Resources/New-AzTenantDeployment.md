---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
ms.openlocfilehash: 38f46b8805b8e259b086e5c5a78e929112dca83a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864621"
---
# New-AzTenantDeployment

## Sinossi
Creare una distribuzione in ambito tenant

## SINTASSI

### ByTemplateFileWithNoParameters (impostazione predefinita)
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateObjectAndParameterObject
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByTemplateFileAndParameterObject
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByTemplateUriAndParameterObject
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByTemplateObjectAndParameterFile
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByTemplateFileAndParameterFile
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateUriAndParameterFile
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateObjectAndParameterUri
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByTemplateFileAndParameterUri
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateUriAndParameterUri
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateObjectWithNoParameters
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateUriWithNoParameters
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzTenantDeployment** aggiunge una distribuzione nell'ambito del tenant corrente.

Per aggiungere una distribuzione in ambito tenant, specificare la posizione e un modello.
La posizione indica a Azure Resource Manager dove archiviare i dati di distribuzione. Il modello è una stringa JSON che contiene singole risorse da distribuire.
Il modello include i segnaposto dei parametri per le risorse necessarie e i valori delle proprietà configurabili, ad esempio nomi e dimensioni.

Per usare un modello personalizzato per la distribuzione, specifica il parametro *TemplateFile* o il parametro *TemplateUri* .
Ogni modello include parametri per le proprietà configurabili.
Per specificare i valori per i parametri del modello, specifica il parametro *TemplateParameterFile* o il parametro *TemplateParameterObject* .
In alternativa, è possibile usare i parametri del modello che vengono aggiunti dinamicamente al comando quando si specifica un modello.
Per usare i parametri dinamici, digitarli al prompt dei comandi oppure digitare un segno meno (-) per indicare un parametro e usare il tasto TAB per spostarsi tra i parametri disponibili.
I valori dei parametri del modello immessi al prompt dei comandi hanno la precedenza sui valori in un oggetto o un file di parametro di modello.

Per aggiungere risorse a un gruppo di risorse, usare il **nuovo AzResourceGroupDeployment** che crea una distribuzione in un gruppo di risorse.
Per aggiungere risorse a un abbonamento, usa il **nuovo-AzSubscriptionDeployment** che crea una distribuzione in ambito abbonamento, che distribuisce le risorse a livello di abbonamento.
Per aggiungere risorse in un gruppo di gestione, usare il **nuovo AzManagementGroupDeployment** che crea una distribuzione in un gruppo di gestione.

## ESEMPI

### Esempio 1: usare un modello e un file di parametro personalizzati per creare una distribuzione
```
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

Questo comando crea una nuova distribuzione nell'ambito del tenant corrente usando un modello personalizzato e un file modello su disco.
Il comando usa il parametro *TemplateFile* per specificare il modello e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori di parametro.

### Esempio 2: usare un oggetto modello personalizzato e un file di parametro per creare una distribuzione
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

Questo comando crea una nuova distribuzione presso il tenant corrente usando un modello personalizzato e un file modello su disco che è stato convertito in una tabella hash in memoria.
I primi due comandi leggono il testo per il file del modello su disco e lo convertono in una tabella hash in memoria.
L'ultimo comando usa il parametro *TemplateObject* per specificare questo Hashtable e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori di parametro.

## PARAMETRI

### -ApiVersion
Quando è impostato, indica la versione dell'API del provider di risorse da usare.
Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.

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

### -AsJob
Esegui cmdlet in background

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

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentDebugLogLevel
Livello del log di debug della distribuzione.

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

### -Posizione
Posizione in cui archiviare i dati di distribuzione.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome della distribuzione che verrà creata.
Valido solo quando viene usato un modello.
Quando viene usato un modello, se l'utente non specifica un nome di distribuzione, usa l'ora corrente, ad esempio "20131223140835".

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.

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

### -SkipTemplateParameterPrompt
Ignora l'elaborazione dei parametri dinamici di PowerShell che verifica se il parametro di modello specificato contiene tutti i parametri necessari usati dal modello.
Questo controllo consentirà all'utente di fornire un valore per i parametri mancanti, ma specificando che-SkipTemplateParameterPrompt ignorerà questo prompt e si verificherà un errore immediatamente se non è stato trovato un parametro associato al modello.
Per gli script non interattivi,-SkipTemplateParameterPrompt può essere fornito per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.

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

### -TemplateFile
Percorso locale del file di modello.

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateObject
Tabella hash che rappresenta il modello.

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterFile
Un file con i parametri del modello.

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterObject
Tabella hash che rappresenta i parametri.

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterUri
URI per il file del parametro di modello.

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateUri
URI nel file del modello.

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. Collections. Hashtable

### System. String

## OUTPUT

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT

## Note

## COLLEGAMENTI CORRELATI
