---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: 6a3a421f1da374db1cc08635891bdeec4375855a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190730"
---
# <span data-ttu-id="3e581-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="3e581-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="3e581-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e581-102">SYNOPSIS</span></span>
<span data-ttu-id="3e581-103">Ottiene le app di funzione in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3e581-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="3e581-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e581-104">SYNTAX</span></span>

### <span data-ttu-id="3e581-105">GetAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3e581-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-IncludeSlot] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e581-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="3e581-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-IncludeSlot] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e581-107">ByName</span><span class="sxs-lookup"><span data-stu-id="3e581-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3e581-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e581-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3e581-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e581-109">DESCRIPTION</span></span>
<span data-ttu-id="3e581-110">Ottiene le app di funzione in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3e581-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="3e581-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e581-111">EXAMPLES</span></span>

### <span data-ttu-id="3e581-112">Esempio 1: ottenere tutte le app funzione.</span><span class="sxs-lookup"><span data-stu-id="3e581-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="3e581-113">Esempio 2: ottenere le app di funzione per nome.</span><span class="sxs-lookup"><span data-stu-id="3e581-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="3e581-114">Esempio 3: ottenere le app funzioni in base al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3e581-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="3e581-115">Esempio 4: ottenere le app di funzione per gli abbonamenti specificati.</span><span class="sxs-lookup"><span data-stu-id="3e581-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="3e581-116">Esempio 5: ottenere le app di funzione in base alla posizione.</span><span class="sxs-lookup"><span data-stu-id="3e581-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="3e581-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e581-117">PARAMETERS</span></span>

### <span data-ttu-id="3e581-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e581-118">-DefaultProfile</span></span>
<span data-ttu-id="3e581-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e581-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e581-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="3e581-120">-IncludeSlot</span></span>
<span data-ttu-id="3e581-121">Consente di specificare se includere gli slot di distribuzione nei risultati.</span><span class="sxs-lookup"><span data-stu-id="3e581-121">Use to specify whether to include deployment slots in results.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e581-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3e581-122">-Location</span></span>
<span data-ttu-id="3e581-123">Posizione dell'app funzione.</span><span class="sxs-lookup"><span data-stu-id="3e581-123">The location of the function app.</span></span>

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

### <span data-ttu-id="3e581-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e581-124">-Name</span></span>
<span data-ttu-id="3e581-125">Nome dell'app funzione.</span><span class="sxs-lookup"><span data-stu-id="3e581-125">The name of the function app.</span></span>

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

### <span data-ttu-id="3e581-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e581-126">-ResourceGroupName</span></span>
<span data-ttu-id="3e581-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3e581-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="3e581-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e581-128">-SubscriptionId</span></span>
<span data-ttu-id="3e581-129">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="3e581-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="3e581-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e581-130">CommonParameters</span></span>
<span data-ttu-id="3e581-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e581-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e581-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e581-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e581-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e581-133">INPUTS</span></span>

## <span data-ttu-id="3e581-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e581-134">OUTPUTS</span></span>

### <span data-ttu-id="3e581-135">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="3e581-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="3e581-136">Note</span><span class="sxs-lookup"><span data-stu-id="3e581-136">NOTES</span></span>

<span data-ttu-id="3e581-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3e581-137">ALIASES</span></span>

## <span data-ttu-id="3e581-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e581-138">RELATED LINKS</span></span>

