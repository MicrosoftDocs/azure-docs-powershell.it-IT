---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 31c9728a95e5cfc52b283a8dddc0e24ffffe1630
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976350"
---
# <span data-ttu-id="77b62-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="77b62-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="77b62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77b62-102">SYNOPSIS</span></span>
<span data-ttu-id="77b62-103">Creare un segnalibro.</span><span class="sxs-lookup"><span data-stu-id="77b62-103">Create a Bookmark.</span></span>

## <span data-ttu-id="77b62-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77b62-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77b62-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="77b62-105">DESCRIPTION</span></span>
<span data-ttu-id="77b62-106">Il cmdlet **New-AzSentinelBookmark crea** un segnalibro dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="77b62-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="77b62-107">È possibile usare il *parametro Confirm* $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="77b62-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="77b62-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77b62-108">EXAMPLES</span></span>

### <span data-ttu-id="77b62-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="77b62-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="77b62-110">Questo esempio crea un **segnalibro nell'area** di lavoro specificata e quindi lo archivia nella $Bookmark variabile.</span><span class="sxs-lookup"><span data-stu-id="77b62-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="77b62-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77b62-111">PARAMETERS</span></span>

### <span data-ttu-id="77b62-112">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="77b62-112">-BookmarkId</span></span>
<span data-ttu-id="77b62-113">Id segnalibro</span><span class="sxs-lookup"><span data-stu-id="77b62-113">Bookmark Id,</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77b62-114">-DefaultProfile</span></span>
<span data-ttu-id="77b62-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77b62-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77b62-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="77b62-116">-DisplayName</span></span>
<span data-ttu-id="77b62-117">Nome visualizzato regola segnalibro.</span><span class="sxs-lookup"><span data-stu-id="77b62-117">Bookmark Rule Display Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b62-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="77b62-118">-IncidentInfo</span></span>
<span data-ttu-id="77b62-119">Informazioni evento imprevisto segnalibro.</span><span class="sxs-lookup"><span data-stu-id="77b62-119">Bookmark Incident Info.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77b62-120">-Label</span><span class="sxs-lookup"><span data-stu-id="77b62-120">-Label</span></span>
<span data-ttu-id="77b62-121">Etichette degli eventi.</span><span class="sxs-lookup"><span data-stu-id="77b62-121">Incident Labels.</span></span>

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

### <span data-ttu-id="77b62-122">-Note</span><span class="sxs-lookup"><span data-stu-id="77b62-122">-Notes</span></span>
<span data-ttu-id="77b62-123">Aggiungere segnalibri alle note.</span><span class="sxs-lookup"><span data-stu-id="77b62-123">Bookmark Notes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b62-124">-Query</span><span class="sxs-lookup"><span data-stu-id="77b62-124">-Query</span></span>
<span data-ttu-id="77b62-125">Query segnalibro.</span><span class="sxs-lookup"><span data-stu-id="77b62-125">Bookmark Query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b62-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="77b62-126">-QueryResult</span></span>
<span data-ttu-id="77b62-127">Risultato della query segnalibro.</span><span class="sxs-lookup"><span data-stu-id="77b62-127">Bookmark Query Result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b62-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77b62-128">-ResourceGroupName</span></span>
<span data-ttu-id="77b62-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="77b62-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b62-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="77b62-130">-WorkspaceName</span></span>
<span data-ttu-id="77b62-131">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="77b62-131">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b62-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77b62-132">-Confirm</span></span>
<span data-ttu-id="77b62-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77b62-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77b62-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77b62-134">-WhatIf</span></span>
<span data-ttu-id="77b62-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77b62-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77b62-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77b62-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77b62-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b62-137">CommonParameters</span></span>
<span data-ttu-id="77b62-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77b62-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b62-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="77b62-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b62-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="77b62-140">INPUTS</span></span>

### <span data-ttu-id="77b62-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="77b62-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="77b62-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77b62-142">OUTPUTS</span></span>

### <span data-ttu-id="77b62-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="77b62-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="77b62-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="77b62-144">NOTES</span></span>

## <span data-ttu-id="77b62-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77b62-145">RELATED LINKS</span></span>
