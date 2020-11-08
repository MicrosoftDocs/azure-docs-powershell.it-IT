---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
ms.openlocfilehash: c5d01fcc7ba007a0336fac5c08db44b840e75806
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020988"
---
# <span data-ttu-id="86b12-101">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="86b12-101">Disable-AzContextAutosave</span></span>

## <span data-ttu-id="86b12-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86b12-102">SYNOPSIS</span></span>
<span data-ttu-id="86b12-103">Disattivare il salvataggio delle credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="86b12-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="86b12-104">Le informazioni di accesso verranno dimenticate la volta successiva che si apre una finestra di PowerShell</span><span class="sxs-lookup"><span data-stu-id="86b12-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="86b12-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86b12-105">SYNTAX</span></span>

```
Disable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86b12-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86b12-106">DESCRIPTION</span></span>
<span data-ttu-id="86b12-107">Disattivare il salvataggio delle credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="86b12-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="86b12-108">Le informazioni di accesso verranno dimenticate la volta successiva che si apre una finestra di PowerShell</span><span class="sxs-lookup"><span data-stu-id="86b12-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="86b12-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86b12-109">EXAMPLES</span></span>

### <span data-ttu-id="86b12-110">Disabilitare il salvataggio del contesto</span><span class="sxs-lookup"><span data-stu-id="86b12-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzContextAutosave
```

<span data-ttu-id="86b12-111">Disabilitare il salvataggio automatico per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="86b12-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="86b12-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86b12-112">PARAMETERS</span></span>

### <span data-ttu-id="86b12-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86b12-113">-DefaultProfile</span></span>
<span data-ttu-id="86b12-114">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="86b12-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86b12-115">-Ambito</span><span class="sxs-lookup"><span data-stu-id="86b12-115">-Scope</span></span>
<span data-ttu-id="86b12-116">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente</span><span class="sxs-lookup"><span data-stu-id="86b12-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="86b12-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="86b12-117">-Confirm</span></span>
<span data-ttu-id="86b12-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86b12-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86b12-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86b12-119">-WhatIf</span></span>
<span data-ttu-id="86b12-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86b12-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86b12-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86b12-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86b12-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86b12-122">CommonParameters</span></span>
<span data-ttu-id="86b12-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86b12-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86b12-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86b12-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86b12-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86b12-125">INPUTS</span></span>

### <span data-ttu-id="86b12-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="86b12-126">None</span></span>

## <span data-ttu-id="86b12-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86b12-127">OUTPUTS</span></span>

### <span data-ttu-id="86b12-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="86b12-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="86b12-129">Note</span><span class="sxs-lookup"><span data-stu-id="86b12-129">NOTES</span></span>

## <span data-ttu-id="86b12-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86b12-130">RELATED LINKS</span></span>
