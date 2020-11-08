---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 6dc016e717e89ad60e066be1c1d86e5871309d9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200694"
---
# <span data-ttu-id="278e5-101">New-AzOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="278e5-101">New-AzOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="278e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="278e5-102">SYNOPSIS</span></span>
<span data-ttu-id="278e5-103">Raccogliere il log delle attività di Azure da un abbonamento specifico.</span><span class="sxs-lookup"><span data-stu-id="278e5-103">Collect Azure Activity log from given subscription.</span></span>

## <span data-ttu-id="278e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="278e5-104">SYNTAX</span></span>

### <span data-ttu-id="278e5-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="278e5-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="278e5-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="278e5-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="278e5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="278e5-107">DESCRIPTION</span></span>
<span data-ttu-id="278e5-108">L'New-AzOperationalInsightsAzureActivityLogDataSource Abilita analisi log per raccogliere il log delle attività di Azure da un abbonamento specifico.</span><span class="sxs-lookup"><span data-stu-id="278e5-108">The New-AzOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="278e5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="278e5-109">EXAMPLES</span></span>

### <span data-ttu-id="278e5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="278e5-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="278e5-111">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="278e5-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="278e5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="278e5-112">PARAMETERS</span></span>

### <span data-ttu-id="278e5-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="278e5-113">-BackfillStartTime</span></span>
<span data-ttu-id="278e5-114">È possibile scegliere di riempire i log di una settimana fa.</span><span class="sxs-lookup"><span data-stu-id="278e5-114">You can choose to backfill logs from a week ago.</span></span>

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

### <span data-ttu-id="278e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="278e5-115">-DefaultProfile</span></span>
<span data-ttu-id="278e5-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="278e5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="278e5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="278e5-117">-Force</span></span>
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

### <span data-ttu-id="278e5-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="278e5-118">-Name</span></span>
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

### <span data-ttu-id="278e5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="278e5-119">-ResourceGroupName</span></span>
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

### <span data-ttu-id="278e5-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="278e5-120">-SubscriptionId</span></span>
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

### <span data-ttu-id="278e5-121">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="278e5-121">-Workspace</span></span>
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

### <span data-ttu-id="278e5-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="278e5-122">-WorkspaceName</span></span>
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

### <span data-ttu-id="278e5-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="278e5-123">-Confirm</span></span>
<span data-ttu-id="278e5-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="278e5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="278e5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="278e5-125">-WhatIf</span></span>
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

### <span data-ttu-id="278e5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="278e5-126">CommonParameters</span></span>
<span data-ttu-id="278e5-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="278e5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="278e5-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="278e5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="278e5-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="278e5-129">INPUTS</span></span>

### <span data-ttu-id="278e5-130">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="278e5-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="278e5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="278e5-131">System.String</span></span>

### <span data-ttu-id="278e5-132">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="278e5-132">System.DateTimeOffset</span></span>

## <span data-ttu-id="278e5-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="278e5-133">OUTPUTS</span></span>

### <span data-ttu-id="278e5-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="278e5-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="278e5-135">Note</span><span class="sxs-lookup"><span data-stu-id="278e5-135">NOTES</span></span>

## <span data-ttu-id="278e5-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="278e5-136">RELATED LINKS</span></span>