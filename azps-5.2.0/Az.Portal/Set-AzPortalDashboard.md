---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 60569a05fc3770119844b05e65ec3dc7989a85ec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331255"
---
# <span data-ttu-id="92a77-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="92a77-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="92a77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92a77-102">SYNOPSIS</span></span>
<span data-ttu-id="92a77-103">Crea o aggiorna un dashboard.</span><span class="sxs-lookup"><span data-stu-id="92a77-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="92a77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92a77-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="92a77-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92a77-105">DESCRIPTION</span></span>
<span data-ttu-id="92a77-106">Crea o aggiorna un dashboard.</span><span class="sxs-lookup"><span data-stu-id="92a77-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="92a77-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92a77-107">EXAMPLES</span></span>

### <span data-ttu-id="92a77-108">Esempio 1: aggiornare la definizione del dashboard usando un modello di dashboard</span><span class="sxs-lookup"><span data-stu-id="92a77-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="92a77-109">Aggiornare una definizione di dashboard usando un file di modello dashbaord.</span><span class="sxs-lookup"><span data-stu-id="92a77-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="92a77-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92a77-110">PARAMETERS</span></span>

### <span data-ttu-id="92a77-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="92a77-111">-DashboardPath</span></span>
<span data-ttu-id="92a77-112">Il percorso di un modello di dashboard esistente.</span><span class="sxs-lookup"><span data-stu-id="92a77-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="92a77-113">I modelli di dashboard possono essere scaricati dal portale.</span><span class="sxs-lookup"><span data-stu-id="92a77-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="92a77-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a77-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="92a77-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="92a77-115">-Name</span></span>


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

### <span data-ttu-id="92a77-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92a77-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="92a77-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92a77-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="92a77-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="92a77-118">-Confirm</span></span>
<span data-ttu-id="92a77-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92a77-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92a77-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92a77-120">-WhatIf</span></span>
<span data-ttu-id="92a77-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92a77-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92a77-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92a77-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92a77-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a77-123">CommonParameters</span></span>
<span data-ttu-id="92a77-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92a77-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a77-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92a77-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a77-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92a77-126">INPUTS</span></span>

## <span data-ttu-id="92a77-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92a77-127">OUTPUTS</span></span>

### <span data-ttu-id="92a77-128">Microsoft. Azure. PowerShell. Cmdlets. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="92a77-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="92a77-129">Note</span><span class="sxs-lookup"><span data-stu-id="92a77-129">NOTES</span></span>

<span data-ttu-id="92a77-130">ALIAS</span><span class="sxs-lookup"><span data-stu-id="92a77-130">ALIASES</span></span>

## <span data-ttu-id="92a77-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92a77-131">RELATED LINKS</span></span>

