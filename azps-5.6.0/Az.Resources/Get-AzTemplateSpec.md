---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: 0b2018eecc081f2fcee5da63ed17cc2e01486777
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960110"
---
# Get-AzTemplateSpec

## SYNOPSIS
Ottiene o elenca le specifiche del modello

## SINTASSI

### ListTemplateSpecsParameterSet (impostazione predefinita)
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetTemplateSpecByNameParameterSet
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetTemplateSpecByIdParameterSet
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Questo cmdlet può essere usato per elencare le specifiche dei modelli in un gruppo di sottoscrizioni/risorse o ottenere specifiche del modello in base al nome o all'ID. Se si riceve una specifica per nome/ID, è possibile recuperare una versione specifica specificando un nome di versione tramite il **parametro -Version.** Quando **si usa -Version,** saranno presenti solo i dettagli della versione specifici all'interno di **. Versioni nell'oggetto* spec del modello restituito. Se non viene specificata alcuna versione specifica durante il recupero di una specifica modello per nome/id, tutte le versioni saranno presenti all'interno di **. Proprietà Versions* dell'oggetto restituito.

**Nota:** quando si elencano tutte le specifiche del modello all'interno di una sottoscrizione o di un gruppo di risorse, vengono restituite specifiche del *modello " . Versions"* sarà *Null.* Le informazioni sulla versione vengono incluse solo quando vengono forniti parametri -Name o -ResourceId (ad esempio, si richiede una specifica o versione del modello).

## ESEMPI

### Esempio 1: Specifiche del modello di elenco nell'abbonamento corrente
```powershell
PS C:\> Get-AzTemplateSpec
```

Elenca tutte le specifiche dei modelli nell'abbonamento corrente.

### Esempio 2: Specifiche del modello di elenco in un gruppo di risorse
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

Elenca tutte le specifiche dei modelli nel gruppo di risorse "myRG" della sottoscrizione corrente.

### Esempio 3: Ottenere le specifiche del modello (con tutte le versioni) in base al nome
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

Ottiene informazioni sulla specifica del modello denominata "MyTemplateSpec" all'interno del gruppo di risorse "myRG".

**Nota:** tutte le versioni delle specifiche del modello saranno presenti all'interno di "*. Versions*" proprietà dell'oggetto restituito.

### Esempio 4: Ottenere le specifiche del modello (versione specifica) in base al nome
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

Ottiene informazioni sulla versione "v1.0" della specifica di modello denominata "MyTemplateSpec" all'interno del gruppo di risorse "myRG".

**Nota:** *". Versions"* dell'oggetto restituito conterrà solo la versione specifica richiesta.

### Esempio 5: Ottenere le specifiche del modello (con tutte le versioni) in base all'ID risorsa
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

Ottiene informazioni sulla specifica del modello denominata "MyTemplateSpec" all'interno del gruppo di risorse "myRG" del \{ subId della \} sottoscrizione.

**Nota:** tutte le versioni delle specifiche del modello saranno presenti all'interno di "*. Versions*" proprietà dell'oggetto restituito.

### Esempio 6: Ottenere le specifiche del modello (versione specifica) in base all'ID risorsa
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

Ottiene informazioni sulla versione 'v1.0' della specifica di modello denominata "MyTemplateSpec" all'interno del gruppo di risorse 'myRG' di \{ subscription \} subId.

**Nota:** *". Versions"* dell'oggetto restituito conterrà solo la versione specifica richiesta.

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

### -Name
Nome della specifica di modello.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
ID risorsa completo della specifica del modello. Esempio: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Versione delle specifiche del modello.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec

## NOTE

## COLLEGAMENTI CORRELATI
