---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
ms.openlocfilehash: ebc0ffd78f653276e66b85d263db41803a48c356
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486152"
---
# <span data-ttu-id="c1613-101">Update-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="c1613-101">Update-AzSentinelBookmark</span></span>

## <span data-ttu-id="c1613-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1613-102">SYNOPSIS</span></span>
<span data-ttu-id="c1613-103">Aggiornare un segnalibro.</span><span class="sxs-lookup"><span data-stu-id="c1613-103">Update a Bookmark.</span></span>

## <span data-ttu-id="c1613-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1613-104">SYNTAX</span></span>

### <span data-ttu-id="c1613-105">BookmarkID.</span><span class="sxs-lookup"><span data-stu-id="c1613-105">BookmarkId.</span></span> <span data-ttu-id="c1613-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="c1613-106">(Default)</span></span>
```
Update-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DisplayName <String>] [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] [-Query <String>]
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1613-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c1613-107">InputObject</span></span>
```
Update-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1613-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1613-108">ResourceId</span></span>
```
Update-AzSentinelBookmark -ResourceId <String> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1613-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1613-109">DESCRIPTION</span></span>
<span data-ttu-id="c1613-110">Il cmdlet **Update-AzSentinelBookmark** aggiorna il segnalibro nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="c1613-110">The **Update-AzSentinelBookmark** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="c1613-111">Puoi passare un oggetto **Bookmark** come parametro o usando l'operatore pipeline o in alternativa puoi specificare i parametri *BookmarkID* necessari.</span><span class="sxs-lookup"><span data-stu-id="c1613-111">You can pass an **Bookmark** object as a parameter or by using the pipeline operator, or alternatively you can specify the required *BookmarkId* parameters.</span></span>
<span data-ttu-id="c1613-112">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="c1613-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="c1613-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1613-113">EXAMPLES</span></span>

### <span data-ttu-id="c1613-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c1613-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId" -Notes "Found something interesting"
```

<span data-ttu-id="c1613-115">Il comando Aggiorna il segnalibro impostando la proprietà *Note* .</span><span class="sxs-lookup"><span data-stu-id="c1613-115">The command updates the Bookmark by setting the *Notes* property.</span></span>  <span data-ttu-id="c1613-116">Tutti gli altri propreties rimangono invariati.</span><span class="sxs-lookup"><span data-stu-id="c1613-116">All other propreties stay the same.</span></span>

### <span data-ttu-id="c1613-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c1613-117">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId"
PS C:\> $Bookmark | Set-AzSentinelBookmark -Notes "Found something interesting"
```

<span data-ttu-id="c1613-118">Il primo comando ottiene il segnalibro in base a *BookmarkID* dall'area di lavoro specificata e lo archivia nella variabile $Bookmark.</span><span class="sxs-lookup"><span data-stu-id="c1613-118">The first command gets the Bookmark by *BookmarkId* from the specified workspace, and then stores it in the $Bookmark variable.</span></span>
<span data-ttu-id="c1613-119">Il secondo comando Aggiorna la proprietà note.</span><span class="sxs-lookup"><span data-stu-id="c1613-119">The second command updates the Notes property.</span></span>   <span data-ttu-id="c1613-120">Tutti gli altri propreties rimangono invariati.</span><span class="sxs-lookup"><span data-stu-id="c1613-120">All other propreties stay the same.</span></span>

## <span data-ttu-id="c1613-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1613-121">PARAMETERS</span></span>

### <span data-ttu-id="c1613-122">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="c1613-122">-BookmarkId</span></span>
<span data-ttu-id="c1613-123">ID segnalibro</span><span class="sxs-lookup"><span data-stu-id="c1613-123">Bookmark Id,</span></span>

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

### <span data-ttu-id="c1613-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1613-124">-DefaultProfile</span></span>
<span data-ttu-id="c1613-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1613-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1613-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c1613-126">-DisplayName</span></span>
<span data-ttu-id="c1613-127">Nome visualizzato della regola del segnalibro.</span><span class="sxs-lookup"><span data-stu-id="c1613-127">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="c1613-128">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="c1613-128">-IncidentInfo</span></span>
<span data-ttu-id="c1613-129">Informazioni sull'incidente del segnalibro.</span><span class="sxs-lookup"><span data-stu-id="c1613-129">Bookmark Incident Info.</span></span>

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

### <span data-ttu-id="c1613-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1613-130">-InputObject</span></span>
<span data-ttu-id="c1613-131">InputObject.</span><span class="sxs-lookup"><span data-stu-id="c1613-131">InputObject.</span></span>

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

### <span data-ttu-id="c1613-132">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="c1613-132">-Label</span></span>
<span data-ttu-id="c1613-133">Etichette Incident.</span><span class="sxs-lookup"><span data-stu-id="c1613-133">Incident Labels.</span></span>

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

### <span data-ttu-id="c1613-134">-Note</span><span class="sxs-lookup"><span data-stu-id="c1613-134">-Notes</span></span>
<span data-ttu-id="c1613-135">Note del segnalibro.</span><span class="sxs-lookup"><span data-stu-id="c1613-135">Bookmark Notes.</span></span>

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

### <span data-ttu-id="c1613-136">-Query</span><span class="sxs-lookup"><span data-stu-id="c1613-136">-Query</span></span>
<span data-ttu-id="c1613-137">Query di segnalibro.</span><span class="sxs-lookup"><span data-stu-id="c1613-137">Bookmark Query.</span></span>

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

### <span data-ttu-id="c1613-138">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="c1613-138">-QueryResult</span></span>
<span data-ttu-id="c1613-139">Risultato della query del segnalibro.</span><span class="sxs-lookup"><span data-stu-id="c1613-139">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="c1613-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1613-140">-ResourceGroupName</span></span>
<span data-ttu-id="c1613-141">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c1613-141">Resource group name.</span></span>

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

### <span data-ttu-id="c1613-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1613-142">-ResourceId</span></span>
<span data-ttu-id="c1613-143">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c1613-143">Resource Id.</span></span>

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

### <span data-ttu-id="c1613-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c1613-144">-WorkspaceName</span></span>
<span data-ttu-id="c1613-145">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c1613-145">Workspace Name.</span></span>

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

### <span data-ttu-id="c1613-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c1613-146">-Confirm</span></span>
<span data-ttu-id="c1613-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1613-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1613-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1613-148">-WhatIf</span></span>
<span data-ttu-id="c1613-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1613-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1613-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1613-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1613-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1613-151">CommonParameters</span></span>
<span data-ttu-id="c1613-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1613-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1613-153">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1613-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1613-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1613-154">INPUTS</span></span>

### <span data-ttu-id="c1613-155">Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="c1613-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

### <span data-ttu-id="c1613-156">System. String</span><span class="sxs-lookup"><span data-stu-id="c1613-156">System.String</span></span>

### <span data-ttu-id="c1613-157">Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="c1613-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>

## <span data-ttu-id="c1613-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1613-158">OUTPUTS</span></span>

### <span data-ttu-id="c1613-159">Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="c1613-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

## <span data-ttu-id="c1613-160">Note</span><span class="sxs-lookup"><span data-stu-id="c1613-160">NOTES</span></span>

## <span data-ttu-id="c1613-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1613-161">RELATED LINKS</span></span>
