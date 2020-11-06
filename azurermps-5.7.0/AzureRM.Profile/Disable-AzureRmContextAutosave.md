---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
ms.openlocfilehash: 622cbd399f554173bbe9734429f4ae787fe94d0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508072"
---
# <span data-ttu-id="eceef-101">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="eceef-101">Disable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="eceef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eceef-102">SYNOPSIS</span></span>
<span data-ttu-id="eceef-103">Disattivare il salvataggio delle credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="eceef-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="eceef-104">Le informazioni di accesso verranno dimenticate la volta successiva che si apre una finestra di PowerShell</span><span class="sxs-lookup"><span data-stu-id="eceef-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eceef-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eceef-105">SYNTAX</span></span>

```
Disable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eceef-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eceef-106">DESCRIPTION</span></span>
<span data-ttu-id="eceef-107">Disattivare il salvataggio delle credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="eceef-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="eceef-108">Le informazioni di accesso verranno dimenticate la volta successiva che si apre una finestra di PowerShell</span><span class="sxs-lookup"><span data-stu-id="eceef-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="eceef-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eceef-109">EXAMPLES</span></span>

### <span data-ttu-id="eceef-110">Disabilitare il salvataggio del contesto</span><span class="sxs-lookup"><span data-stu-id="eceef-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzureRmContextAutosave
```

<span data-ttu-id="eceef-111">Disabilitare il salvataggio automatico per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="eceef-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="eceef-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eceef-112">PARAMETERS</span></span>

### <span data-ttu-id="eceef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eceef-113">-DefaultProfile</span></span>
<span data-ttu-id="eceef-114">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="eceef-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eceef-115">-Ambito</span><span class="sxs-lookup"><span data-stu-id="eceef-115">-Scope</span></span>
<span data-ttu-id="eceef-116">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente</span><span class="sxs-lookup"><span data-stu-id="eceef-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="eceef-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eceef-117">-Confirm</span></span>
<span data-ttu-id="eceef-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eceef-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eceef-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eceef-119">-WhatIf</span></span>
<span data-ttu-id="eceef-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eceef-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eceef-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eceef-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eceef-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eceef-122">CommonParameters</span></span>
<span data-ttu-id="eceef-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eceef-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eceef-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eceef-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eceef-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eceef-125">INPUTS</span></span>

### <span data-ttu-id="eceef-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="eceef-126">None</span></span>

## <span data-ttu-id="eceef-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eceef-127">OUTPUTS</span></span>

### <span data-ttu-id="eceef-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="eceef-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="eceef-129">Informazioni sulle impostazioni di salvataggio automatico correnti, ad esempio se l'opzione Salvataggio automatico è abilitata per l'utente corrente e dove vengono salvati i file di contesto e credenziale.</span><span class="sxs-lookup"><span data-stu-id="eceef-129">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="eceef-130">Note</span><span class="sxs-lookup"><span data-stu-id="eceef-130">NOTES</span></span>

## <span data-ttu-id="eceef-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eceef-131">RELATED LINKS</span></span>

