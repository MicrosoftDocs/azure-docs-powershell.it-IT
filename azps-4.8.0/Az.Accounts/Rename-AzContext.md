---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 09c0faec1ab424ef1bfb10fec35dd59646e4711c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189869"
---
# <span data-ttu-id="1d0f0-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="1d0f0-101">Rename-AzContext</span></span>

## <span data-ttu-id="1d0f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d0f0-102">SYNOPSIS</span></span>
<span data-ttu-id="1d0f0-103">Rinominare un contesto Azure.</span><span class="sxs-lookup"><span data-stu-id="1d0f0-103">Rename an Azure context.</span></span>  <span data-ttu-id="1d0f0-104">Per impostazione predefinita, i contesti sono denominati dall'account utente e dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1d0f0-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="1d0f0-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d0f0-105">SYNTAX</span></span>

### <span data-ttu-id="1d0f0-106">RenameByInputObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1d0f0-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="1d0f0-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="1d0f0-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="1d0f0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d0f0-108">DESCRIPTION</span></span>
<span data-ttu-id="1d0f0-109">Rinominare un contesto Azure.</span><span class="sxs-lookup"><span data-stu-id="1d0f0-109">Rename an Azure context.</span></span>  <span data-ttu-id="1d0f0-110">Per impostazione predefinita, i contesti sono denominati dall'account utente e dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1d0f0-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="1d0f0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d0f0-111">EXAMPLES</span></span>

### <span data-ttu-id="1d0f0-112">Esempio 1: rinominare un contesto usando i parametri denominati</span><span class="sxs-lookup"><span data-stu-id="1d0f0-112">Example 1: Rename a context using named parameters</span></span>
```powershell
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="1d0f0-113">Rinominare il contesto " user1@contoso.org con" con l'abbonamento "12345-6789-2345-3567890" in "lavoro".</span><span class="sxs-lookup"><span data-stu-id="1d0f0-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="1d0f0-114">Dopo questo comando, sarai in grado di scegliere come destinazione il contesto usando "Select-AzContext work".</span><span class="sxs-lookup"><span data-stu-id="1d0f0-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="1d0f0-115">Tieni presente che puoi eseguire la tabulazione dei valori per "SourceName" usando la scheda completamento.</span><span class="sxs-lookup"><span data-stu-id="1d0f0-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="1d0f0-116">Esempio 2: rinominare un contesto usando i parametri posizionali</span><span class="sxs-lookup"><span data-stu-id="1d0f0-116">Example 2: Rename a context using positional parameters</span></span>
```powershell
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="1d0f0-117">Rinominare il contesto denominato "contesto personale" in "lavoro".</span><span class="sxs-lookup"><span data-stu-id="1d0f0-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="1d0f0-118">Dopo questo comando, sarai in grado di indirizzare il contesto usando Select-AzContext lavoro</span><span class="sxs-lookup"><span data-stu-id="1d0f0-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="1d0f0-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d0f0-119">PARAMETERS</span></span>

### <span data-ttu-id="1d0f0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d0f0-120">-DefaultProfile</span></span>
<span data-ttu-id="1d0f0-121">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1d0f0-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d0f0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1d0f0-122">-Force</span></span>
<span data-ttu-id="1d0f0-123">Rinominare il contesto anche se il contesto di destinazione esiste già</span><span class="sxs-lookup"><span data-stu-id="1d0f0-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="1d0f0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d0f0-124">-InputObject</span></span>
<span data-ttu-id="1d0f0-125">Oggetto context, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="1d0f0-125">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="1d0f0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d0f0-126">-PassThru</span></span>
<span data-ttu-id="1d0f0-127">Restituisce il contesto rinominato.</span><span class="sxs-lookup"><span data-stu-id="1d0f0-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="1d0f0-128">-Ambito</span><span class="sxs-lookup"><span data-stu-id="1d0f0-128">-Scope</span></span>
<span data-ttu-id="1d0f0-129">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente</span><span class="sxs-lookup"><span data-stu-id="1d0f0-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="1d0f0-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="1d0f0-130">-SourceName</span></span>
<span data-ttu-id="1d0f0-131">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="1d0f0-131">The name of the context</span></span>

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

### <span data-ttu-id="1d0f0-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="1d0f0-132">-TargetName</span></span>
<span data-ttu-id="1d0f0-133">Nuovo nome del contesto</span><span class="sxs-lookup"><span data-stu-id="1d0f0-133">The new name of the context</span></span>

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

### <span data-ttu-id="1d0f0-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1d0f0-134">-Confirm</span></span>
<span data-ttu-id="1d0f0-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d0f0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d0f0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d0f0-136">-WhatIf</span></span>
<span data-ttu-id="1d0f0-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d0f0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d0f0-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d0f0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d0f0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d0f0-139">CommonParameters</span></span>
<span data-ttu-id="1d0f0-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d0f0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d0f0-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d0f0-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d0f0-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d0f0-142">INPUTS</span></span>

### <span data-ttu-id="1d0f0-143">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="1d0f0-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="1d0f0-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d0f0-144">OUTPUTS</span></span>

### <span data-ttu-id="1d0f0-145">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="1d0f0-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="1d0f0-146">Note</span><span class="sxs-lookup"><span data-stu-id="1d0f0-146">NOTES</span></span>

## <span data-ttu-id="1d0f0-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d0f0-147">RELATED LINKS</span></span>
