---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: ef1829dec7bdc1c3b41fa9e418246e1d9afcc1f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966061"
---
# <span data-ttu-id="ba2ed-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="ba2ed-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="ba2ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba2ed-102">SYNOPSIS</span></span>
<span data-ttu-id="ba2ed-103">Registrare un gruppo di applicazioni desktop virtuali di Windows.</span><span class="sxs-lookup"><span data-stu-id="ba2ed-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="ba2ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba2ed-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ba2ed-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ba2ed-105">DESCRIPTION</span></span>
<span data-ttu-id="ba2ed-106">Registrare un gruppo di applicazioni desktop virtuali di Windows.</span><span class="sxs-lookup"><span data-stu-id="ba2ed-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="ba2ed-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba2ed-107">EXAMPLES</span></span>

### <span data-ttu-id="ba2ed-108">Esempio 1: Registrare un gruppo di applicazioni Desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="ba2ed-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="ba2ed-109">Questo comando registra un gruppo di applicazioni Desktop virtuale di Windows in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ba2ed-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="ba2ed-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba2ed-110">PARAMETERS</span></span>

### <span data-ttu-id="ba2ed-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="ba2ed-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="ba2ed-112">Percorso ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="ba2ed-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="ba2ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba2ed-113">-DefaultProfile</span></span>
<span data-ttu-id="ba2ed-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba2ed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba2ed-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba2ed-115">-ResourceGroupName</span></span>
<span data-ttu-id="ba2ed-116">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ba2ed-116">Resource Group Name</span></span>

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

### <span data-ttu-id="ba2ed-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba2ed-117">-SubscriptionId</span></span>
<span data-ttu-id="ba2ed-118">ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="ba2ed-118">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba2ed-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ba2ed-119">-WorkspaceName</span></span>
<span data-ttu-id="ba2ed-120">Nome area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ba2ed-120">Workspace Name</span></span>

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

### <span data-ttu-id="ba2ed-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba2ed-121">-Confirm</span></span>
<span data-ttu-id="ba2ed-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba2ed-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba2ed-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba2ed-123">-WhatIf</span></span>
<span data-ttu-id="ba2ed-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba2ed-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba2ed-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba2ed-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba2ed-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba2ed-126">CommonParameters</span></span>
<span data-ttu-id="ba2ed-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba2ed-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba2ed-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ba2ed-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba2ed-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="ba2ed-129">INPUTS</span></span>

## <span data-ttu-id="ba2ed-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba2ed-130">OUTPUTS</span></span>

### <span data-ttu-id="ba2ed-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="ba2ed-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="ba2ed-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="ba2ed-132">NOTES</span></span>

<span data-ttu-id="ba2ed-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ba2ed-133">ALIASES</span></span>

## <span data-ttu-id="ba2ed-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba2ed-134">RELATED LINKS</span></span>

