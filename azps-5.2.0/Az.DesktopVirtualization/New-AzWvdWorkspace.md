---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: a9fc9a4900b7e11fddb01e47fbcf1c5407926749
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338455"
---
# <span data-ttu-id="b5670-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="b5670-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="b5670-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5670-102">SYNOPSIS</span></span>
<span data-ttu-id="b5670-103">Creare o aggiornare un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b5670-103">Create or update a workspace.</span></span>

## <span data-ttu-id="b5670-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5670-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b5670-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5670-105">DESCRIPTION</span></span>
<span data-ttu-id="b5670-106">Creare o aggiornare un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b5670-106">Create or update a workspace.</span></span>

## <span data-ttu-id="b5670-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5670-107">EXAMPLES</span></span>

### <span data-ttu-id="b5670-108">Esempio 1: creare un'area di lavoro desktop virtuale di Windows per nome</span><span class="sxs-lookup"><span data-stu-id="b5670-108">Example 1: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="b5670-109">Questo comando crea un'area di lavoro desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5670-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="b5670-110">Esempio 2: creare un'area di lavoro desktop virtuale di Windows per nome</span><span class="sxs-lookup"><span data-stu-id="b5670-110">Example 2: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="b5670-111">Questo comando crea un'area di lavoro desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5670-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="b5670-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5670-112">PARAMETERS</span></span>

### <span data-ttu-id="b5670-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="b5670-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="b5670-114">Elenco di ID delle risorse di applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="b5670-114">List of applicationGroup resource Ids.</span></span>

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

### <span data-ttu-id="b5670-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5670-115">-DefaultProfile</span></span>
<span data-ttu-id="b5670-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5670-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5670-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5670-117">-Description</span></span>
<span data-ttu-id="b5670-118">Descrizione dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b5670-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="b5670-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b5670-119">-FriendlyName</span></span>
<span data-ttu-id="b5670-120">Nome descrittivo dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b5670-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="b5670-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b5670-121">-Location</span></span>
<span data-ttu-id="b5670-122">Posizione geografica in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="b5670-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="b5670-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5670-123">-Name</span></span>
<span data-ttu-id="b5670-124">Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="b5670-124">The name of the workspace</span></span>

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

### <span data-ttu-id="b5670-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5670-125">-ResourceGroupName</span></span>
<span data-ttu-id="b5670-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5670-126">The name of the resource group.</span></span>
<span data-ttu-id="b5670-127">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b5670-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b5670-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5670-128">-SubscriptionId</span></span>
<span data-ttu-id="b5670-129">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b5670-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b5670-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="b5670-130">-Tag</span></span>
<span data-ttu-id="b5670-131">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="b5670-131">Resource tags.</span></span>

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

### <span data-ttu-id="b5670-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b5670-132">-Confirm</span></span>
<span data-ttu-id="b5670-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5670-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5670-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5670-134">-WhatIf</span></span>
<span data-ttu-id="b5670-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5670-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5670-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5670-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5670-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5670-137">CommonParameters</span></span>
<span data-ttu-id="b5670-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5670-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5670-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5670-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5670-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5670-140">INPUTS</span></span>

## <span data-ttu-id="b5670-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5670-141">OUTPUTS</span></span>

### <span data-ttu-id="b5670-142">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201019Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="b5670-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IWorkspace</span></span>

## <span data-ttu-id="b5670-143">Note</span><span class="sxs-lookup"><span data-stu-id="b5670-143">NOTES</span></span>

<span data-ttu-id="b5670-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b5670-144">ALIASES</span></span>

## <span data-ttu-id="b5670-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5670-145">RELATED LINKS</span></span>

