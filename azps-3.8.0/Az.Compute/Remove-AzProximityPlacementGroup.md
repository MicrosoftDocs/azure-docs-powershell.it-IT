---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
ms.openlocfilehash: 07adbff46713136ec412d10bd428765230e1838c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865495"
---
# <span data-ttu-id="131a9-101">Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="131a9-101">Remove-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="131a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="131a9-102">SYNOPSIS</span></span>
<span data-ttu-id="131a9-103">Eliminare la risorsa gruppo posizionamento di prossimità.</span><span class="sxs-lookup"><span data-stu-id="131a9-103">Delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="131a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="131a9-104">SYNTAX</span></span>

### <span data-ttu-id="131a9-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="131a9-105">DefaultParameter (Default)</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="131a9-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="131a9-106">ResourceIdParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="131a9-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="131a9-107">ObjectParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-InputObject] <PSProximityPlacementGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="131a9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="131a9-108">DESCRIPTION</span></span>
<span data-ttu-id="131a9-109">Questo cmdlet eliminerà le risorse del gruppo di posizionamento di prossimità.</span><span class="sxs-lookup"><span data-stu-id="131a9-109">This cmdlet will delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="131a9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="131a9-110">EXAMPLES</span></span>

### <span data-ttu-id="131a9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="131a9-111">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup  -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName  | Remove-AzureRmProximityPlacementGroup
```

<span data-ttu-id="131a9-112">Questo comando rimuove il gruppo di posizionamento di prossimità assegnato.</span><span class="sxs-lookup"><span data-stu-id="131a9-112">This command removes the given proximity placement group.</span></span>

## <span data-ttu-id="131a9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="131a9-113">PARAMETERS</span></span>

### <span data-ttu-id="131a9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="131a9-114">-AsJob</span></span>
<span data-ttu-id="131a9-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="131a9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="131a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="131a9-116">-DefaultProfile</span></span>
<span data-ttu-id="131a9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="131a9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="131a9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="131a9-118">-Force</span></span>
<span data-ttu-id="131a9-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="131a9-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="131a9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="131a9-120">-InputObject</span></span>
<span data-ttu-id="131a9-121">Oggetto gruppo posizionamento di prossimità PS</span><span class="sxs-lookup"><span data-stu-id="131a9-121">The PS Proximity Placement Group Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup
Parameter Sets: ObjectParameter
Aliases: ProximityPlacementGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="131a9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="131a9-122">-Name</span></span>
<span data-ttu-id="131a9-123">Nome del gruppo di posizionamento di prossimità.</span><span class="sxs-lookup"><span data-stu-id="131a9-123">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131a9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="131a9-124">-ResourceGroupName</span></span>
<span data-ttu-id="131a9-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="131a9-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131a9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="131a9-126">-ResourceId</span></span>
<span data-ttu-id="131a9-127">ID risorsa per il gruppo di posizionamento di prossimità.</span><span class="sxs-lookup"><span data-stu-id="131a9-127">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="131a9-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="131a9-128">-Confirm</span></span>
<span data-ttu-id="131a9-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="131a9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="131a9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="131a9-130">-WhatIf</span></span>
<span data-ttu-id="131a9-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="131a9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="131a9-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="131a9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="131a9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="131a9-133">CommonParameters</span></span>
<span data-ttu-id="131a9-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="131a9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="131a9-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="131a9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="131a9-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="131a9-136">INPUTS</span></span>

### <span data-ttu-id="131a9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="131a9-137">System.String</span></span>

### <span data-ttu-id="131a9-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="131a9-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="131a9-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="131a9-139">OUTPUTS</span></span>

### <span data-ttu-id="131a9-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="131a9-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="131a9-141">Note</span><span class="sxs-lookup"><span data-stu-id="131a9-141">NOTES</span></span>

## <span data-ttu-id="131a9-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="131a9-142">RELATED LINKS</span></span>
