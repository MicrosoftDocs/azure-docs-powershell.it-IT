---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
ms.openlocfilehash: d0d6c69bb85fcdf851f0f134bb376252525aec91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519402"
---
# <span data-ttu-id="1aee3-101">Get-AzureRmContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="1aee3-101">Get-AzureRmContextAutosaveSetting</span></span>

## <span data-ttu-id="1aee3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1aee3-102">SYNOPSIS</span></span>
<span data-ttu-id="1aee3-103">Visualizzare i metadati sulla caratteristica di salvataggio automatico del contesto, incluso whterh il contesto viene automaticamente Aved e dove è possibile trovare informazioni sul contesto e le credenziali salvate.</span><span class="sxs-lookup"><span data-stu-id="1aee3-103">Display metadata about the context autosave feature, including whterh the context is automaticallys aved, and where saved context and credential information cna be found.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1aee3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1aee3-104">SYNTAX</span></span>

```
Get-AzureRmContextAutosaveSetting [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1aee3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1aee3-105">DESCRIPTION</span></span>
<span data-ttu-id="1aee3-106">Visualizzare i metadati sulla caratteristica di salvataggio automatico del contesto, ad esempio se il contesto viene salvato automaticamente e in cui è possibile trovare informazioni sul contesto e le credenziali salvate.</span><span class="sxs-lookup"><span data-stu-id="1aee3-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="1aee3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1aee3-107">EXAMPLES</span></span>

### <span data-ttu-id="1aee3-108">Ottenere i metadati di salvataggio del contesto per la sessione corrente</span><span class="sxs-lookup"><span data-stu-id="1aee3-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="1aee3-109">Ottenere informazioni su se e wehere il contesto viene salvato.</span><span class="sxs-lookup"><span data-stu-id="1aee3-109">Get details about whether and wehere the context is saved.</span></span>  <span data-ttu-id="1aee3-110">Nell'esempio precedente la caratteristica salvataggio automatico è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="1aee3-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="1aee3-111">Ottenere i metadati di salvataggio del contesto per l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="1aee3-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="1aee3-112">Informazioni su se e wehere il contesto viene salvato per impostazione predefinita per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="1aee3-112">Get details about whether and wehere the context is saved by default for the current user.</span></span>  <span data-ttu-id="1aee3-113">Tieni presente che questa operazione può essere diversa dalle impostazioni attive nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="1aee3-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="1aee3-114">Nell'esempio precedente la caratteristica di salvataggio automatico è stata abilitata e i dati vengono salvati nella posizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1aee3-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="1aee3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1aee3-115">PARAMETERS</span></span>

### <span data-ttu-id="1aee3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aee3-116">-DefaultProfile</span></span>
<span data-ttu-id="1aee3-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1aee3-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aee3-118">-Ambito</span><span class="sxs-lookup"><span data-stu-id="1aee3-118">-Scope</span></span>
<span data-ttu-id="1aee3-119">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="1aee3-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aee3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aee3-120">CommonParameters</span></span>
<span data-ttu-id="1aee3-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aee3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aee3-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aee3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aee3-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1aee3-123">INPUTS</span></span>

### <span data-ttu-id="1aee3-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1aee3-124">None</span></span>

## <span data-ttu-id="1aee3-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1aee3-125">OUTPUTS</span></span>

### <span data-ttu-id="1aee3-126">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="1aee3-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="1aee3-127">Informazioni sulle impostazioni di salvataggio automatico correnti, ad esempio se l'opzione Salvataggio automatico è abilitata per l'utente corrente e dove vengono salvati i file di contesto e credenziale.</span><span class="sxs-lookup"><span data-stu-id="1aee3-127">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="1aee3-128">Note</span><span class="sxs-lookup"><span data-stu-id="1aee3-128">NOTES</span></span>

## <span data-ttu-id="1aee3-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1aee3-129">RELATED LINKS</span></span>

