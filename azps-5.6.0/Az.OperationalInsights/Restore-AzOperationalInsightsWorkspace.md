---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1035d918870a15000be066fd59cc72913d8d8cf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989755"
---
# <span data-ttu-id="0703f-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0703f-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="0703f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0703f-102">SYNOPSIS</span></span>
<span data-ttu-id="0703f-103">Ripristinare un'area di lavoro eliminata.</span><span class="sxs-lookup"><span data-stu-id="0703f-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="0703f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0703f-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0703f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0703f-105">DESCRIPTION</span></span>
<span data-ttu-id="0703f-106">Ripristinare un'area di lavoro eliminata.</span><span class="sxs-lookup"><span data-stu-id="0703f-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="0703f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0703f-107">EXAMPLES</span></span>

### <span data-ttu-id="0703f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0703f-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="0703f-109">Ripristinare l'area di lavoro eliminata.</span><span class="sxs-lookup"><span data-stu-id="0703f-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="0703f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0703f-110">PARAMETERS</span></span>

### <span data-ttu-id="0703f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0703f-111">-DefaultProfile</span></span>
<span data-ttu-id="0703f-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0703f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0703f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0703f-113">-Force</span></span>
<span data-ttu-id="0703f-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="0703f-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0703f-115">-Location</span><span class="sxs-lookup"><span data-stu-id="0703f-115">-Location</span></span>
<span data-ttu-id="0703f-116">Area geografica in cui verrà creata l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0703f-116">The geographic region that the workspace will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0703f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0703f-117">-Name</span></span>
<span data-ttu-id="0703f-118">Il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0703f-118">The workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0703f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0703f-119">-ResourceGroupName</span></span>
<span data-ttu-id="0703f-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0703f-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0703f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0703f-121">-Confirm</span></span>
<span data-ttu-id="0703f-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0703f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0703f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0703f-123">-WhatIf</span></span>
<span data-ttu-id="0703f-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0703f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0703f-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0703f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0703f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0703f-126">CommonParameters</span></span>
<span data-ttu-id="0703f-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0703f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0703f-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0703f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0703f-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="0703f-129">INPUTS</span></span>

### <span data-ttu-id="0703f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0703f-130">System.String</span></span>

## <span data-ttu-id="0703f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0703f-131">OUTPUTS</span></span>

### <span data-ttu-id="0703f-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0703f-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="0703f-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="0703f-133">NOTES</span></span>

## <span data-ttu-id="0703f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0703f-134">RELATED LINKS</span></span>
