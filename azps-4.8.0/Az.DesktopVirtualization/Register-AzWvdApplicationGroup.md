---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: 874cc587bff418bf0d6846fe39bdf7d10c42d7dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192969"
---
# <span data-ttu-id="c009e-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="c009e-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="c009e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c009e-102">SYNOPSIS</span></span>
<span data-ttu-id="c009e-103">Registrare un gruppo di applicazioni desktop virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="c009e-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="c009e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c009e-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c009e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c009e-105">DESCRIPTION</span></span>
<span data-ttu-id="c009e-106">Registrare un gruppo di applicazioni desktop virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="c009e-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="c009e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c009e-107">EXAMPLES</span></span>

### <span data-ttu-id="c009e-108">Esempio 1: registrare un gruppo di applicazioni desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="c009e-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="c009e-109">Questo comando registra un gruppo di applicazioni desktop virtuale di Windows in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c009e-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="c009e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c009e-110">PARAMETERS</span></span>

### <span data-ttu-id="c009e-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="c009e-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="c009e-112">Percorso ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="c009e-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="c009e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c009e-113">-DefaultProfile</span></span>
<span data-ttu-id="c009e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c009e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c009e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c009e-115">-ResourceGroupName</span></span>
<span data-ttu-id="c009e-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c009e-116">Resource Group Name</span></span>

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

### <span data-ttu-id="c009e-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c009e-117">-SubscriptionId</span></span>
<span data-ttu-id="c009e-118">ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="c009e-118">Subscription Id</span></span>

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

### <span data-ttu-id="c009e-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c009e-119">-WorkspaceName</span></span>
<span data-ttu-id="c009e-120">Nome area di lavoro</span><span class="sxs-lookup"><span data-stu-id="c009e-120">Workspace Name</span></span>

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

### <span data-ttu-id="c009e-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c009e-121">-Confirm</span></span>
<span data-ttu-id="c009e-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c009e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c009e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c009e-123">-WhatIf</span></span>
<span data-ttu-id="c009e-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c009e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c009e-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c009e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c009e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c009e-126">CommonParameters</span></span>
<span data-ttu-id="c009e-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c009e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c009e-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c009e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c009e-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c009e-129">INPUTS</span></span>

## <span data-ttu-id="c009e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c009e-130">OUTPUTS</span></span>

### <span data-ttu-id="c009e-131">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="c009e-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="c009e-132">Note</span><span class="sxs-lookup"><span data-stu-id="c009e-132">NOTES</span></span>

<span data-ttu-id="c009e-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c009e-133">ALIASES</span></span>

## <span data-ttu-id="c009e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c009e-134">RELATED LINKS</span></span>

