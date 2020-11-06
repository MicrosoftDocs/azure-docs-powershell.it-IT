---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/rename-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: aea1fac4450a8625eb3d31e9f951a465344a3bd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514932"
---
# <span data-ttu-id="ca21e-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="ca21e-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="ca21e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca21e-102">SYNOPSIS</span></span>
<span data-ttu-id="ca21e-103">Rinominare un contesto Azure.</span><span class="sxs-lookup"><span data-stu-id="ca21e-103">Rename an Azure context.</span></span>  <span data-ttu-id="ca21e-104">Per impostazione predefinita, i contesti sono denominati dall'account utente e dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ca21e-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca21e-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca21e-105">SYNTAX</span></span>

### <span data-ttu-id="ca21e-106">RenameByInputObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ca21e-106">RenameByInputObject (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="ca21e-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="ca21e-107">RenameByName</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="ca21e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca21e-108">DESCRIPTION</span></span>
<span data-ttu-id="ca21e-109">Rinominare un contesto Azure.</span><span class="sxs-lookup"><span data-stu-id="ca21e-109">Rename an Azure context.</span></span>  <span data-ttu-id="ca21e-110">Per impostazione predefinita, i contesti sono denominati dall'account utente e dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ca21e-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="ca21e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca21e-111">EXAMPLES</span></span>

### <span data-ttu-id="ca21e-112">Rinominare un contesto usando i parametri denominati</span><span class="sxs-lookup"><span data-stu-id="ca21e-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="ca21e-113">Rinominare il contesto " user1@contoso.org con" con l'abbonamento "12345-6789-2345-3567890" in "lavoro".</span><span class="sxs-lookup"><span data-stu-id="ca21e-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="ca21e-114">Dopo questo comando, sarai in grado di scegliere come destinazione il contesto usando "Select-AzureRmContext work".</span><span class="sxs-lookup"><span data-stu-id="ca21e-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="ca21e-115">Tieni presente che puoi eseguire la tabulazione dei valori per "SourceName" usando la scheda completamento.</span><span class="sxs-lookup"><span data-stu-id="ca21e-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="ca21e-116">Rinominare un contesto usando i parametri posizionali</span><span class="sxs-lookup"><span data-stu-id="ca21e-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="ca21e-117">Rinominare il contesto denominato "contesto personale" in "lavoro".</span><span class="sxs-lookup"><span data-stu-id="ca21e-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="ca21e-118">Dopo questo comando, sarai in grado di indirizzare il contesto usando Select-AzureRmContext lavoro</span><span class="sxs-lookup"><span data-stu-id="ca21e-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="ca21e-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca21e-119">PARAMETERS</span></span>

### <span data-ttu-id="ca21e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca21e-120">-DefaultProfile</span></span>
<span data-ttu-id="ca21e-121">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ca21e-121">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca21e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ca21e-122">-Force</span></span>
<span data-ttu-id="ca21e-123">Rinominare il contesto anche se il contesto di destinazione esiste già</span><span class="sxs-lookup"><span data-stu-id="ca21e-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="ca21e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca21e-124">-InputObject</span></span>
<span data-ttu-id="ca21e-125">Oggetto context, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="ca21e-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: RenameByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca21e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca21e-126">-PassThru</span></span>
<span data-ttu-id="ca21e-127">Restituisce il contesto rinominato.</span><span class="sxs-lookup"><span data-stu-id="ca21e-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="ca21e-128">-Ambito</span><span class="sxs-lookup"><span data-stu-id="ca21e-128">-Scope</span></span>
<span data-ttu-id="ca21e-129">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente</span><span class="sxs-lookup"><span data-stu-id="ca21e-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="ca21e-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="ca21e-130">-SourceName</span></span>
<span data-ttu-id="ca21e-131">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="ca21e-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RenameByName
Aliases:
Accepted values: Default

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca21e-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="ca21e-132">-TargetName</span></span>
<span data-ttu-id="ca21e-133">Nuovo nome del contesto</span><span class="sxs-lookup"><span data-stu-id="ca21e-133">The new name of the context</span></span>

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

### <span data-ttu-id="ca21e-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca21e-134">-Confirm</span></span>
<span data-ttu-id="ca21e-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca21e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca21e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca21e-136">-WhatIf</span></span>
<span data-ttu-id="ca21e-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca21e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca21e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca21e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca21e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca21e-139">CommonParameters</span></span>
<span data-ttu-id="ca21e-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca21e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca21e-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca21e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca21e-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca21e-142">INPUTS</span></span>

### <span data-ttu-id="ca21e-143">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ca21e-143">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="ca21e-144">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ca21e-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ca21e-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca21e-145">OUTPUTS</span></span>

### <span data-ttu-id="ca21e-146">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ca21e-146">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="ca21e-147">Note</span><span class="sxs-lookup"><span data-stu-id="ca21e-147">NOTES</span></span>

## <span data-ttu-id="ca21e-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca21e-148">RELATED LINKS</span></span>
