---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/unregister-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
ms.openlocfilehash: 0533864f3fd16e9810e837629782b767fbdc0435
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341095"
---
# <span data-ttu-id="a6ebe-101">Unregister-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="a6ebe-101">Unregister-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="a6ebe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="a6ebe-103">Annulla la registrazione del gruppo applicazione desktop virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="a6ebe-103">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="a6ebe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6ebe-104">SYNTAX</span></span>

```
Unregister-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a6ebe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6ebe-105">DESCRIPTION</span></span>
<span data-ttu-id="a6ebe-106">Annulla la registrazione del gruppo applicazione desktop virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="a6ebe-106">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="a6ebe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6ebe-107">EXAMPLES</span></span>

### <span data-ttu-id="a6ebe-108">Esempio 1: annullare la registrazione di un gruppo di applicazioni desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="a6ebe-108">Example 1: Unregister a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Unregister-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="a6ebe-109">Questo comando Annulla la registrazione di un gruppo di applicazioni desktop virtuale di Windows in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="a6ebe-109">This command unregisters a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="a6ebe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6ebe-110">PARAMETERS</span></span>

### <span data-ttu-id="a6ebe-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="a6ebe-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="a6ebe-112">Percorso ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6ebe-112">ResourceGroupName Path</span></span>

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

### <span data-ttu-id="a6ebe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6ebe-113">-DefaultProfile</span></span>
<span data-ttu-id="a6ebe-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6ebe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6ebe-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6ebe-115">-ResourceGroupName</span></span>
<span data-ttu-id="a6ebe-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a6ebe-116">Resource Group Name</span></span>

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

### <span data-ttu-id="a6ebe-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6ebe-117">-SubscriptionId</span></span>
<span data-ttu-id="a6ebe-118">ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="a6ebe-118">Subscription Id</span></span>

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

### <span data-ttu-id="a6ebe-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a6ebe-119">-WorkspaceName</span></span>
<span data-ttu-id="a6ebe-120">Nome area di lavoro</span><span class="sxs-lookup"><span data-stu-id="a6ebe-120">Workspace Name</span></span>

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

### <span data-ttu-id="a6ebe-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a6ebe-121">-Confirm</span></span>
<span data-ttu-id="a6ebe-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6ebe-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6ebe-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6ebe-123">-WhatIf</span></span>
<span data-ttu-id="a6ebe-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6ebe-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6ebe-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6ebe-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6ebe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6ebe-126">CommonParameters</span></span>
<span data-ttu-id="a6ebe-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6ebe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6ebe-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6ebe-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6ebe-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6ebe-129">INPUTS</span></span>

## <span data-ttu-id="a6ebe-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6ebe-130">OUTPUTS</span></span>

### <span data-ttu-id="a6ebe-131">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="a6ebe-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="a6ebe-132">Note</span><span class="sxs-lookup"><span data-stu-id="a6ebe-132">NOTES</span></span>

<span data-ttu-id="a6ebe-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a6ebe-133">ALIASES</span></span>

## <span data-ttu-id="a6ebe-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6ebe-134">RELATED LINKS</span></span>

