---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: b97db1a21afab939e94b776b3da8d43f3d1468b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476376"
---
# <span data-ttu-id="fb282-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="fb282-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="fb282-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb282-102">SYNOPSIS</span></span>
<span data-ttu-id="fb282-103">Creare o aggiornare un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="fb282-103">Create or update a workspace.</span></span>

## <span data-ttu-id="fb282-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb282-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fb282-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb282-105">DESCRIPTION</span></span>
<span data-ttu-id="fb282-106">Creare o aggiornare un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="fb282-106">Create or update a workspace.</span></span>

## <span data-ttu-id="fb282-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb282-107">EXAMPLES</span></span>

### <span data-ttu-id="fb282-108">Esempio 1: creare un'area di lavoro desktop virtuale di Windows per nome</span><span class="sxs-lookup"><span data-stu-id="fb282-108">Example 1: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="fb282-109">Questo comando crea un'area di lavoro desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fb282-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="fb282-110">Esempio 2: creare un'area di lavoro desktop virtuale di Windows per nome</span><span class="sxs-lookup"><span data-stu-id="fb282-110">Example 2: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="fb282-111">Questo comando crea un'area di lavoro desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fb282-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="fb282-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb282-112">PARAMETERS</span></span>

### <span data-ttu-id="fb282-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="fb282-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="fb282-114">Elenco di ID delle risorse di applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="fb282-114">List of applicationGroup resource Ids.</span></span>

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

### <span data-ttu-id="fb282-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb282-115">-DefaultProfile</span></span>
<span data-ttu-id="fb282-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb282-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb282-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb282-117">-Description</span></span>
<span data-ttu-id="fb282-118">Descrizione dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="fb282-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="fb282-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="fb282-119">-FriendlyName</span></span>
<span data-ttu-id="fb282-120">Nome descrittivo dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="fb282-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="fb282-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fb282-121">-Location</span></span>
<span data-ttu-id="fb282-122">Posizione geografica in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="fb282-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="fb282-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb282-123">-Name</span></span>
<span data-ttu-id="fb282-124">Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="fb282-124">The name of the workspace</span></span>

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

### <span data-ttu-id="fb282-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb282-125">-ResourceGroupName</span></span>
<span data-ttu-id="fb282-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fb282-126">The name of the resource group.</span></span>
<span data-ttu-id="fb282-127">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fb282-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fb282-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fb282-128">-SubscriptionId</span></span>
<span data-ttu-id="fb282-129">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fb282-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fb282-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="fb282-130">-Tag</span></span>
<span data-ttu-id="fb282-131">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="fb282-131">Resource tags.</span></span>

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

### <span data-ttu-id="fb282-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fb282-132">-Confirm</span></span>
<span data-ttu-id="fb282-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb282-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb282-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb282-134">-WhatIf</span></span>
<span data-ttu-id="fb282-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb282-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb282-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb282-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb282-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb282-137">CommonParameters</span></span>
<span data-ttu-id="fb282-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb282-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb282-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb282-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb282-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb282-140">INPUTS</span></span>

## <span data-ttu-id="fb282-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb282-141">OUTPUTS</span></span>

### <span data-ttu-id="fb282-142">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201102Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="fb282-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="fb282-143">Note</span><span class="sxs-lookup"><span data-stu-id="fb282-143">NOTES</span></span>

<span data-ttu-id="fb282-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fb282-144">ALIASES</span></span>

## <span data-ttu-id="fb282-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb282-145">RELATED LINKS</span></span>

