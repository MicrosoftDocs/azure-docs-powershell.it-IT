---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6c0e557078bde5cbec7b1f7dd96f1fa2c71408a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860241"
---
# <span data-ttu-id="383bb-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="383bb-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="383bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="383bb-102">SYNOPSIS</span></span>
<span data-ttu-id="383bb-103">Consentire il salvataggio e la carica automatica delle credenziali di Azure, delle informazioni sull'account e dell'abbonamento quando si apre una finestra di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="383bb-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="383bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="383bb-104">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="383bb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="383bb-105">DESCRIPTION</span></span>
<span data-ttu-id="383bb-106">Consentire il salvataggio e la carica automatica delle credenziali di Azure, delle informazioni sull'account e dell'abbonamento quando si apre una finestra di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="383bb-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="383bb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="383bb-107">EXAMPLES</span></span>

### <span data-ttu-id="383bb-108">Abilitare il salvataggio delle credenziali per l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="383bb-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzContextAutosave
```

<span data-ttu-id="383bb-109">Attivare il salvataggio automatico delle credenziali per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="383bb-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="383bb-110">Ogni volta che viene aperta una finestra di PowerShell, il contesto corrente verrà ricordato senza effettuare l'accesso.</span><span class="sxs-lookup"><span data-stu-id="383bb-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="383bb-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="383bb-111">PARAMETERS</span></span>

### <span data-ttu-id="383bb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="383bb-112">-DefaultProfile</span></span>
<span data-ttu-id="383bb-113">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="383bb-113">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="383bb-114">-Ambito</span><span class="sxs-lookup"><span data-stu-id="383bb-114">-Scope</span></span>
<span data-ttu-id="383bb-115">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente</span><span class="sxs-lookup"><span data-stu-id="383bb-115">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="383bb-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="383bb-116">-Confirm</span></span>
<span data-ttu-id="383bb-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="383bb-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="383bb-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="383bb-118">-WhatIf</span></span>
<span data-ttu-id="383bb-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="383bb-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="383bb-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="383bb-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="383bb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="383bb-121">CommonParameters</span></span>
<span data-ttu-id="383bb-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="383bb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="383bb-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="383bb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="383bb-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="383bb-124">INPUTS</span></span>

### <span data-ttu-id="383bb-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="383bb-125">None</span></span>

## <span data-ttu-id="383bb-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="383bb-126">OUTPUTS</span></span>

### <span data-ttu-id="383bb-127">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="383bb-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="383bb-128">Note</span><span class="sxs-lookup"><span data-stu-id="383bb-128">NOTES</span></span>

## <span data-ttu-id="383bb-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="383bb-129">RELATED LINKS</span></span>
