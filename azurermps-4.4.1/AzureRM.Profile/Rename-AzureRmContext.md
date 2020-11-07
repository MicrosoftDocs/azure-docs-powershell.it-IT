---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: 9c9c0c3c52f610c0bb2c0198e9995cf2804b2b24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688262"
---
# <span data-ttu-id="6628c-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="6628c-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="6628c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6628c-102">SYNOPSIS</span></span>
<span data-ttu-id="6628c-103">Rinominare un contesto Azure.</span><span class="sxs-lookup"><span data-stu-id="6628c-103">Rename an Azure context.</span></span>  <span data-ttu-id="6628c-104">Per impostazione predefinita, i contesti sono denominati dall'account utente e dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6628c-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6628c-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6628c-105">SYNTAX</span></span>

### <span data-ttu-id="6628c-106">Oggetto di input (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6628c-106">Input Object (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="6628c-107">Nome contesto</span><span class="sxs-lookup"><span data-stu-id="6628c-107">Context Name</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="6628c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6628c-108">DESCRIPTION</span></span>
<span data-ttu-id="6628c-109">Rinominare un contesto Azure.</span><span class="sxs-lookup"><span data-stu-id="6628c-109">Rename an Azure context.</span></span>  <span data-ttu-id="6628c-110">Per impostazione predefinita, i contesti sono denominati dall'account utente e dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6628c-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="6628c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6628c-111">EXAMPLES</span></span>

### <span data-ttu-id="6628c-112">Rinominare un contesto usando i parametri denominati</span><span class="sxs-lookup"><span data-stu-id="6628c-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="6628c-113">Rinominare il contesto " user1@contoso.org con" con l'abbonamento "12345-6789-2345-3567890" in "lavoro".</span><span class="sxs-lookup"><span data-stu-id="6628c-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="6628c-114">Dopo questo comando, sarai in grado di scegliere come destinazione il contesto usando "Select-AzureRmContext work".</span><span class="sxs-lookup"><span data-stu-id="6628c-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="6628c-115">Tieni presente che puoi eseguire la tabulazione dei valori per "SourceName" usando la scheda completamento.</span><span class="sxs-lookup"><span data-stu-id="6628c-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="6628c-116">Rinominare un contesto usando i parametri posizionali</span><span class="sxs-lookup"><span data-stu-id="6628c-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="6628c-117">Rinominare il contesto denominato "contesto personale" in "lavoro".</span><span class="sxs-lookup"><span data-stu-id="6628c-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="6628c-118">Dopo questo comando, sarai in grado di indirizzare il contesto usando Select-AzureRmContext lavoro</span><span class="sxs-lookup"><span data-stu-id="6628c-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="6628c-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6628c-119">PARAMETERS</span></span>

### <span data-ttu-id="6628c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6628c-120">-DefaultProfile</span></span>
<span data-ttu-id="6628c-121">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6628c-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6628c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="6628c-122">-Force</span></span>
<span data-ttu-id="6628c-123">Rinominare il contesto anche se il contesto di destinazione esiste già</span><span class="sxs-lookup"><span data-stu-id="6628c-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="6628c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6628c-124">-InputObject</span></span>
<span data-ttu-id="6628c-125">Oggetto context, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="6628c-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Input Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6628c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6628c-126">-PassThru</span></span>
<span data-ttu-id="6628c-127">Restituisce il contesto rinominato.</span><span class="sxs-lookup"><span data-stu-id="6628c-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="6628c-128">-Ambito</span><span class="sxs-lookup"><span data-stu-id="6628c-128">-Scope</span></span>
<span data-ttu-id="6628c-129">Determina l'ambito delle modifiche al contesto, ad esempio le modifiche apportate a wheher si applicano solo al processo cusrrent o a tutte le sessioni avviate dall'utente</span><span class="sxs-lookup"><span data-stu-id="6628c-129">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="6628c-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="6628c-130">-SourceName</span></span>
<span data-ttu-id="6628c-131">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="6628c-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Context Name
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6628c-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="6628c-132">-TargetName</span></span>
<span data-ttu-id="6628c-133">Nuovo nome del contesto</span><span class="sxs-lookup"><span data-stu-id="6628c-133">The new name of the context</span></span>

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

### <span data-ttu-id="6628c-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6628c-134">-Confirm</span></span>
<span data-ttu-id="6628c-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6628c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6628c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6628c-136">-WhatIf</span></span>
<span data-ttu-id="6628c-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6628c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6628c-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6628c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6628c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6628c-139">CommonParameters</span></span>
<span data-ttu-id="6628c-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6628c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6628c-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6628c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6628c-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6628c-142">INPUTS</span></span>

### <span data-ttu-id="6628c-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6628c-143">None</span></span>

## <span data-ttu-id="6628c-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6628c-144">OUTPUTS</span></span>

### <span data-ttu-id="6628c-145">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="6628c-145">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="6628c-146">Note</span><span class="sxs-lookup"><span data-stu-id="6628c-146">NOTES</span></span>

## <span data-ttu-id="6628c-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6628c-147">RELATED LINKS</span></span>

