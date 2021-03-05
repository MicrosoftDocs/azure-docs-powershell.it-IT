---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
ms.openlocfilehash: 0fe04e773e02a8b6b61f9c57d8316ac8936f05aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963677"
---
# <span data-ttu-id="44b25-101">New-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="44b25-101">New-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="44b25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44b25-102">SYNOPSIS</span></span>
<span data-ttu-id="44b25-103">Aggiungere un commento dell'evento imprevisto a un evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="44b25-103">Add an Incident Comment to an Incident.</span></span>

## <span data-ttu-id="44b25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44b25-104">SYNTAX</span></span>

```
New-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-IncidentCommentId <String>] -Message <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44b25-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="44b25-105">DESCRIPTION</span></span>
<span data-ttu-id="44b25-106">Il cmdlet **New-AzSentinelIncidentComment** crea un commento dell'evento dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="44b25-106">The **New-AzSentinelIncidentComment** cmdlet creates a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="44b25-107">È possibile usare il *parametro Confirm* $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="44b25-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="44b25-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44b25-108">EXAMPLES</span></span>

### <span data-ttu-id="44b25-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="44b25-109">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $IncidentComment = New-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId ($Incident.Name) -Message "Still needs investigation"
```

<span data-ttu-id="44b25-110">Questo esempio crea **un evento IncidentComment nell'area** di lavoro specificata e quindi lo archivia nella $IncidentComment variabile.</span><span class="sxs-lookup"><span data-stu-id="44b25-110">This example creates an **IncidentComment** in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="44b25-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44b25-111">PARAMETERS</span></span>

### <span data-ttu-id="44b25-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44b25-112">-DefaultProfile</span></span>
<span data-ttu-id="44b25-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44b25-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44b25-114">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="44b25-114">-IncidentCommentId</span></span>
<span data-ttu-id="44b25-115">ID commento evento.</span><span class="sxs-lookup"><span data-stu-id="44b25-115">Incident Comment Id.</span></span>

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

### <span data-ttu-id="44b25-116">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="44b25-116">-IncidentId</span></span>
<span data-ttu-id="44b25-117">ID evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="44b25-117">Incident Id.</span></span>

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

### <span data-ttu-id="44b25-118">-Messaggio</span><span class="sxs-lookup"><span data-stu-id="44b25-118">-Message</span></span>
<span data-ttu-id="44b25-119">Messaggio dell'evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="44b25-119">Incident Message.</span></span>

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

### <span data-ttu-id="44b25-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44b25-120">-ResourceGroupName</span></span>
<span data-ttu-id="44b25-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="44b25-121">Resource group name.</span></span>

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

### <span data-ttu-id="44b25-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="44b25-122">-WorkspaceName</span></span>
<span data-ttu-id="44b25-123">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="44b25-123">Workspace Name.</span></span>

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

### <span data-ttu-id="44b25-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44b25-124">-Confirm</span></span>
<span data-ttu-id="44b25-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44b25-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44b25-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44b25-126">-WhatIf</span></span>
<span data-ttu-id="44b25-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44b25-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44b25-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44b25-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44b25-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b25-129">CommonParameters</span></span>
<span data-ttu-id="44b25-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44b25-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b25-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="44b25-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b25-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="44b25-132">INPUTS</span></span>

### <span data-ttu-id="44b25-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="44b25-133">None</span></span>
## <span data-ttu-id="44b25-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44b25-134">OUTPUTS</span></span>

### <span data-ttu-id="44b25-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="44b25-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="44b25-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="44b25-136">NOTES</span></span>

## <span data-ttu-id="44b25-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44b25-137">RELATED LINKS</span></span>
