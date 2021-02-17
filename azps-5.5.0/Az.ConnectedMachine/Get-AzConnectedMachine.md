---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
ms.openlocfilehash: afb6a5bab6c2761095fb3ab69a2898aeeb53b45c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209923"
---
# <span data-ttu-id="545a2-101">Get-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="545a2-101">Get-AzConnectedMachine</span></span>

## <span data-ttu-id="545a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="545a2-102">SYNOPSIS</span></span>
<span data-ttu-id="545a2-103">Recupera informazioni sulla visualizzazione modello o sulla visualizzazione dell'istanza di un computer ibrido.</span><span class="sxs-lookup"><span data-stu-id="545a2-103">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="545a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="545a2-104">SYNTAX</span></span>

### <span data-ttu-id="545a2-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="545a2-105">List1 (Default)</span></span>
```
Get-AzConnectedMachine [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="545a2-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="545a2-106">Get</span></span>
```
Get-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="545a2-107">Elenco</span><span class="sxs-lookup"><span data-stu-id="545a2-107">List</span></span>
```
Get-AzConnectedMachine -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="545a2-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="545a2-108">DESCRIPTION</span></span>
<span data-ttu-id="545a2-109">Recupera informazioni sulla visualizzazione modello o sulla visualizzazione dell'istanza di un computer ibrido.</span><span class="sxs-lookup"><span data-stu-id="545a2-109">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="545a2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="545a2-110">EXAMPLES</span></span>

### <span data-ttu-id="545a2-111">Esempio 1: Elencare tutti i computer connessi in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="545a2-111">Example 1: List all connected machines in a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -SubscriptionId 67379433-5e19-4702-b39a-c0a03ca8d20c

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
linwestus2_1   westus2  linux    Connected  Succeeded
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded

```

<span data-ttu-id="545a2-112">Elenca tutti i computer connessi in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="545a2-112">Lists all connected machines in a subscription.</span></span>
<span data-ttu-id="545a2-113">Se non viene specificato l'abbonamento, userà quello del contesto corrente di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="545a2-113">If subscription isn't specified, it will use the subscription from your current Azure PowerShell context.</span></span>

### <span data-ttu-id="545a2-114">Esempio 2: Elencare tutti i computer connessi in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="545a2-114">Example 2: List all connected machines in a resource group</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="545a2-115">Elencare tutti i computer connessi in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="545a2-115">List all connected machines in a resource group.</span></span>

### <span data-ttu-id="545a2-116">Esempio 3: Ottenere un computer connesso in un gruppo di risorse in base al nome</span><span class="sxs-lookup"><span data-stu-id="545a2-116">Example 3: Get a connected machine in a resource group by name</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name winwestus2_1

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="545a2-117">Ottenere un computer connesso in un gruppo di risorse in base al nome.</span><span class="sxs-lookup"><span data-stu-id="545a2-117">Get a connected machine in a resource group by name.</span></span>

## <span data-ttu-id="545a2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="545a2-118">PARAMETERS</span></span>

### <span data-ttu-id="545a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="545a2-119">-DefaultProfile</span></span>
<span data-ttu-id="545a2-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="545a2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="545a2-121">-Expand</span><span class="sxs-lookup"><span data-stu-id="545a2-121">-Expand</span></span>
<span data-ttu-id="545a2-122">Espressione di espansione da applicare all'operazione.</span><span class="sxs-lookup"><span data-stu-id="545a2-122">The expand expression to apply on the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Support.InstanceViewTypes
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545a2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="545a2-123">-Name</span></span>
<span data-ttu-id="545a2-124">Nome del computer ibrido.</span><span class="sxs-lookup"><span data-stu-id="545a2-124">The name of the hybrid machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545a2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="545a2-125">-ResourceGroupName</span></span>
<span data-ttu-id="545a2-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="545a2-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545a2-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="545a2-127">-SubscriptionId</span></span>
<span data-ttu-id="545a2-128">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="545a2-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="545a2-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="545a2-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="545a2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545a2-130">CommonParameters</span></span>
<span data-ttu-id="545a2-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="545a2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545a2-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="545a2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545a2-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="545a2-133">INPUTS</span></span>

## <span data-ttu-id="545a2-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="545a2-134">OUTPUTS</span></span>

### <span data-ttu-id="545a2-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span><span class="sxs-lookup"><span data-stu-id="545a2-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span></span>

## <span data-ttu-id="545a2-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="545a2-136">NOTES</span></span>

<span data-ttu-id="545a2-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="545a2-137">ALIASES</span></span>

## <span data-ttu-id="545a2-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="545a2-138">RELATED LINKS</span></span>

