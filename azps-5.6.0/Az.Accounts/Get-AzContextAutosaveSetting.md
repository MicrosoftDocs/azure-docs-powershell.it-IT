---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 629e35c5b700477fc46565b2da0e5dcf6f3c5b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981342"
---
# Get-AzContextAutosaveSetting

## SYNOPSIS
Visualizzare i metadati sulla caratteristica di salvataggio automatico del contesto, ad esempio se il contesto viene salvato automaticamente e dove vengono trovate le informazioni relative al contesto e alle credenziali salvate.

## SINTASSI

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Visualizzare i metadati sulla caratteristica di salvataggio automatico del contesto, ad esempio se il contesto viene salvato automaticamente e dove vengono trovate le informazioni relative al contesto e alle credenziali salvate.

## ESEMPI

### Ottenere i metadati per il salvataggio del contesto per la sessione corrente
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

Informazioni dettagliate su se e dove viene salvato il contesto.  Nell'esempio precedente la funzionalità di salvataggio automatico è stata disabilitata.

### Ottenere i metadati per il salvataggio del contesto per l'utente corrente
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

Informazioni dettagliate su se e dove salvare il contesto per impostazione predefinita per l'utente corrente.  Si noti che questa impostazione potrebbe essere diversa da quella attiva nella sessione corrente. Nell'esempio precedente la funzionalità di salvataggio automatico è stata abilitata e i dati vengono salvati nel percorso predefinito.

## PARAMETERS

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

### -Scope
Determina l'ambito delle modifiche di contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente.

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings

## NOTE

## COLLEGAMENTI CORRELATI
