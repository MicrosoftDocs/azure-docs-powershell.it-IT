---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: d5c31519ba55babb79e3e902a01e46746c5b70f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189866"
---
# <span data-ttu-id="09539-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="09539-101">Remove-AzContext</span></span>

## <span data-ttu-id="09539-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09539-102">SYNOPSIS</span></span>
<span data-ttu-id="09539-103">Rimuovere un contesto dal set di contesti disponibili</span><span class="sxs-lookup"><span data-stu-id="09539-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="09539-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09539-104">SYNTAX</span></span>

### <span data-ttu-id="09539-105">RemoveByInputObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="09539-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09539-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="09539-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="09539-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09539-107">DESCRIPTION</span></span>
<span data-ttu-id="09539-108">Rimuovere un contesto Azure dal set di contesti</span><span class="sxs-lookup"><span data-stu-id="09539-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="09539-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09539-109">EXAMPLES</span></span>

### <span data-ttu-id="09539-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="09539-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="09539-111">Rimuovere il contesto denominato default</span><span class="sxs-lookup"><span data-stu-id="09539-111">Remove the context named default</span></span>

## <span data-ttu-id="09539-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09539-112">PARAMETERS</span></span>

### <span data-ttu-id="09539-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09539-113">-DefaultProfile</span></span>
<span data-ttu-id="09539-114">Le credenziali, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09539-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09539-115">-Force</span><span class="sxs-lookup"><span data-stu-id="09539-115">-Force</span></span>
<span data-ttu-id="09539-116">Rimuovi contesto anche se è l'impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="09539-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="09539-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09539-117">-InputObject</span></span>
<span data-ttu-id="09539-118">Oggetto context, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="09539-118">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="09539-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="09539-119">-Name</span></span>
<span data-ttu-id="09539-120">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="09539-120">The name of the context</span></span>

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

### <span data-ttu-id="09539-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09539-121">-PassThru</span></span>
<span data-ttu-id="09539-122">Restituire il contesto rimosso</span><span class="sxs-lookup"><span data-stu-id="09539-122">Return the removed context</span></span>

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

### <span data-ttu-id="09539-123">-Ambito</span><span class="sxs-lookup"><span data-stu-id="09539-123">-Scope</span></span>
<span data-ttu-id="09539-124">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente</span><span class="sxs-lookup"><span data-stu-id="09539-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="09539-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="09539-125">-Confirm</span></span>
<span data-ttu-id="09539-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09539-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09539-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09539-127">-WhatIf</span></span>
<span data-ttu-id="09539-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09539-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09539-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09539-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09539-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09539-130">CommonParameters</span></span>
<span data-ttu-id="09539-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09539-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09539-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09539-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09539-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09539-133">INPUTS</span></span>

### <span data-ttu-id="09539-134">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="09539-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="09539-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09539-135">OUTPUTS</span></span>

### <span data-ttu-id="09539-136">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="09539-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="09539-137">Note</span><span class="sxs-lookup"><span data-stu-id="09539-137">NOTES</span></span>

## <span data-ttu-id="09539-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09539-138">RELATED LINKS</span></span>
