---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
ms.openlocfilehash: 15dcc77a616037d6190fa11be34b8bc8f762aa59
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188265"
---
# Get-AzDeploymentWhatIfResult

## Sinossi
Ottiene un modello ARM What-If risultato per una distribuzione nell'ambito dell'abbonamento. 

## SINTASSI

### ByTemplateFileWithNoParameters (impostazione predefinita)
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByTemplateObjectAndParameterObject
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByTemplateFileAndParameterObject
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByTemplateUriAndParameterObject
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByTemplateObjectAndParameterFile
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByTemplateFileAndParameterFile
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByTemplateUriAndParameterFile
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByTemplateObjectAndParameterUri
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByTemplateFileAndParameterUri
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByTemplateUriAndParameterUri
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByTemplateObjectWithNoParameters
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByTemplateUriWithNoParameters
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzDeploymentWhatIfResult** restituisce il modello ARM What-If risultato per una distribuzione di modelli nell'ambito dell'abbonamento corrente. Restituisce un elenco di modifiche che indicano quali risorse verranno aggiornate se la distribuzione viene applicata senza apportare modifiche alle risorse reali. Per specificare il formato per il risultato restituito, usa il parametro *ResultFormat* .

## ESEMPI

### Esempio 1: ottenere un risultato What-If all'ambito dell'abbonamento
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

Questo comando ottiene un risultato What-If nell'ambito dell'abbonamento corrente usando un file di modello personalizzato e un file di parametro su disco.
Il comando usa il parametro *location* per specificare dove archiviare i dati di distribuzione.
Il comando usa il parametro *TemplateFile* per specificare un file modello.
Il comando usa il parametro *TemplateParameterFile* per specificare un file di parametro di modello.
Il comando usa il parametro *ResultFormat* per impostare il risultato What-If per includere payload di risorse completo.

### Esempio 2: ottenere un risultato What-If all'ambito dell'abbonamento con ResourceIdOnly
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

Questo comando ottiene un risultato What-If nell'ambito dell'abbonamento corrente usando un file di modello personalizzato e un file di parametro su disco.
Il comando usa il parametro *location* per specificare dove archiviare i dati di distribuzione.
Il comando usa il parametro *TemplateFile* per specificare un file modello.
Il comando usa il parametro *TemplateParameterFile* per specificare un file di parametro di modello.
Il comando usa il parametro *ResultFormat* per impostare il risultato What-If solo per contenere gli ID delle risorse.

## PARAMETRI

### -ApiVersion
Quando è impostato, indica la versione dell'API del provider di risorse da usare.
Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.

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

### -ExcludeChangeType
Elenco delimitato da virgole dei tipi di modifica delle risorse da escludere dai risultati What-If.

```yaml
Type: System.String[]
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome della distribuzione che verrà creata. Se non viene specificato, il nome del file del modello viene impostato automaticamente quando viene fornito un file di modello; il valore predefinito è l'ora corrente in cui viene fornito un oggetto modello, ad esempio "20131223140835".

```yaml
Type: System.String
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResultFormat
Formato del risultato What-If.

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.WhatIfResultFormat
Parameter Sets: (All)
Aliases:
Accepted values: ResourceIdOnly, FullResourcePayloads

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
Type: System.Management.Automation.SwitchParameter
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
Type: System.String
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
Type: System.Collections.Hashtable
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
Type: System.String
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
Type: System.Collections.Hashtable
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
Type: System.String
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
Type: System.String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. Collections. Hashtable

### System. String

## OUTPUT

### Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. Deployments. PSWhatIfOperationResult

## Note

## COLLEGAMENTI CORRELATI
