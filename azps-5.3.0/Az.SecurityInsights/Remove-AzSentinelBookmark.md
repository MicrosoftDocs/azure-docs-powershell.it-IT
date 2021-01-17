---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
ms.openlocfilehash: 544c019fd52c0cb5723cbeafb5a82df072ac284e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486168"
---
# <span data-ttu-id="446c8-101">Remove-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="446c8-101">Remove-AzSentinelBookmark</span></span>

## <span data-ttu-id="446c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="446c8-102">SYNOPSIS</span></span>
<span data-ttu-id="446c8-103">Eliminare un segnalibro.</span><span class="sxs-lookup"><span data-stu-id="446c8-103">Delete a Bookmark.</span></span>

## <span data-ttu-id="446c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="446c8-104">SYNTAX</span></span>

### <span data-ttu-id="446c8-105">BookmarkID.</span><span class="sxs-lookup"><span data-stu-id="446c8-105">BookmarkId.</span></span> <span data-ttu-id="446c8-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="446c8-106">(Default)</span></span>
```
Remove-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="446c8-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="446c8-107">InputObject</span></span>
```
Remove-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="446c8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="446c8-108">DESCRIPTION</span></span>
<span data-ttu-id="446c8-109">Il cmdlet **Remove-AzSentinelBookmark** Elimina definitivamente un segnalibro da un'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="446c8-109">The **Remove-AzSentinelBookmark** cmdlet permanently deletes a Bookmark from a specified workspace.</span></span>
<span data-ttu-id="446c8-110">Puoi passare un oggetto **Bookmark** usando l'operatore pipeline o in alternativa puoi specificare i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="446c8-110">You can pass an **Bookmark** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="446c8-111">Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="446c8-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="446c8-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="446c8-112">EXAMPLES</span></span>

### <span data-ttu-id="446c8-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="446c8-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="446c8-114">Questo comando rimuove il segnalibro dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="446c8-114">This command removes the Bookmark from the workspace.</span></span>

## <span data-ttu-id="446c8-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="446c8-115">PARAMETERS</span></span>

### <span data-ttu-id="446c8-116">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="446c8-116">-BookmarkId</span></span>
<span data-ttu-id="446c8-117">ID segnalibro</span><span class="sxs-lookup"><span data-stu-id="446c8-117">Bookmark Id,</span></span>

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

### <span data-ttu-id="446c8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="446c8-118">-DefaultProfile</span></span>
<span data-ttu-id="446c8-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="446c8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="446c8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="446c8-120">-InputObject</span></span>
<span data-ttu-id="446c8-121">InputObject.</span><span class="sxs-lookup"><span data-stu-id="446c8-121">InputObject.</span></span>

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

### <span data-ttu-id="446c8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="446c8-122">-PassThru</span></span>
<span data-ttu-id="446c8-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="446c8-123">PassThru</span></span>

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

### <span data-ttu-id="446c8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="446c8-124">-ResourceGroupName</span></span>
<span data-ttu-id="446c8-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="446c8-125">Resource group name.</span></span>

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

### <span data-ttu-id="446c8-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="446c8-126">-WorkspaceName</span></span>
<span data-ttu-id="446c8-127">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="446c8-127">Workspace Name.</span></span>

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

### <span data-ttu-id="446c8-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="446c8-128">-Confirm</span></span>
<span data-ttu-id="446c8-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="446c8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="446c8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="446c8-130">-WhatIf</span></span>
<span data-ttu-id="446c8-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="446c8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="446c8-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="446c8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="446c8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="446c8-133">CommonParameters</span></span>
<span data-ttu-id="446c8-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="446c8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="446c8-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="446c8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="446c8-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="446c8-136">INPUTS</span></span>

### <span data-ttu-id="446c8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="446c8-137">System.String</span></span>
### <span data-ttu-id="446c8-138">Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="446c8-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="446c8-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="446c8-139">OUTPUTS</span></span>

### <span data-ttu-id="446c8-140">Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="446c8-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="446c8-141">Note</span><span class="sxs-lookup"><span data-stu-id="446c8-141">NOTES</span></span>

## <span data-ttu-id="446c8-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="446c8-142">RELATED LINKS</span></span>
