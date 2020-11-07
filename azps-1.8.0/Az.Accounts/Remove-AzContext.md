---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: a2fc63409f36215d40fcf1e2e17c48b4dbe89e11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673743"
---
# <span data-ttu-id="b079c-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="b079c-101">Remove-AzContext</span></span>

## <span data-ttu-id="b079c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b079c-102">SYNOPSIS</span></span>
<span data-ttu-id="b079c-103">Rimuovere un contesto dal set di contesti disponibili</span><span class="sxs-lookup"><span data-stu-id="b079c-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="b079c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b079c-104">SYNTAX</span></span>

### <span data-ttu-id="b079c-105">RemoveByInputObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b079c-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b079c-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="b079c-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="b079c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b079c-107">DESCRIPTION</span></span>
<span data-ttu-id="b079c-108">Rimuovere un contesto Azure dal set di contesti</span><span class="sxs-lookup"><span data-stu-id="b079c-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="b079c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b079c-109">EXAMPLES</span></span>

### <span data-ttu-id="b079c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b079c-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="b079c-111">Rimuovere il contesto denominato default</span><span class="sxs-lookup"><span data-stu-id="b079c-111">Remove the context named default</span></span>

## <span data-ttu-id="b079c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b079c-112">PARAMETERS</span></span>

### <span data-ttu-id="b079c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b079c-113">-DefaultProfile</span></span>
<span data-ttu-id="b079c-114">Le credenziali, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b079c-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b079c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b079c-115">-Force</span></span>
<span data-ttu-id="b079c-116">Rimuovi contesto anche se è il defualt</span><span class="sxs-lookup"><span data-stu-id="b079c-116">Remove context even if it is the defualt</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b079c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b079c-117">-InputObject</span></span>
<span data-ttu-id="b079c-118">Oggetto context, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="b079c-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b079c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b079c-119">-Name</span></span>
<span data-ttu-id="b079c-120">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="b079c-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b079c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b079c-121">-PassThru</span></span>
<span data-ttu-id="b079c-122">Restituire il contesto rimosso</span><span class="sxs-lookup"><span data-stu-id="b079c-122">Return the removed context</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b079c-123">-Ambito</span><span class="sxs-lookup"><span data-stu-id="b079c-123">-Scope</span></span>
<span data-ttu-id="b079c-124">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente</span><span class="sxs-lookup"><span data-stu-id="b079c-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="b079c-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b079c-125">-Confirm</span></span>
<span data-ttu-id="b079c-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b079c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b079c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b079c-127">-WhatIf</span></span>
<span data-ttu-id="b079c-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b079c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b079c-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b079c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b079c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b079c-130">CommonParameters</span></span>
<span data-ttu-id="b079c-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b079c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b079c-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b079c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b079c-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b079c-133">INPUTS</span></span>

### <span data-ttu-id="b079c-134">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="b079c-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="b079c-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b079c-135">OUTPUTS</span></span>

### <span data-ttu-id="b079c-136">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="b079c-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="b079c-137">Note</span><span class="sxs-lookup"><span data-stu-id="b079c-137">NOTES</span></span>

## <span data-ttu-id="b079c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b079c-138">RELATED LINKS</span></span>
