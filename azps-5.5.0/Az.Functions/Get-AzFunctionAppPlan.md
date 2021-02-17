---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
ms.openlocfilehash: d08d050253842e13967d001889e1b7d1b331ce17
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192479"
---
# <span data-ttu-id="9c84f-101">Get-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="9c84f-101">Get-AzFunctionAppPlan</span></span>

## <span data-ttu-id="9c84f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c84f-102">SYNOPSIS</span></span>
<span data-ttu-id="9c84f-103">Ottenere i piani delle app per le funzioni in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9c84f-103">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="9c84f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c84f-104">SYNTAX</span></span>

### <span data-ttu-id="9c84f-105">GetAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9c84f-105">GetAll (Default)</span></span>
```
Get-AzFunctionAppPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9c84f-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="9c84f-106">ByLocation</span></span>
```
Get-AzFunctionAppPlan -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c84f-107">ByName</span><span class="sxs-lookup"><span data-stu-id="9c84f-107">ByName</span></span>
```
Get-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9c84f-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c84f-108">ByResourceGroupName</span></span>
```
Get-AzFunctionAppPlan [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c84f-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9c84f-109">DESCRIPTION</span></span>
<span data-ttu-id="9c84f-110">Ottenere i piani delle app per le funzioni in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9c84f-110">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="9c84f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c84f-111">EXAMPLES</span></span>

### <span data-ttu-id="9c84f-112">Esempio 1: Ottenere tutti i piani dell'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="9c84f-112">Example 1: Get all function app plans.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium428118799    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium677505437    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium711892854    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium819994758    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="9c84f-113">Questo comando recupera tutti i piani dell'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="9c84f-113">This command gets all function app plans.</span></span>

### <span data-ttu-id="9c84f-114">Esempio 2: Ottenere i piani dell'app per le funzioni in base al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9c84f-114">Example 2: Get function app plans by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -ResourceGroupName "West Europe"

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="9c84f-115">Questo comando recupera i piani delle app per le funzioni in base al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9c84f-115">This command gets function app plans by resource group name.</span></span>

### <span data-ttu-id="9c84f-116">Esempio 3: Ottenere i piani dell'app per le funzioni per gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="9c84f-116">Example 3: Get function app plans for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8z

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8z
```

<span data-ttu-id="9c84f-117">Questo comando ottiene i piani dell'app per le funzioni per gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="9c84f-117">This command gets function app plans for the given subscriptions.</span></span>

### <span data-ttu-id="9c84f-118">Esempio 4: Ottenere i piani delle app per le funzioni in base alla posizione.</span><span class="sxs-lookup"><span data-stu-id="9c84f-118">Example 4: Get function app plans by location.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Location "Central US"

Name                               WorkerType SkuTier        SkuName Location   ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------   -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     Central US Func99-West-Europe-Win-Premium   3r16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="9c84f-119">Questo comando recupera i piani delle app per le funzioni in base alla posizione.</span><span class="sxs-lookup"><span data-stu-id="9c84f-119">This command gets function app plans by location.</span></span>

## <span data-ttu-id="9c84f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c84f-120">PARAMETERS</span></span>

### <span data-ttu-id="9c84f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c84f-121">-DefaultProfile</span></span>
<span data-ttu-id="9c84f-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c84f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c84f-123">-Location</span><span class="sxs-lookup"><span data-stu-id="9c84f-123">-Location</span></span>
<span data-ttu-id="9c84f-124">Posizione del piano dell'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="9c84f-124">The location of the function app plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c84f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9c84f-125">-Name</span></span>
<span data-ttu-id="9c84f-126">Nome del piano di servizio.</span><span class="sxs-lookup"><span data-stu-id="9c84f-126">The service plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c84f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c84f-127">-ResourceGroupName</span></span>
<span data-ttu-id="9c84f-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9c84f-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c84f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c84f-129">-SubscriptionId</span></span>
<span data-ttu-id="9c84f-130">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9c84f-130">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c84f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c84f-131">CommonParameters</span></span>
<span data-ttu-id="9c84f-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c84f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c84f-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9c84f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c84f-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="9c84f-134">INPUTS</span></span>

## <span data-ttu-id="9c84f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c84f-135">OUTPUTS</span></span>

### <span data-ttu-id="9c84f-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9c84f-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="9c84f-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="9c84f-137">NOTES</span></span>

<span data-ttu-id="9c84f-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9c84f-138">ALIASES</span></span>

## <span data-ttu-id="9c84f-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c84f-139">RELATED LINKS</span></span>

