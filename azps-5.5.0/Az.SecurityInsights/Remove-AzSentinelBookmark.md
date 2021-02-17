---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
ms.openlocfilehash: 544c019fd52c0cb5723cbeafb5a82df072ac284e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191207"
---
# <span data-ttu-id="769b6-101">Remove-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="769b6-101">Remove-AzSentinelBookmark</span></span>

## <span data-ttu-id="769b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="769b6-102">SYNOPSIS</span></span>
<span data-ttu-id="769b6-103">Eliminare un segnalibro.</span><span class="sxs-lookup"><span data-stu-id="769b6-103">Delete a Bookmark.</span></span>

## <span data-ttu-id="769b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="769b6-104">SYNTAX</span></span>

### <span data-ttu-id="769b6-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="769b6-105">BookmarkId.</span></span> <span data-ttu-id="769b6-106">(Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="769b6-106">(Default)</span></span>
```
Remove-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="769b6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="769b6-107">InputObject</span></span>
```
Remove-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="769b6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="769b6-108">DESCRIPTION</span></span>
<span data-ttu-id="769b6-109">Il cmdlet **Remove-AzSentinelBookmark** elimina definitivamente un segnalibro da un'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="769b6-109">The **Remove-AzSentinelBookmark** cmdlet permanently deletes a Bookmark from a specified workspace.</span></span>
<span data-ttu-id="769b6-110">È possibile passare un **oggetto Bookmark** usando l'operatore pipeline oppure è possibile specificare i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="769b6-110">You can pass an **Bookmark** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="769b6-111">È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="769b6-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="769b6-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="769b6-112">EXAMPLES</span></span>

### <span data-ttu-id="769b6-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="769b6-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="769b6-114">Questo comando rimuove il segnalibro dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="769b6-114">This command removes the Bookmark from the workspace.</span></span>

## <span data-ttu-id="769b6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="769b6-115">PARAMETERS</span></span>

### <span data-ttu-id="769b6-116">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="769b6-116">-BookmarkId</span></span>
<span data-ttu-id="769b6-117">Id segnalibro</span><span class="sxs-lookup"><span data-stu-id="769b6-117">Bookmark Id,</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="769b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="769b6-118">-DefaultProfile</span></span>
<span data-ttu-id="769b6-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="769b6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="769b6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="769b6-120">-InputObject</span></span>
<span data-ttu-id="769b6-121">InputObject.</span><span class="sxs-lookup"><span data-stu-id="769b6-121">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="769b6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="769b6-122">-PassThru</span></span>
<span data-ttu-id="769b6-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="769b6-123">PassThru</span></span>

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

### <span data-ttu-id="769b6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="769b6-124">-ResourceGroupName</span></span>
<span data-ttu-id="769b6-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="769b6-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="769b6-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="769b6-126">-WorkspaceName</span></span>
<span data-ttu-id="769b6-127">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="769b6-127">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="769b6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="769b6-128">-Confirm</span></span>
<span data-ttu-id="769b6-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="769b6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="769b6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="769b6-130">-WhatIf</span></span>
<span data-ttu-id="769b6-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="769b6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="769b6-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="769b6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="769b6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="769b6-133">CommonParameters</span></span>
<span data-ttu-id="769b6-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="769b6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="769b6-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="769b6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="769b6-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="769b6-136">INPUTS</span></span>

### <span data-ttu-id="769b6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="769b6-137">System.String</span></span>
### <span data-ttu-id="769b6-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="769b6-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="769b6-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="769b6-139">OUTPUTS</span></span>

### <span data-ttu-id="769b6-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="769b6-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="769b6-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="769b6-141">NOTES</span></span>

## <span data-ttu-id="769b6-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="769b6-142">RELATED LINKS</span></span>
