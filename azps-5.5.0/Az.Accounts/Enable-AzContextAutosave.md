---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195446"
---
# <span data-ttu-id="21129-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="21129-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="21129-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21129-102">SYNOPSIS</span></span>
<span data-ttu-id="21129-103">I contesti di Azure sono oggetti di PowerShell che rappresentano l'abbonamento attivo su cui eseguire i comandi e le informazioni di autenticazione necessarie per connettersi a un cloud Azure.</span><span class="sxs-lookup"><span data-stu-id="21129-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="21129-104">Con i contesti di Azure, Azure PowerShell non deve essere riautorizzare l'account ogni volta che si cambia abbonamento.</span><span class="sxs-lookup"><span data-stu-id="21129-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="21129-105">Per altre informazioni, vedere oggetti di [contesto di Azure PowerShell.](https://docs.microsoft.com/powershell/azure/context-persistence)</span><span class="sxs-lookup"><span data-stu-id="21129-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="21129-106">Questo cmdlet consente di salvare e caricare automaticamente le informazioni relative al contesto di Azure quando si avvia un processo di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="21129-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="21129-107">Ad esempio, quando si apre una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="21129-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="21129-108">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21129-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21129-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="21129-109">DESCRIPTION</span></span>

<span data-ttu-id="21129-110">Consente di salvare e caricare automaticamente le informazioni di contesto di Azure all'avvio di un processo di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="21129-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="21129-111">Il contesto viene salvato al termine dell'esecuzione di qualsiasi cmdlet che influisce sul contesto.</span><span class="sxs-lookup"><span data-stu-id="21129-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="21129-112">Ad esempio, qualsiasi cmdlet del profilo.</span><span class="sxs-lookup"><span data-stu-id="21129-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="21129-113">Se si usa l'autenticazione utente, i token possono essere aggiornati durante l'esecuzione di qualsiasi cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21129-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="21129-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21129-114">EXAMPLES</span></span>

### <span data-ttu-id="21129-115">Esempio 1: Abilitare le credenziali di salvataggio automatico per l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="21129-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="21129-116">Attivare il salvataggio automatico delle credenziali per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="21129-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="21129-117">Ogni volta che si apre una finestra di PowerShell, il contesto corrente viene memorizzata senza eseguire l'accesso.</span><span class="sxs-lookup"><span data-stu-id="21129-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="21129-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="21129-118">Example 2</span></span>

<span data-ttu-id="21129-119">Consentire il salvataggio e il caricamento automatico delle informazioni su credenziali, account e abbonamenti di Azure quando si apre una finestra di PowerShell in questa sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="21129-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="21129-120">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="21129-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="21129-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21129-121">PARAMETERS</span></span>

### <span data-ttu-id="21129-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21129-122">-DefaultProfile</span></span>

<span data-ttu-id="21129-123">Le credenziali, il tenant e la sottoscrizione usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="21129-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="21129-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="21129-124">-Scope</span></span>

<span data-ttu-id="21129-125">Determina l'ambito delle modifiche di contesto.</span><span class="sxs-lookup"><span data-stu-id="21129-125">Determines the scope of context changes.</span></span> <span data-ttu-id="21129-126">Ad esempio, se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="21129-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="21129-127">Le modifiche apportate con `CurrentUser` l'ambito influiscono su tutte le sessioni di PowerShell avviate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="21129-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="21129-128">Se una particolare sessione deve avere impostazioni diverse, usare `Process` l'ambito.</span><span class="sxs-lookup"><span data-stu-id="21129-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21129-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21129-129">-Confirm</span></span>

<span data-ttu-id="21129-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21129-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21129-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21129-131">-WhatIf</span></span>

<span data-ttu-id="21129-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21129-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21129-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21129-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="21129-134">Parametri comuni</span><span class="sxs-lookup"><span data-stu-id="21129-134">Common Parameters</span></span>

<span data-ttu-id="21129-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21129-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21129-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="21129-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21129-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="21129-137">INPUTS</span></span>

### <span data-ttu-id="21129-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="21129-138">None</span></span>

## <span data-ttu-id="21129-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21129-139">OUTPUTS</span></span>

### <span data-ttu-id="21129-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="21129-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="21129-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="21129-141">NOTES</span></span>

## <span data-ttu-id="21129-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21129-142">RELATED LINKS</span></span>
