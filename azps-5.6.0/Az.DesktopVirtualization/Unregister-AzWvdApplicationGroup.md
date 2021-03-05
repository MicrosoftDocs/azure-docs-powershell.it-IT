---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/unregister-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
ms.openlocfilehash: 9d3b8c0b1c126353eeab8a2509395e25e467bf0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965997"
---
# <span data-ttu-id="06694-101">Unregister-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="06694-101">Unregister-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="06694-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06694-102">SYNOPSIS</span></span>
<span data-ttu-id="06694-103">Annullare la registrazione del gruppo di applicazioni desktop virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="06694-103">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="06694-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06694-104">SYNTAX</span></span>

```
Unregister-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="06694-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="06694-105">DESCRIPTION</span></span>
<span data-ttu-id="06694-106">Annullare la registrazione del gruppo di applicazioni desktop virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="06694-106">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="06694-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06694-107">EXAMPLES</span></span>

### <span data-ttu-id="06694-108">Esempio 1: Annullare la registrazione di un gruppo di applicazioni Desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="06694-108">Example 1: Unregister a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Unregister-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="06694-109">Questo comando annulla la registrazione di un gruppo di applicazioni desktop virtuale di Windows in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="06694-109">This command unregisters a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="06694-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06694-110">PARAMETERS</span></span>

### <span data-ttu-id="06694-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="06694-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="06694-112">ResourceGroupName Path</span><span class="sxs-lookup"><span data-stu-id="06694-112">ResourceGroupName Path</span></span>

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

### <span data-ttu-id="06694-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06694-113">-DefaultProfile</span></span>
<span data-ttu-id="06694-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06694-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06694-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06694-115">-ResourceGroupName</span></span>
<span data-ttu-id="06694-116">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="06694-116">Resource Group Name</span></span>

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

### <span data-ttu-id="06694-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06694-117">-SubscriptionId</span></span>
<span data-ttu-id="06694-118">ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="06694-118">Subscription Id</span></span>

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

### <span data-ttu-id="06694-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="06694-119">-WorkspaceName</span></span>
<span data-ttu-id="06694-120">Nome area di lavoro</span><span class="sxs-lookup"><span data-stu-id="06694-120">Workspace Name</span></span>

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

### <span data-ttu-id="06694-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06694-121">-Confirm</span></span>
<span data-ttu-id="06694-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06694-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06694-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06694-123">-WhatIf</span></span>
<span data-ttu-id="06694-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06694-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06694-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06694-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06694-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06694-126">CommonParameters</span></span>
<span data-ttu-id="06694-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06694-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06694-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="06694-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06694-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="06694-129">INPUTS</span></span>

## <span data-ttu-id="06694-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06694-130">OUTPUTS</span></span>

### <span data-ttu-id="06694-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="06694-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="06694-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="06694-132">NOTES</span></span>

<span data-ttu-id="06694-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="06694-133">ALIASES</span></span>

## <span data-ttu-id="06694-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06694-134">RELATED LINKS</span></span>

