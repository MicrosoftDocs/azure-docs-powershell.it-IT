---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 09c0faec1ab424ef1bfb10fec35dd59646e4711c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190423"
---
# <span data-ttu-id="fe0b5-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="fe0b5-101">Rename-AzContext</span></span>

## <span data-ttu-id="fe0b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe0b5-102">SYNOPSIS</span></span>
<span data-ttu-id="fe0b5-103">Rinominare un contesto di Azure.</span><span class="sxs-lookup"><span data-stu-id="fe0b5-103">Rename an Azure context.</span></span>  <span data-ttu-id="fe0b5-104">Per impostazione predefinita, i contesti sono denominati in base all'account utente e all'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fe0b5-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="fe0b5-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe0b5-105">SYNTAX</span></span>

### <span data-ttu-id="fe0b5-106">RenameByInputObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fe0b5-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="fe0b5-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="fe0b5-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="fe0b5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fe0b5-108">DESCRIPTION</span></span>
<span data-ttu-id="fe0b5-109">Rinominare un contesto di Azure.</span><span class="sxs-lookup"><span data-stu-id="fe0b5-109">Rename an Azure context.</span></span>  <span data-ttu-id="fe0b5-110">Per impostazione predefinita, i contesti sono denominati in base all'account utente e all'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fe0b5-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="fe0b5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe0b5-111">EXAMPLES</span></span>

### <span data-ttu-id="fe0b5-112">Esempio 1: Rinominare un contesto usando parametri denominati</span><span class="sxs-lookup"><span data-stu-id="fe0b5-112">Example 1: Rename a context using named parameters</span></span>
```powershell
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="fe0b5-113">Rinominare il contesto per ' con abbonamento user1@contoso.org '12345-6789-2345-3567890' in 'Lavoro'.</span><span class="sxs-lookup"><span data-stu-id="fe0b5-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="fe0b5-114">Dopo questo comando sarà possibile scegliere come destinazione il contesto usando 'Select-AzContext Work'.</span><span class="sxs-lookup"><span data-stu-id="fe0b5-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="fe0b5-115">Si noti che è possibile scorrere i valori di "SourceName" usando il completamento della tabulazione.</span><span class="sxs-lookup"><span data-stu-id="fe0b5-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="fe0b5-116">Esempio 2: Rinominare un contesto usando parametri posizionali</span><span class="sxs-lookup"><span data-stu-id="fe0b5-116">Example 2: Rename a context using positional parameters</span></span>
```powershell
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="fe0b5-117">Rinominare il contesto denominato "Il mio contesto" in "Lavoro".</span><span class="sxs-lookup"><span data-stu-id="fe0b5-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="fe0b5-118">Dopo questo comando sarà possibile scegliere come destinazione il contesto usando Select-AzContext lavoro</span><span class="sxs-lookup"><span data-stu-id="fe0b5-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="fe0b5-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe0b5-119">PARAMETERS</span></span>

### <span data-ttu-id="fe0b5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe0b5-120">-DefaultProfile</span></span>
<span data-ttu-id="fe0b5-121">Le credenziali, il tenant e la sottoscrizione usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fe0b5-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe0b5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="fe0b5-122">-Force</span></span>
<span data-ttu-id="fe0b5-123">Rinominare il contesto anche se il contesto di destinazione esiste già</span><span class="sxs-lookup"><span data-stu-id="fe0b5-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="fe0b5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe0b5-124">-InputObject</span></span>
<span data-ttu-id="fe0b5-125">Un oggetto di contesto, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="fe0b5-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RenameByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe0b5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe0b5-126">-PassThru</span></span>
<span data-ttu-id="fe0b5-127">Restituisce il contesto rinominato.</span><span class="sxs-lookup"><span data-stu-id="fe0b5-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="fe0b5-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="fe0b5-128">-Scope</span></span>
<span data-ttu-id="fe0b5-129">Determina l'ambito delle modifiche di contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente</span><span class="sxs-lookup"><span data-stu-id="fe0b5-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="fe0b5-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="fe0b5-130">-SourceName</span></span>
<span data-ttu-id="fe0b5-131">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="fe0b5-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RenameByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe0b5-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="fe0b5-132">-TargetName</span></span>
<span data-ttu-id="fe0b5-133">Il nuovo nome del contesto</span><span class="sxs-lookup"><span data-stu-id="fe0b5-133">The new name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe0b5-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe0b5-134">-Confirm</span></span>
<span data-ttu-id="fe0b5-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe0b5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe0b5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe0b5-136">-WhatIf</span></span>
<span data-ttu-id="fe0b5-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe0b5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe0b5-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe0b5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe0b5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe0b5-139">CommonParameters</span></span>
<span data-ttu-id="fe0b5-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe0b5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe0b5-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe0b5-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe0b5-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="fe0b5-142">INPUTS</span></span>

### <span data-ttu-id="fe0b5-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="fe0b5-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="fe0b5-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe0b5-144">OUTPUTS</span></span>

### <span data-ttu-id="fe0b5-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="fe0b5-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="fe0b5-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="fe0b5-146">NOTES</span></span>

## <span data-ttu-id="fe0b5-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe0b5-147">RELATED LINKS</span></span>
