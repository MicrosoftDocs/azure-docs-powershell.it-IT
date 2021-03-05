---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
ms.openlocfilehash: 5093f924f87f146550b13e3858f9a93b3f193ca0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005661"
---
# <span data-ttu-id="5ff87-101">Get-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="5ff87-101">Get-AzSentinelBookmark</span></span>

## <span data-ttu-id="5ff87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ff87-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff87-103">Ottenere un segnalibro.</span><span class="sxs-lookup"><span data-stu-id="5ff87-103">Get a Bookmark.</span></span>

## <span data-ttu-id="5ff87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ff87-104">SYNTAX</span></span>

### <span data-ttu-id="5ff87-105">WorkspaceScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5ff87-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ff87-106">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="5ff87-106">BookmarkId.</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ff87-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ff87-107">ResourceId</span></span>
```
Get-AzSentinelBookmark -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ff87-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5ff87-108">DESCRIPTION</span></span>
<span data-ttu-id="5ff87-109">Il **cmdlet Get-AzSentinelBookmark ottiene** un segnalibro dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="5ff87-109">The **Get-AzSentinelBookmark** cmdlet gets a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="5ff87-110">Se si specifica il *parametro BookmarkId,* viene **restituito un** singolo oggetto Bookmark.</span><span class="sxs-lookup"><span data-stu-id="5ff87-110">If you specify the *BookmarkId* parameter, a single **Bookmark** object is returned.</span></span>
<span data-ttu-id="5ff87-111">Se non si specifica il parametro *BookmarkId,* verrà restituita una matrice contenente tutti i segnalibri nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="5ff87-111">If you do not specify the *BookmarkId* parameter, an array containing all of the Bookmarks in the specified workspace are returned.</span></span>
<span data-ttu-id="5ff87-112">È possibile usare **l'oggetto Segnalibro** per aggiornare il segnalibro, ad esempio per aggiungere note al **segnalibro.**</span><span class="sxs-lookup"><span data-stu-id="5ff87-112">You can use the **Bookmark** object to update the Bookmark, for example you can add Notes the **Bookmark**.</span></span>

## <span data-ttu-id="5ff87-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ff87-113">EXAMPLES</span></span>

### <span data-ttu-id="5ff87-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5ff87-114">Example 1</span></span>
```powershell
PS C:\> $Bookmarks = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="5ff87-115">Questo esempio recupera tutti i **segnalibri nell'area** di lavoro specificata e li archivia nella $Bookmarks variabile.</span><span class="sxs-lookup"><span data-stu-id="5ff87-115">This example gets all of the **Bookmarks** in the specified workspace, and then stores it in the $Bookmarks variable.</span></span>

### <span data-ttu-id="5ff87-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5ff87-116">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="5ff87-117">Questo esempio recupera un **segnalibro** nell'area di lavoro specificata e quindi lo archivia nella $Bookmark variabile.</span><span class="sxs-lookup"><span data-stu-id="5ff87-117">This example gets an **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="5ff87-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ff87-118">PARAMETERS</span></span>

### <span data-ttu-id="5ff87-119">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="5ff87-119">-BookmarkId</span></span>
<span data-ttu-id="5ff87-120">Id segnalibro</span><span class="sxs-lookup"><span data-stu-id="5ff87-120">Bookmark Id,</span></span>

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

### <span data-ttu-id="5ff87-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff87-121">-DefaultProfile</span></span>
<span data-ttu-id="5ff87-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ff87-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ff87-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ff87-123">-ResourceGroupName</span></span>
<span data-ttu-id="5ff87-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5ff87-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff87-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ff87-125">-ResourceId</span></span>
<span data-ttu-id="5ff87-126">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="5ff87-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff87-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5ff87-127">-WorkspaceName</span></span>
<span data-ttu-id="5ff87-128">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5ff87-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff87-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff87-129">CommonParameters</span></span>
<span data-ttu-id="5ff87-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ff87-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff87-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5ff87-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff87-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="5ff87-132">INPUTS</span></span>

### <span data-ttu-id="5ff87-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5ff87-133">System.String</span></span>
## <span data-ttu-id="5ff87-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ff87-134">OUTPUTS</span></span>

### <span data-ttu-id="5ff87-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="5ff87-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="5ff87-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="5ff87-136">NOTES</span></span>

## <span data-ttu-id="5ff87-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ff87-137">RELATED LINKS</span></span>
