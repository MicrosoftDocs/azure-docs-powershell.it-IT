---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: b97db1a21afab939e94b776b3da8d43f3d1468b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204258"
---
# <span data-ttu-id="62aec-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="62aec-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="62aec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62aec-102">SYNOPSIS</span></span>
<span data-ttu-id="62aec-103">Creare o aggiornare un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="62aec-103">Create or update a workspace.</span></span>

## <span data-ttu-id="62aec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62aec-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="62aec-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="62aec-105">DESCRIPTION</span></span>
<span data-ttu-id="62aec-106">Creare o aggiornare un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="62aec-106">Create or update a workspace.</span></span>

## <span data-ttu-id="62aec-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62aec-107">EXAMPLES</span></span>

### <span data-ttu-id="62aec-108">Esempio 1: Creare un'area di lavoro desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="62aec-108">Example 1: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="62aec-109">Questo comando crea un'area di lavoro desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="62aec-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="62aec-110">Esempio 2: Creare un'area di lavoro desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="62aec-110">Example 2: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="62aec-111">Questo comando crea un'area di lavoro desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="62aec-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="62aec-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62aec-112">PARAMETERS</span></span>

### <span data-ttu-id="62aec-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="62aec-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="62aec-114">Elenco di ID di risorse applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="62aec-114">List of applicationGroup resource Ids.</span></span>

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

### <span data-ttu-id="62aec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62aec-115">-DefaultProfile</span></span>
<span data-ttu-id="62aec-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62aec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62aec-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="62aec-117">-Description</span></span>
<span data-ttu-id="62aec-118">Descrizione dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="62aec-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="62aec-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="62aec-119">-FriendlyName</span></span>
<span data-ttu-id="62aec-120">Nome descrittivo dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="62aec-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="62aec-121">-Location</span><span class="sxs-lookup"><span data-stu-id="62aec-121">-Location</span></span>
<span data-ttu-id="62aec-122">Posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="62aec-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="62aec-123">-Name</span><span class="sxs-lookup"><span data-stu-id="62aec-123">-Name</span></span>
<span data-ttu-id="62aec-124">Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="62aec-124">The name of the workspace</span></span>

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

### <span data-ttu-id="62aec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62aec-125">-ResourceGroupName</span></span>
<span data-ttu-id="62aec-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="62aec-126">The name of the resource group.</span></span>
<span data-ttu-id="62aec-127">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="62aec-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="62aec-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62aec-128">-SubscriptionId</span></span>
<span data-ttu-id="62aec-129">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="62aec-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="62aec-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="62aec-130">-Tag</span></span>
<span data-ttu-id="62aec-131">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="62aec-131">Resource tags.</span></span>

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

### <span data-ttu-id="62aec-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62aec-132">-Confirm</span></span>
<span data-ttu-id="62aec-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62aec-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62aec-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62aec-134">-WhatIf</span></span>
<span data-ttu-id="62aec-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62aec-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62aec-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62aec-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62aec-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62aec-137">CommonParameters</span></span>
<span data-ttu-id="62aec-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62aec-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62aec-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="62aec-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62aec-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="62aec-140">INPUTS</span></span>

## <span data-ttu-id="62aec-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62aec-141">OUTPUTS</span></span>

### <span data-ttu-id="62aec-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="62aec-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="62aec-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="62aec-143">NOTES</span></span>

<span data-ttu-id="62aec-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="62aec-144">ALIASES</span></span>

## <span data-ttu-id="62aec-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62aec-145">RELATED LINKS</span></span>

