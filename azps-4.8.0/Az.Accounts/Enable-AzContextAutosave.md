---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189884"
---
# <span data-ttu-id="b94ee-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="b94ee-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="b94ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b94ee-102">SYNOPSIS</span></span>
<span data-ttu-id="b94ee-103">I contesti di Azure sono oggetti di PowerShell che rappresentano l'abbonamento attivo per eseguire comandi e le informazioni di autenticazione necessarie per connettersi a un cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="b94ee-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="b94ee-104">Con i contesti di Azure, Azure PowerShell non deve riautenticare l'account ogni volta che si cambia abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b94ee-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="b94ee-105">Per altre informazioni, Vedi [oggetti Context di Azure PowerShell](https://docs.microsoft.com/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="b94ee-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="b94ee-106">Questo cmdlet consente di salvare e caricare automaticamente le informazioni sul contesto di Azure quando si avvia un processo di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b94ee-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="b94ee-107">Ad esempio, quando si apre una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="b94ee-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="b94ee-108">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b94ee-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b94ee-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b94ee-109">DESCRIPTION</span></span>

<span data-ttu-id="b94ee-110">Consente di salvare le informazioni di contesto di Azure e caricarle automaticamente all'avvio di un processo di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b94ee-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="b94ee-111">Il contesto viene salvato alla fine dell'esecuzione di qualsiasi cmdlet che influisce sul contesto.</span><span class="sxs-lookup"><span data-stu-id="b94ee-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="b94ee-112">Ad esempio, qualsiasi cmdlet di profilo.</span><span class="sxs-lookup"><span data-stu-id="b94ee-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="b94ee-113">Se si usa l'autenticazione utente, i token possono essere aggiornati durante l'uso di qualsiasi cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b94ee-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="b94ee-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b94ee-114">EXAMPLES</span></span>

### <span data-ttu-id="b94ee-115">Esempio 1: abilitare il salvataggio delle credenziali per l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="b94ee-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="b94ee-116">Attivare il salvataggio automatico delle credenziali per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="b94ee-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="b94ee-117">Ogni volta che viene aperta una finestra di PowerShell, il contesto corrente viene ricordato senza effettuare l'accesso.</span><span class="sxs-lookup"><span data-stu-id="b94ee-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="b94ee-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b94ee-118">Example 2</span></span>

<span data-ttu-id="b94ee-119">Consente di salvare e caricare automaticamente le informazioni di credenziali, account e sottoscrizione di Azure quando si apre una finestra di PowerShell in questa sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b94ee-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="b94ee-120">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="b94ee-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="b94ee-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b94ee-121">PARAMETERS</span></span>

### <span data-ttu-id="b94ee-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b94ee-122">-DefaultProfile</span></span>

<span data-ttu-id="b94ee-123">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b94ee-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="b94ee-124">-Ambito</span><span class="sxs-lookup"><span data-stu-id="b94ee-124">-Scope</span></span>

<span data-ttu-id="b94ee-125">Determina l'ambito delle modifiche al contesto.</span><span class="sxs-lookup"><span data-stu-id="b94ee-125">Determines the scope of context changes.</span></span> <span data-ttu-id="b94ee-126">Ad esempio, se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="b94ee-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="b94ee-127">Le modifiche apportate all'ambito `CurrentUser` verranno applicate a tutte le sessioni di PowerShell avviate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b94ee-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="b94ee-128">Se una particolare sessione deve avere impostazioni diverse, usare l'ambito `Process` .</span><span class="sxs-lookup"><span data-stu-id="b94ee-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

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

### <span data-ttu-id="b94ee-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b94ee-129">-Confirm</span></span>

<span data-ttu-id="b94ee-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b94ee-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b94ee-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b94ee-131">-WhatIf</span></span>

<span data-ttu-id="b94ee-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b94ee-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b94ee-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b94ee-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="b94ee-134">Parametri comuni</span><span class="sxs-lookup"><span data-stu-id="b94ee-134">Common Parameters</span></span>

<span data-ttu-id="b94ee-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b94ee-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b94ee-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b94ee-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b94ee-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b94ee-137">INPUTS</span></span>

### <span data-ttu-id="b94ee-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b94ee-138">None</span></span>

## <span data-ttu-id="b94ee-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b94ee-139">OUTPUTS</span></span>

### <span data-ttu-id="b94ee-140">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="b94ee-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="b94ee-141">Note</span><span class="sxs-lookup"><span data-stu-id="b94ee-141">NOTES</span></span>

## <span data-ttu-id="b94ee-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b94ee-142">RELATED LINKS</span></span>
