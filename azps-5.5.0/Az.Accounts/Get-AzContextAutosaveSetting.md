---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 193a1dab5bd08489740d0d95f65c6aad1ea85e43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199934"
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

### Ottenere i metadati di salvataggio del contesto per la sessione corrente
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

Informazioni dettagliate su se e dove salvare il contesto per impostazione predefinita per l'utente corrente.  Si noti che questa impostazione potrebbe essere diversa da quella attiva nella sessione corrente. Nell'esempio precedente la funzionalità di salvataggio automatico è stata abilitata e i dati vengono salvati nella posizione predefinita.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings

## NOTE

## COLLEGAMENTI CORRELATI
