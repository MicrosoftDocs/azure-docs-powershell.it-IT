---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 193a1dab5bd08489740d0d95f65c6aad1ea85e43
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479164"
---
# <span data-ttu-id="f3dde-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="f3dde-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="f3dde-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3dde-102">SYNOPSIS</span></span>
<span data-ttu-id="f3dde-103">Visualizzare i metadati sulla caratteristica di salvataggio automatico del contesto, ad esempio se il contesto viene salvato automaticamente e in cui è possibile trovare informazioni sul contesto e le credenziali salvate.</span><span class="sxs-lookup"><span data-stu-id="f3dde-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="f3dde-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3dde-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3dde-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3dde-105">DESCRIPTION</span></span>
<span data-ttu-id="f3dde-106">Visualizzare i metadati sulla caratteristica di salvataggio automatico del contesto, ad esempio se il contesto viene salvato automaticamente e in cui è possibile trovare informazioni sul contesto e le credenziali salvate.</span><span class="sxs-lookup"><span data-stu-id="f3dde-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="f3dde-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3dde-107">EXAMPLES</span></span>

### <span data-ttu-id="f3dde-108">Ottenere i metadati di salvataggio del contesto per la sessione corrente</span><span class="sxs-lookup"><span data-stu-id="f3dde-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="f3dde-109">Ottenere informazioni dettagliate sull'eventuale salvataggio del contesto.</span><span class="sxs-lookup"><span data-stu-id="f3dde-109">Get details about whether and where the context is saved.</span></span>  <span data-ttu-id="f3dde-110">Nell'esempio precedente la caratteristica salvataggio automatico è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="f3dde-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="f3dde-111">Ottenere i metadati di salvataggio del contesto per l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="f3dde-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="f3dde-112">Informazioni su se e dove il contesto viene salvato per impostazione predefinita per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="f3dde-112">Get details about whether and where the context is saved by default for the current user.</span></span>  <span data-ttu-id="f3dde-113">Tieni presente che questa operazione può essere diversa dalle impostazioni attive nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="f3dde-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="f3dde-114">Nell'esempio precedente la caratteristica di salvataggio automatico è stata abilitata e i dati vengono salvati nella posizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f3dde-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="f3dde-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3dde-115">PARAMETERS</span></span>

### <span data-ttu-id="f3dde-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3dde-116">-DefaultProfile</span></span>
<span data-ttu-id="f3dde-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f3dde-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3dde-118">-Ambito</span><span class="sxs-lookup"><span data-stu-id="f3dde-118">-Scope</span></span>
<span data-ttu-id="f3dde-119">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="f3dde-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="f3dde-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3dde-120">CommonParameters</span></span>
<span data-ttu-id="f3dde-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3dde-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3dde-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3dde-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3dde-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3dde-123">INPUTS</span></span>

### <span data-ttu-id="f3dde-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f3dde-124">None</span></span>

## <span data-ttu-id="f3dde-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3dde-125">OUTPUTS</span></span>

### <span data-ttu-id="f3dde-126">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="f3dde-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="f3dde-127">Note</span><span class="sxs-lookup"><span data-stu-id="f3dde-127">NOTES</span></span>

## <span data-ttu-id="f3dde-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3dde-128">RELATED LINKS</span></span>
