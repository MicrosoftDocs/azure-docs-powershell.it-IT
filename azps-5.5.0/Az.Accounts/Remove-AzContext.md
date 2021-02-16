---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: d5c31519ba55babb79e3e902a01e46746c5b70f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190439"
---
# <span data-ttu-id="c0c05-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="c0c05-101">Remove-AzContext</span></span>

## <span data-ttu-id="c0c05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0c05-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c05-103">Rimuovere un contesto dal set di contesti disponibili</span><span class="sxs-lookup"><span data-stu-id="c0c05-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="c0c05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0c05-104">SYNTAX</span></span>

### <span data-ttu-id="c0c05-105">RemoveByInputObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c0c05-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0c05-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="c0c05-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="c0c05-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c0c05-107">DESCRIPTION</span></span>
<span data-ttu-id="c0c05-108">Rimuovere un contesto azure dal set di contesti</span><span class="sxs-lookup"><span data-stu-id="c0c05-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="c0c05-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0c05-109">EXAMPLES</span></span>

### <span data-ttu-id="c0c05-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c0c05-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="c0c05-111">Rimuovere il contesto denominato predefinito</span><span class="sxs-lookup"><span data-stu-id="c0c05-111">Remove the context named default</span></span>

## <span data-ttu-id="c0c05-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0c05-112">PARAMETERS</span></span>

### <span data-ttu-id="c0c05-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c05-113">-DefaultProfile</span></span>
<span data-ttu-id="c0c05-114">Le credenziali, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0c05-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0c05-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c0c05-115">-Force</span></span>
<span data-ttu-id="c0c05-116">Rimuovere il contesto anche se è l'impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="c0c05-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="c0c05-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0c05-117">-InputObject</span></span>
<span data-ttu-id="c0c05-118">Un oggetto di contesto, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="c0c05-118">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="c0c05-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c0c05-119">-Name</span></span>
<span data-ttu-id="c0c05-120">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="c0c05-120">The name of the context</span></span>

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

### <span data-ttu-id="c0c05-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0c05-121">-PassThru</span></span>
<span data-ttu-id="c0c05-122">Restituire il contesto rimosso</span><span class="sxs-lookup"><span data-stu-id="c0c05-122">Return the removed context</span></span>

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

### <span data-ttu-id="c0c05-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="c0c05-123">-Scope</span></span>
<span data-ttu-id="c0c05-124">Determina l'ambito delle modifiche di contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente</span><span class="sxs-lookup"><span data-stu-id="c0c05-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="c0c05-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0c05-125">-Confirm</span></span>
<span data-ttu-id="c0c05-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0c05-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0c05-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0c05-127">-WhatIf</span></span>
<span data-ttu-id="c0c05-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0c05-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0c05-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0c05-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0c05-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c05-130">CommonParameters</span></span>
<span data-ttu-id="c0c05-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0c05-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c05-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0c05-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c05-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="c0c05-133">INPUTS</span></span>

### <span data-ttu-id="c0c05-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="c0c05-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="c0c05-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0c05-135">OUTPUTS</span></span>

### <span data-ttu-id="c0c05-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="c0c05-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="c0c05-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="c0c05-137">NOTES</span></span>

## <span data-ttu-id="c0c05-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0c05-138">RELATED LINKS</span></span>
