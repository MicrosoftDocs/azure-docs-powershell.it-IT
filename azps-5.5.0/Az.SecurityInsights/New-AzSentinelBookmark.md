---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 3c30edd841eb2e773c5d813e798e63fc9858437d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201735"
---
# <span data-ttu-id="eb1df-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="eb1df-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="eb1df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb1df-102">SYNOPSIS</span></span>
<span data-ttu-id="eb1df-103">Creare un segnalibro.</span><span class="sxs-lookup"><span data-stu-id="eb1df-103">Create a Bookmark.</span></span>

## <span data-ttu-id="eb1df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb1df-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb1df-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eb1df-105">DESCRIPTION</span></span>
<span data-ttu-id="eb1df-106">Il cmdlet **New-AzSentinelBookmark crea** un segnalibro dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="eb1df-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="eb1df-107">È possibile usare il *parametro Confirm* $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="eb1df-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="eb1df-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb1df-108">EXAMPLES</span></span>

### <span data-ttu-id="eb1df-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eb1df-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="eb1df-110">Questo esempio crea un **segnalibro nell'area** di lavoro specificata e quindi lo archivia nella $Bookmark variabile.</span><span class="sxs-lookup"><span data-stu-id="eb1df-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="eb1df-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb1df-111">PARAMETERS</span></span>

### <span data-ttu-id="eb1df-112">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="eb1df-112">-BookmarkId</span></span>
<span data-ttu-id="eb1df-113">Id segnalibro</span><span class="sxs-lookup"><span data-stu-id="eb1df-113">Bookmark Id,</span></span>

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

### <span data-ttu-id="eb1df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb1df-114">-DefaultProfile</span></span>
<span data-ttu-id="eb1df-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb1df-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb1df-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="eb1df-116">-DisplayName</span></span>
<span data-ttu-id="eb1df-117">Nome visualizzato regola segnalibro.</span><span class="sxs-lookup"><span data-stu-id="eb1df-117">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="eb1df-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="eb1df-118">-IncidentInfo</span></span>
<span data-ttu-id="eb1df-119">Informazioni evento imprevisto segnalibro.</span><span class="sxs-lookup"><span data-stu-id="eb1df-119">Bookmark Incident Info.</span></span>

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

### <span data-ttu-id="eb1df-120">-Label</span><span class="sxs-lookup"><span data-stu-id="eb1df-120">-Label</span></span>
<span data-ttu-id="eb1df-121">Etichette degli eventi.</span><span class="sxs-lookup"><span data-stu-id="eb1df-121">Incident Labels.</span></span>

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

### <span data-ttu-id="eb1df-122">-Note</span><span class="sxs-lookup"><span data-stu-id="eb1df-122">-Notes</span></span>
<span data-ttu-id="eb1df-123">Aggiungere segnalibri alle note.</span><span class="sxs-lookup"><span data-stu-id="eb1df-123">Bookmark Notes.</span></span>

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

### <span data-ttu-id="eb1df-124">-Query</span><span class="sxs-lookup"><span data-stu-id="eb1df-124">-Query</span></span>
<span data-ttu-id="eb1df-125">Query segnalibro.</span><span class="sxs-lookup"><span data-stu-id="eb1df-125">Bookmark Query.</span></span>

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

### <span data-ttu-id="eb1df-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="eb1df-126">-QueryResult</span></span>
<span data-ttu-id="eb1df-127">Risultato della query segnalibro.</span><span class="sxs-lookup"><span data-stu-id="eb1df-127">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="eb1df-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb1df-128">-ResourceGroupName</span></span>
<span data-ttu-id="eb1df-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eb1df-129">Resource group name.</span></span>

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

### <span data-ttu-id="eb1df-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eb1df-130">-WorkspaceName</span></span>
<span data-ttu-id="eb1df-131">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="eb1df-131">Workspace Name.</span></span>

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

### <span data-ttu-id="eb1df-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb1df-132">-Confirm</span></span>
<span data-ttu-id="eb1df-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb1df-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb1df-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb1df-134">-WhatIf</span></span>
<span data-ttu-id="eb1df-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb1df-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb1df-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb1df-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb1df-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb1df-137">CommonParameters</span></span>
<span data-ttu-id="eb1df-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb1df-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb1df-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eb1df-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb1df-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="eb1df-140">INPUTS</span></span>

### <span data-ttu-id="eb1df-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="eb1df-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="eb1df-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb1df-142">OUTPUTS</span></span>

### <span data-ttu-id="eb1df-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="eb1df-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="eb1df-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="eb1df-144">NOTES</span></span>

## <span data-ttu-id="eb1df-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb1df-145">RELATED LINKS</span></span>
