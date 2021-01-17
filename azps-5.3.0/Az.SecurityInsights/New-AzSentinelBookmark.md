---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 3c30edd841eb2e773c5d813e798e63fc9858437d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486200"
---
# <span data-ttu-id="f62c0-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="f62c0-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="f62c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f62c0-102">SYNOPSIS</span></span>
<span data-ttu-id="f62c0-103">Creare un segnalibro.</span><span class="sxs-lookup"><span data-stu-id="f62c0-103">Create a Bookmark.</span></span>

## <span data-ttu-id="f62c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f62c0-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f62c0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f62c0-105">DESCRIPTION</span></span>
<span data-ttu-id="f62c0-106">Il cmdlet **New-AzSentinelBookmark** crea un segnalibro dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="f62c0-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="f62c0-107">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="f62c0-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="f62c0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f62c0-108">EXAMPLES</span></span>

### <span data-ttu-id="f62c0-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f62c0-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="f62c0-110">Questo esempio crea un **segnalibro** nell'area di lavoro specificata e lo archivia nella variabile $Bookmark.</span><span class="sxs-lookup"><span data-stu-id="f62c0-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="f62c0-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f62c0-111">PARAMETERS</span></span>

### <span data-ttu-id="f62c0-112">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="f62c0-112">-BookmarkId</span></span>
<span data-ttu-id="f62c0-113">ID segnalibro</span><span class="sxs-lookup"><span data-stu-id="f62c0-113">Bookmark Id,</span></span>

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

### <span data-ttu-id="f62c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f62c0-114">-DefaultProfile</span></span>
<span data-ttu-id="f62c0-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f62c0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f62c0-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f62c0-116">-DisplayName</span></span>
<span data-ttu-id="f62c0-117">Nome visualizzato della regola del segnalibro.</span><span class="sxs-lookup"><span data-stu-id="f62c0-117">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="f62c0-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="f62c0-118">-IncidentInfo</span></span>
<span data-ttu-id="f62c0-119">Informazioni sull'incidente del segnalibro.</span><span class="sxs-lookup"><span data-stu-id="f62c0-119">Bookmark Incident Info.</span></span>

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

### <span data-ttu-id="f62c0-120">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="f62c0-120">-Label</span></span>
<span data-ttu-id="f62c0-121">Etichette Incident.</span><span class="sxs-lookup"><span data-stu-id="f62c0-121">Incident Labels.</span></span>

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

### <span data-ttu-id="f62c0-122">-Note</span><span class="sxs-lookup"><span data-stu-id="f62c0-122">-Notes</span></span>
<span data-ttu-id="f62c0-123">Note del segnalibro.</span><span class="sxs-lookup"><span data-stu-id="f62c0-123">Bookmark Notes.</span></span>

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

### <span data-ttu-id="f62c0-124">-Query</span><span class="sxs-lookup"><span data-stu-id="f62c0-124">-Query</span></span>
<span data-ttu-id="f62c0-125">Query di segnalibro.</span><span class="sxs-lookup"><span data-stu-id="f62c0-125">Bookmark Query.</span></span>

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

### <span data-ttu-id="f62c0-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="f62c0-126">-QueryResult</span></span>
<span data-ttu-id="f62c0-127">Risultato della query del segnalibro.</span><span class="sxs-lookup"><span data-stu-id="f62c0-127">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="f62c0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f62c0-128">-ResourceGroupName</span></span>
<span data-ttu-id="f62c0-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f62c0-129">Resource group name.</span></span>

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

### <span data-ttu-id="f62c0-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f62c0-130">-WorkspaceName</span></span>
<span data-ttu-id="f62c0-131">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f62c0-131">Workspace Name.</span></span>

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

### <span data-ttu-id="f62c0-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f62c0-132">-Confirm</span></span>
<span data-ttu-id="f62c0-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f62c0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f62c0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f62c0-134">-WhatIf</span></span>
<span data-ttu-id="f62c0-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f62c0-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f62c0-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f62c0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f62c0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f62c0-137">CommonParameters</span></span>
<span data-ttu-id="f62c0-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f62c0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f62c0-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f62c0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f62c0-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f62c0-140">INPUTS</span></span>

### <span data-ttu-id="f62c0-141">Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="f62c0-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="f62c0-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f62c0-142">OUTPUTS</span></span>

### <span data-ttu-id="f62c0-143">Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="f62c0-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="f62c0-144">Note</span><span class="sxs-lookup"><span data-stu-id="f62c0-144">NOTES</span></span>

## <span data-ttu-id="f62c0-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f62c0-145">RELATED LINKS</span></span>
