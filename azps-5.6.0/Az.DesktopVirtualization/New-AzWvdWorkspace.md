---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: 9335bb4c3177fa405d65038255f43dbba5fb88fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966078"
---
# <span data-ttu-id="80e95-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="80e95-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="80e95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80e95-102">SYNOPSIS</span></span>
<span data-ttu-id="80e95-103">Creare o aggiornare un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="80e95-103">Create or update a workspace.</span></span>

## <span data-ttu-id="80e95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80e95-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="80e95-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="80e95-105">DESCRIPTION</span></span>
<span data-ttu-id="80e95-106">Creare o aggiornare un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="80e95-106">Create or update a workspace.</span></span>

## <span data-ttu-id="80e95-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80e95-107">EXAMPLES</span></span>

### <span data-ttu-id="80e95-108">Esempio 1: Creare un'area di lavoro desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="80e95-108">Example 1: Create a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference $null `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="80e95-109">Questo comando crea un'area di lavoro desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="80e95-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="80e95-110">Esempio 2: Creare un'area di lavoro desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="80e95-110">Example 2: Create a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="80e95-111">Questo comando crea un'area di lavoro desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="80e95-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="80e95-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80e95-112">PARAMETERS</span></span>

### <span data-ttu-id="80e95-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="80e95-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="80e95-114">Elenco di ID di risorse applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="80e95-114">List of applicationGroup resource Ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80e95-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80e95-115">-DefaultProfile</span></span>
<span data-ttu-id="80e95-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80e95-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80e95-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="80e95-117">-Description</span></span>
<span data-ttu-id="80e95-118">Descrizione dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="80e95-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="80e95-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="80e95-119">-FriendlyName</span></span>
<span data-ttu-id="80e95-120">Nome descrittivo dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="80e95-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="80e95-121">-Location</span><span class="sxs-lookup"><span data-stu-id="80e95-121">-Location</span></span>
<span data-ttu-id="80e95-122">Posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="80e95-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="80e95-123">-Name</span><span class="sxs-lookup"><span data-stu-id="80e95-123">-Name</span></span>
<span data-ttu-id="80e95-124">Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="80e95-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80e95-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80e95-125">-ResourceGroupName</span></span>
<span data-ttu-id="80e95-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="80e95-126">The name of the resource group.</span></span>
<span data-ttu-id="80e95-127">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="80e95-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="80e95-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80e95-128">-SubscriptionId</span></span>
<span data-ttu-id="80e95-129">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="80e95-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80e95-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="80e95-130">-Tag</span></span>
<span data-ttu-id="80e95-131">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="80e95-131">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80e95-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80e95-132">-Confirm</span></span>
<span data-ttu-id="80e95-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80e95-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80e95-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80e95-134">-WhatIf</span></span>
<span data-ttu-id="80e95-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80e95-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80e95-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80e95-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80e95-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80e95-137">CommonParameters</span></span>
<span data-ttu-id="80e95-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80e95-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80e95-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="80e95-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80e95-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="80e95-140">INPUTS</span></span>

## <span data-ttu-id="80e95-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80e95-141">OUTPUTS</span></span>

### <span data-ttu-id="80e95-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="80e95-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="80e95-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="80e95-143">NOTES</span></span>

<span data-ttu-id="80e95-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="80e95-144">ALIASES</span></span>

## <span data-ttu-id="80e95-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80e95-145">RELATED LINKS</span></span>

