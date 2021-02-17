---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: a81bb1515e25f9000438fbd463117e4fd69b9690
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209443"
---
# <span data-ttu-id="3623c-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="3623c-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="3623c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3623c-102">SYNOPSIS</span></span>
<span data-ttu-id="3623c-103">Recupera le app con funzioni in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3623c-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="3623c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3623c-104">SYNTAX</span></span>

### <span data-ttu-id="3623c-105">GetAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3623c-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3623c-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="3623c-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3623c-107">ByName</span><span class="sxs-lookup"><span data-stu-id="3623c-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3623c-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3623c-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3623c-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3623c-109">DESCRIPTION</span></span>
<span data-ttu-id="3623c-110">Recupera le app con funzioni in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3623c-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="3623c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3623c-111">EXAMPLES</span></span>

### <span data-ttu-id="3623c-112">Esempio 1: Ottenere tutte le app con funzioni.</span><span class="sxs-lookup"><span data-stu-id="3623c-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="3623c-113">Esempio 2: Ottenere le app con funzioni in base al nome.</span><span class="sxs-lookup"><span data-stu-id="3623c-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="3623c-114">Esempio 3: Ottenere app con funzioni in base al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3623c-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="3623c-115">Esempio 4: Ottenere app con funzioni per gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="3623c-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="3623c-116">Esempio 5: Ottenere le app con funzioni in base alla posizione.</span><span class="sxs-lookup"><span data-stu-id="3623c-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="3623c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3623c-117">PARAMETERS</span></span>

### <span data-ttu-id="3623c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3623c-118">-DefaultProfile</span></span>
<span data-ttu-id="3623c-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3623c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3623c-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="3623c-120">-IncludeSlot</span></span>
<span data-ttu-id="3623c-121">Consente di specificare se includere gli slot di distribuzione nei risultati.</span><span class="sxs-lookup"><span data-stu-id="3623c-121">Use to specify whether to include deployment slots in results.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3623c-122">-Location</span><span class="sxs-lookup"><span data-stu-id="3623c-122">-Location</span></span>
<span data-ttu-id="3623c-123">Posizione dell'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="3623c-123">The location of the function app.</span></span>

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

### <span data-ttu-id="3623c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3623c-124">-Name</span></span>
<span data-ttu-id="3623c-125">Nome dell'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="3623c-125">The name of the function app.</span></span>

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

### <span data-ttu-id="3623c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3623c-126">-ResourceGroupName</span></span>
<span data-ttu-id="3623c-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3623c-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="3623c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3623c-128">-SubscriptionId</span></span>
<span data-ttu-id="3623c-129">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3623c-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="3623c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3623c-130">CommonParameters</span></span>
<span data-ttu-id="3623c-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3623c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3623c-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3623c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3623c-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="3623c-133">INPUTS</span></span>

## <span data-ttu-id="3623c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3623c-134">OUTPUTS</span></span>

### <span data-ttu-id="3623c-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="3623c-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="3623c-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="3623c-136">NOTES</span></span>

<span data-ttu-id="3623c-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3623c-137">ALIASES</span></span>

## <span data-ttu-id="3623c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3623c-138">RELATED LINKS</span></span>

