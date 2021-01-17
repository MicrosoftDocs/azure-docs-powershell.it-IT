---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
ms.openlocfilehash: 53dfedcfe4e61deb5064b20134bf063921532aec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486216"
---
# <span data-ttu-id="5ead9-101">Get-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="5ead9-101">Get-AzSentinelBookmark</span></span>

## <span data-ttu-id="5ead9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ead9-102">SYNOPSIS</span></span>
<span data-ttu-id="5ead9-103">Ottenere un segnalibro.</span><span class="sxs-lookup"><span data-stu-id="5ead9-103">Get a Bookmark.</span></span>

## <span data-ttu-id="5ead9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ead9-104">SYNTAX</span></span>

### <span data-ttu-id="5ead9-105">WorkspaceScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5ead9-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ead9-106">BookmarkID.</span><span class="sxs-lookup"><span data-stu-id="5ead9-106">BookmarkId.</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ead9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ead9-107">ResourceId</span></span>
```
Get-AzSentinelBookmark -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ead9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ead9-108">DESCRIPTION</span></span>
<span data-ttu-id="5ead9-109">Il cmdlet **Get-AzSentinelBookmark** ottiene un segnalibro dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="5ead9-109">The **Get-AzSentinelBookmark** cmdlet gets a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="5ead9-110">Se specifichi il parametro *BookmarkID* , viene restituito un singolo oggetto **Bookmark** .</span><span class="sxs-lookup"><span data-stu-id="5ead9-110">If you specify the *BookmarkId* parameter, a single **Bookmark** object is returned.</span></span>
<span data-ttu-id="5ead9-111">Se non specifichi il parametro *BookmarkID* , viene restituita una matrice contenente tutti i segnalibri nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="5ead9-111">If you do not specify the *BookmarkId* parameter, an array containing all of the Bookmarks in the specified workspace are returned.</span></span>
<span data-ttu-id="5ead9-112">Puoi usare l'oggetto **Bookmark** per aggiornare il segnalibro, ad esempio puoi aggiungere note al **segnalibro**.</span><span class="sxs-lookup"><span data-stu-id="5ead9-112">You can use the **Bookmark** object to update the Bookmark, for example you can add Notes the **Bookmark**.</span></span>

## <span data-ttu-id="5ead9-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ead9-113">EXAMPLES</span></span>

### <span data-ttu-id="5ead9-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5ead9-114">Example 1</span></span>
```powershell
PS C:\> $Bookmarks = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="5ead9-115">Questo esempio recupera tutti i **segnalibri** nell'area di lavoro specificata e lo archivia nella variabile $Bookmarks.</span><span class="sxs-lookup"><span data-stu-id="5ead9-115">This example gets all of the **Bookmarks** in the specified workspace, and then stores it in the $Bookmarks variable.</span></span>

### <span data-ttu-id="5ead9-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5ead9-116">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="5ead9-117">Questo esempio ottiene un **segnalibro** nell'area di lavoro specificata e lo archivia nella variabile $Bookmark.</span><span class="sxs-lookup"><span data-stu-id="5ead9-117">This example gets an **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="5ead9-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ead9-118">PARAMETERS</span></span>

### <span data-ttu-id="5ead9-119">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="5ead9-119">-BookmarkId</span></span>
<span data-ttu-id="5ead9-120">ID segnalibro</span><span class="sxs-lookup"><span data-stu-id="5ead9-120">Bookmark Id,</span></span>

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

### <span data-ttu-id="5ead9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ead9-121">-DefaultProfile</span></span>
<span data-ttu-id="5ead9-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ead9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ead9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ead9-123">-ResourceGroupName</span></span>
<span data-ttu-id="5ead9-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5ead9-124">Resource group name.</span></span>

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

### <span data-ttu-id="5ead9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ead9-125">-ResourceId</span></span>
<span data-ttu-id="5ead9-126">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="5ead9-126">Resource Id.</span></span>

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

### <span data-ttu-id="5ead9-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5ead9-127">-WorkspaceName</span></span>
<span data-ttu-id="5ead9-128">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5ead9-128">Workspace Name.</span></span>

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

### <span data-ttu-id="5ead9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ead9-129">CommonParameters</span></span>
<span data-ttu-id="5ead9-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ead9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ead9-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ead9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ead9-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ead9-132">INPUTS</span></span>

### <span data-ttu-id="5ead9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5ead9-133">System.String</span></span>
## <span data-ttu-id="5ead9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ead9-134">OUTPUTS</span></span>

### <span data-ttu-id="5ead9-135">Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="5ead9-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="5ead9-136">Note</span><span class="sxs-lookup"><span data-stu-id="5ead9-136">NOTES</span></span>

## <span data-ttu-id="5ead9-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ead9-137">RELATED LINKS</span></span>
