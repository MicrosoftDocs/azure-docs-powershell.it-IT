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
# <span data-ttu-id="01fcf-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="01fcf-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="01fcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="01fcf-103">Visualizzare i metadati sulla caratteristica di salvataggio automatico del contesto, ad esempio se il contesto viene salvato automaticamente e dove vengono trovate le informazioni relative al contesto e alle credenziali salvate.</span><span class="sxs-lookup"><span data-stu-id="01fcf-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="01fcf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01fcf-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01fcf-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="01fcf-105">DESCRIPTION</span></span>
<span data-ttu-id="01fcf-106">Visualizzare i metadati sulla caratteristica di salvataggio automatico del contesto, ad esempio se il contesto viene salvato automaticamente e dove vengono trovate le informazioni relative al contesto e alle credenziali salvate.</span><span class="sxs-lookup"><span data-stu-id="01fcf-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="01fcf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01fcf-107">EXAMPLES</span></span>

### <span data-ttu-id="01fcf-108">Ottenere i metadati per il salvataggio del contesto per la sessione corrente</span><span class="sxs-lookup"><span data-stu-id="01fcf-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="01fcf-109">Informazioni dettagliate su se e dove viene salvato il contesto.</span><span class="sxs-lookup"><span data-stu-id="01fcf-109">Get details about whether and where the context is saved.</span></span>  <span data-ttu-id="01fcf-110">Nell'esempio precedente la funzionalità di salvataggio automatico è stata disabilitata.</span><span class="sxs-lookup"><span data-stu-id="01fcf-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="01fcf-111">Ottenere i metadati per il salvataggio del contesto per l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="01fcf-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="01fcf-112">Informazioni dettagliate su se e dove salvare il contesto per impostazione predefinita per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="01fcf-112">Get details about whether and where the context is saved by default for the current user.</span></span>  <span data-ttu-id="01fcf-113">Si noti che questa impostazione potrebbe essere diversa da quella attiva nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="01fcf-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="01fcf-114">Nell'esempio precedente la funzionalità di salvataggio automatico è stata abilitata e i dati vengono salvati nel percorso predefinito.</span><span class="sxs-lookup"><span data-stu-id="01fcf-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="01fcf-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01fcf-115">PARAMETERS</span></span>

### <span data-ttu-id="01fcf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01fcf-116">-DefaultProfile</span></span>
<span data-ttu-id="01fcf-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="01fcf-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01fcf-118">-Scope</span><span class="sxs-lookup"><span data-stu-id="01fcf-118">-Scope</span></span>
<span data-ttu-id="01fcf-119">Determina l'ambito delle modifiche di contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="01fcf-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="01fcf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01fcf-120">CommonParameters</span></span>
<span data-ttu-id="01fcf-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01fcf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01fcf-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="01fcf-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01fcf-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="01fcf-123">INPUTS</span></span>

### <span data-ttu-id="01fcf-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="01fcf-124">None</span></span>

## <span data-ttu-id="01fcf-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01fcf-125">OUTPUTS</span></span>

### <span data-ttu-id="01fcf-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="01fcf-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="01fcf-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="01fcf-127">NOTES</span></span>

## <span data-ttu-id="01fcf-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01fcf-128">RELATED LINKS</span></span>
