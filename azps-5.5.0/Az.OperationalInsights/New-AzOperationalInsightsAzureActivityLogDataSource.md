---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 6dc016e717e89ad60e066be1c1d86e5871309d9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184103"
---
# <span data-ttu-id="302f6-101">New-AzOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="302f6-101">New-AzOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="302f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="302f6-102">SYNOPSIS</span></span>
<span data-ttu-id="302f6-103">Raccogliere il log attività di Azure dalla sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="302f6-103">Collect Azure Activity log from given subscription.</span></span>

## <span data-ttu-id="302f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="302f6-104">SYNTAX</span></span>

### <span data-ttu-id="302f6-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="302f6-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="302f6-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="302f6-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="302f6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="302f6-107">DESCRIPTION</span></span>
<span data-ttu-id="302f6-108">LNew-AzOperationalInsightsAzureActivityLogDataSource consente a Analisi log di raccogliere il log attività di Azure da una determinata sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="302f6-108">The New-AzOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="302f6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="302f6-109">EXAMPLES</span></span>

### <span data-ttu-id="302f6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="302f6-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="302f6-111">{{ Aggiungi la descrizione di esempio qui }}</span><span class="sxs-lookup"><span data-stu-id="302f6-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="302f6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="302f6-112">PARAMETERS</span></span>

### <span data-ttu-id="302f6-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="302f6-113">-BackfillStartTime</span></span>
<span data-ttu-id="302f6-114">È possibile scegliere di eseguire i registri di recupero delle informazioni una settimana fa.</span><span class="sxs-lookup"><span data-stu-id="302f6-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="302f6-115">-DefaultProfile</span></span>
<span data-ttu-id="302f6-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="302f6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="302f6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="302f6-117">-Force</span></span>
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

### <span data-ttu-id="302f6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="302f6-118">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302f6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="302f6-119">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302f6-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="302f6-120">-SubscriptionId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302f6-121">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="302f6-121">-Workspace</span></span>
```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="302f6-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="302f6-122">-WorkspaceName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302f6-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="302f6-123">-Confirm</span></span>
<span data-ttu-id="302f6-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="302f6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="302f6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="302f6-125">-WhatIf</span></span>
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

### <span data-ttu-id="302f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302f6-126">CommonParameters</span></span>
<span data-ttu-id="302f6-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="302f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="302f6-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="302f6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302f6-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="302f6-129">INPUTS</span></span>

### <span data-ttu-id="302f6-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="302f6-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="302f6-131">System.String</span><span class="sxs-lookup"><span data-stu-id="302f6-131">System.String</span></span>

### <span data-ttu-id="302f6-132">System.DateTime Offset</span><span class="sxs-lookup"><span data-stu-id="302f6-132">System.DateTimeOffset</span></span>

## <span data-ttu-id="302f6-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="302f6-133">OUTPUTS</span></span>

### <span data-ttu-id="302f6-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="302f6-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="302f6-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="302f6-135">NOTES</span></span>

## <span data-ttu-id="302f6-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="302f6-136">RELATED LINKS</span></span>
