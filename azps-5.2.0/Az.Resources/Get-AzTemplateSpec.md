---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365270"
---
# Get-AzTemplateSpec

## Sinossi
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

## Descrizione
Questo cmdlet può essere usato per elencare le specifiche di un modello in un gruppo di abbonamenti/risorse o per ottenere una specifica specifiche del modello per nome o ID. Quando si riceve un modello specifico per nome/ID, è possibile recuperare facoltativamente una versione specifica specificando un nome di versione tramite il parametro **-Version** . Quando viene usata la **versione** , solo i dettagli specifici della versione saranno presenti in **. Versioni* nell'oggetto spec modello restituito. Se non viene specificata una versione specifica durante il recupero di una specifica modello per nome/ID, tutte le versioni saranno presenti all'interno di **. Proprietà Versions* dell'oggetto restituito.

**Nota**: quando si elencano tutte le specifiche del modello all'interno di un gruppo di abbonamenti o risorse, ogni specifica di modello restituita è *". La proprietà Versions* sarà *null*. Le informazioni sulla versione sono incluse solo quando-Name oppure-i parametri ResourceId sono disponibili (ad esempio: si richiede una specifica/versione del modello specifico).

## ESEMPI

### Esempio 1: specifiche del modello di elenco nell'abbonamento corrente
```powershell
PS C:\> Get-AzTemplateSpec
```

Elenca tutte le specifiche del modello nell'abbonamento corrente.

### Esempio 2: specifiche del modello di elenco in un gruppo di risorse
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

Elenca tutte le specifiche del modello nel gruppo di risorse "myRG" della sottoscrizione corrente.

### Esempio 3: ottenere la specifica del modello (con tutte le versioni) per nome
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

Ottiene informazioni sulla specifica del modello denominata "MyTemplateSpec" nel gruppo di risorse "myRG".

**Nota**: tutte le versioni della specifica del modello saranno presenti all'interno del "*. Proprietà Versions* dell'oggetto return.

### Esempio 4: ottenere la specifica del modello (versione specifica) per nome
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

Ottiene le informazioni sulla versione "v 1.0" della specifica del modello denominata "MyTemplateSpec" nel gruppo di risorse "myRG".

**Nota**: *". La proprietà Versions* dell'oggetto restituito conterrà solo la versione specifica richiesta.

### Esempio 5: ottenere la specifica del modello (con tutte le versioni) per ID risorsa
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

Ottiene le informazioni sulla specifica del modello denominata "MyTemplateSpec" nel gruppo di risorse "myRG" dell'abbonamento \{ subId \} .

**Nota**: tutte le versioni della specifica del modello saranno presenti all'interno del "*. Proprietà Versions* dell'oggetto return.

### Esempio 6: ottenere la specifica del modello (versione specifica) per ID risorsa
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

Ottiene le informazioni sulla versione "v 1.0" della specifica del modello denominata "MyTemplateSpec" nel gruppo di risorse "myRG" della sottoscrizione di \{ subId \} .

**Nota**: *". La proprietà Versions* dell'oggetto restituito conterrà solo la versione specifica richiesta.

## PARAMETRI

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

### -Nome
Nome della specifica del modello.

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
ID risorsa completo del modello spec. esempio:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

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

### -Versione
Versione della specifica del modello.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSTemplateSpec

## Note

## COLLEGAMENTI CORRELATI
