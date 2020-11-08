---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: a6308120303684a8e87280ef903056361fbaf848
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031911"
---
# <span data-ttu-id="dd08c-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="dd08c-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="dd08c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd08c-102">SYNOPSIS</span></span>
<span data-ttu-id="dd08c-103">Ottenere o elencare le risorse del gruppo posizionamento di prossimità.</span><span class="sxs-lookup"><span data-stu-id="dd08c-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="dd08c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd08c-104">SYNTAX</span></span>

### <span data-ttu-id="dd08c-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dd08c-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-ColocationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd08c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="dd08c-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ColocationStatus] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd08c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd08c-107">DESCRIPTION</span></span>
<span data-ttu-id="dd08c-108">Questo cmdlet otterrà o elenca le risorse del gruppo di posizionamento di prossimità.</span><span class="sxs-lookup"><span data-stu-id="dd08c-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="dd08c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd08c-109">EXAMPLES</span></span>

### <span data-ttu-id="dd08c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dd08c-110">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
VirtualMachines             : {}
VirtualMachineScaleSets     : {}
AvailabilitySets            : {}
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {[key1, val1]}
```

<span data-ttu-id="dd08c-111">Questo comando ottiene il gruppo posizionamento di prossimità</span><span class="sxs-lookup"><span data-stu-id="dd08c-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="dd08c-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="dd08c-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="dd08c-113">Questo comando elenca tutti i gruppi di posizionamento di prossimità in un gruppo di risorse specifico.</span><span class="sxs-lookup"><span data-stu-id="dd08c-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="dd08c-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="dd08c-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="dd08c-115">Questo comando elenca tutti i gruppi di posizionamento di prossimità sotto l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="dd08c-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="dd08c-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd08c-116">PARAMETERS</span></span>

### <span data-ttu-id="dd08c-117">-ColocationStatus</span><span class="sxs-lookup"><span data-stu-id="dd08c-117">-ColocationStatus</span></span>
<span data-ttu-id="dd08c-118">Mostra lo stato di Colocation di una risorsa nel gruppo posizionamento di prossimità.</span><span class="sxs-lookup"><span data-stu-id="dd08c-118">Shows the colocation status of a resource in the proximity placement group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd08c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd08c-119">-DefaultProfile</span></span>
<span data-ttu-id="dd08c-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd08c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd08c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd08c-121">-Name</span></span>
<span data-ttu-id="dd08c-122">Nome del gruppo di posizionamento di prossimità.</span><span class="sxs-lookup"><span data-stu-id="dd08c-122">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dd08c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd08c-123">-ResourceGroupName</span></span>
<span data-ttu-id="dd08c-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dd08c-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dd08c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd08c-125">-ResourceId</span></span>
<span data-ttu-id="dd08c-126">ID risorsa per il gruppo di posizionamento di prossimità.</span><span class="sxs-lookup"><span data-stu-id="dd08c-126">The resource id for the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd08c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd08c-127">CommonParameters</span></span>
<span data-ttu-id="dd08c-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd08c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd08c-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd08c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd08c-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd08c-130">INPUTS</span></span>

### <span data-ttu-id="dd08c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dd08c-131">System.String</span></span>

## <span data-ttu-id="dd08c-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd08c-132">OUTPUTS</span></span>

### <span data-ttu-id="dd08c-133">Microsoft. Azure. Commands. Compute. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="dd08c-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="dd08c-134">Note</span><span class="sxs-lookup"><span data-stu-id="dd08c-134">NOTES</span></span>

## <span data-ttu-id="dd08c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd08c-135">RELATED LINKS</span></span>
