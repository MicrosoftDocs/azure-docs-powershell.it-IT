---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
ms.openlocfilehash: eccb0ce5a9a92eae956c11273bf6397f20473e39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953005"
---
# <span data-ttu-id="34f65-101">Update-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="34f65-101">Update-AzSentinelBookmark</span></span>

## <span data-ttu-id="34f65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34f65-102">SYNOPSIS</span></span>
<span data-ttu-id="34f65-103">Aggiornare un segnalibro.</span><span class="sxs-lookup"><span data-stu-id="34f65-103">Update a Bookmark.</span></span>

## <span data-ttu-id="34f65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34f65-104">SYNTAX</span></span>

### <span data-ttu-id="34f65-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="34f65-105">BookmarkId.</span></span> <span data-ttu-id="34f65-106">(Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="34f65-106">(Default)</span></span>
```
Update-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DisplayName <String>] [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] [-Query <String>]
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34f65-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="34f65-107">InputObject</span></span>
```
Update-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34f65-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="34f65-108">ResourceId</span></span>
```
Update-AzSentinelBookmark -ResourceId <String> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34f65-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="34f65-109">DESCRIPTION</span></span>
<span data-ttu-id="34f65-110">Il cmdlet **Update-AzSentinelBookmark aggiorna** il segnalibro nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="34f65-110">The **Update-AzSentinelBookmark** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="34f65-111">È possibile passare un **oggetto Bookmark** come parametro o usando l'operatore pipeline oppure in alternativa è possibile specificare i parametri *BookmarkId* obbligatori.</span><span class="sxs-lookup"><span data-stu-id="34f65-111">You can pass an **Bookmark** object as a parameter or by using the pipeline operator, or alternatively you can specify the required *BookmarkId* parameters.</span></span>
<span data-ttu-id="34f65-112">È possibile usare il *parametro Confirm* $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="34f65-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="34f65-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34f65-113">EXAMPLES</span></span>

### <span data-ttu-id="34f65-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="34f65-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId" -Notes "Found something interesting"
```

<span data-ttu-id="34f65-115">Il comando aggiorna il segnalibro impostando la *proprietà* Note.</span><span class="sxs-lookup"><span data-stu-id="34f65-115">The command updates the Bookmark by setting the *Notes* property.</span></span>  <span data-ttu-id="34f65-116">Tutte le altre proprezze rimangono uguali.</span><span class="sxs-lookup"><span data-stu-id="34f65-116">All other propreties stay the same.</span></span>

### <span data-ttu-id="34f65-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="34f65-117">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId"
PS C:\> $Bookmark | Set-AzSentinelBookmark -Notes "Found something interesting"
```

<span data-ttu-id="34f65-118">Il primo comando recupera il segnalibro in base *a BookmarkId* dall'area di lavoro specificata e quindi lo archivia nella $Bookmark variabile.</span><span class="sxs-lookup"><span data-stu-id="34f65-118">The first command gets the Bookmark by *BookmarkId* from the specified workspace, and then stores it in the $Bookmark variable.</span></span>
<span data-ttu-id="34f65-119">Il secondo comando aggiorna la proprietà Note.</span><span class="sxs-lookup"><span data-stu-id="34f65-119">The second command updates the Notes property.</span></span>   <span data-ttu-id="34f65-120">Tutte le altre proprezze rimangono uguali.</span><span class="sxs-lookup"><span data-stu-id="34f65-120">All other propreties stay the same.</span></span>

## <span data-ttu-id="34f65-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34f65-121">PARAMETERS</span></span>

### <span data-ttu-id="34f65-122">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="34f65-122">-BookmarkId</span></span>
<span data-ttu-id="34f65-123">Id segnalibro</span><span class="sxs-lookup"><span data-stu-id="34f65-123">Bookmark Id,</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId., ParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f65-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f65-124">-DefaultProfile</span></span>
<span data-ttu-id="34f65-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34f65-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f65-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="34f65-126">-DisplayName</span></span>
<span data-ttu-id="34f65-127">Nome visualizzato regola segnalibro.</span><span class="sxs-lookup"><span data-stu-id="34f65-127">Bookmark Rule Display Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f65-128">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="34f65-128">-IncidentInfo</span></span>
<span data-ttu-id="34f65-129">Informazioni evento imprevisto segnalibro.</span><span class="sxs-lookup"><span data-stu-id="34f65-129">Bookmark Incident Info.</span></span>

```yaml
Type: PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34f65-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34f65-130">-InputObject</span></span>
<span data-ttu-id="34f65-131">InputObject.</span><span class="sxs-lookup"><span data-stu-id="34f65-131">InputObject.</span></span>

```yaml
Type: PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34f65-132">-Label</span><span class="sxs-lookup"><span data-stu-id="34f65-132">-Label</span></span>
<span data-ttu-id="34f65-133">Etichette degli eventi.</span><span class="sxs-lookup"><span data-stu-id="34f65-133">Incident Labels.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f65-134">-Note</span><span class="sxs-lookup"><span data-stu-id="34f65-134">-Notes</span></span>
<span data-ttu-id="34f65-135">Aggiungere segnalibri alle note.</span><span class="sxs-lookup"><span data-stu-id="34f65-135">Bookmark Notes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f65-136">-Query</span><span class="sxs-lookup"><span data-stu-id="34f65-136">-Query</span></span>
<span data-ttu-id="34f65-137">Query segnalibro.</span><span class="sxs-lookup"><span data-stu-id="34f65-137">Bookmark Query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f65-138">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="34f65-138">-QueryResult</span></span>
<span data-ttu-id="34f65-139">Risultato della query segnalibro.</span><span class="sxs-lookup"><span data-stu-id="34f65-139">Bookmark Query Result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f65-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34f65-140">-ResourceGroupName</span></span>
<span data-ttu-id="34f65-141">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="34f65-141">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f65-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34f65-142">-ResourceId</span></span>
<span data-ttu-id="34f65-143">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="34f65-143">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34f65-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="34f65-144">-WorkspaceName</span></span>
<span data-ttu-id="34f65-145">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="34f65-145">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f65-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34f65-146">-Confirm</span></span>
<span data-ttu-id="34f65-147">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34f65-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f65-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34f65-148">-WhatIf</span></span>
<span data-ttu-id="34f65-149">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34f65-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34f65-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34f65-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f65-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f65-151">CommonParameters</span></span>
<span data-ttu-id="34f65-152">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34f65-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f65-153">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34f65-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f65-154">INPUT</span><span class="sxs-lookup"><span data-stu-id="34f65-154">INPUTS</span></span>

### <span data-ttu-id="34f65-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="34f65-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

### <span data-ttu-id="34f65-156">System.String</span><span class="sxs-lookup"><span data-stu-id="34f65-156">System.String</span></span>

### <span data-ttu-id="34f65-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="34f65-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>

## <span data-ttu-id="34f65-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34f65-158">OUTPUTS</span></span>

### <span data-ttu-id="34f65-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="34f65-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

## <span data-ttu-id="34f65-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="34f65-160">NOTES</span></span>

## <span data-ttu-id="34f65-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34f65-161">RELATED LINKS</span></span>
