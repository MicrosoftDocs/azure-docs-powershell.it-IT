---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 8002a0a38353022c273aa680ccae9cf354b3540d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988957"
---
# <span data-ttu-id="d648b-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="d648b-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="d648b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d648b-102">SYNOPSIS</span></span>
<span data-ttu-id="d648b-103">Crea o aggiorna un dashboard.</span><span class="sxs-lookup"><span data-stu-id="d648b-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="d648b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d648b-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d648b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d648b-105">DESCRIPTION</span></span>
<span data-ttu-id="d648b-106">Crea o aggiorna un dashboard.</span><span class="sxs-lookup"><span data-stu-id="d648b-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="d648b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d648b-107">EXAMPLES</span></span>

### <span data-ttu-id="d648b-108">Esempio 1: Aggiornare la definizione del dashboard usando un modello di dashboard</span><span class="sxs-lookup"><span data-stu-id="d648b-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="d648b-109">Aggiornare la definizione di una dashboard usando un file modello con trattino.</span><span class="sxs-lookup"><span data-stu-id="d648b-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="d648b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d648b-110">PARAMETERS</span></span>

### <span data-ttu-id="d648b-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="d648b-111">-DashboardPath</span></span>
<span data-ttu-id="d648b-112">Percorso di un modello di dashboard esistente.</span><span class="sxs-lookup"><span data-stu-id="d648b-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="d648b-113">I modelli di dashboard possono essere scaricati dal portale.</span><span class="sxs-lookup"><span data-stu-id="d648b-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="d648b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d648b-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="d648b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d648b-115">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d648b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d648b-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="d648b-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d648b-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="d648b-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d648b-118">-Confirm</span></span>
<span data-ttu-id="d648b-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d648b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d648b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d648b-120">-WhatIf</span></span>
<span data-ttu-id="d648b-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d648b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d648b-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d648b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d648b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d648b-123">CommonParameters</span></span>
<span data-ttu-id="d648b-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d648b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d648b-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d648b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d648b-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="d648b-126">INPUTS</span></span>

## <span data-ttu-id="d648b-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d648b-127">OUTPUTS</span></span>

### <span data-ttu-id="d648b-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="d648b-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="d648b-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="d648b-129">NOTES</span></span>

<span data-ttu-id="d648b-130">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d648b-130">ALIASES</span></span>

## <span data-ttu-id="d648b-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d648b-131">RELATED LINKS</span></span>

