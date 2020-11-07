---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
ms.openlocfilehash: 2a3f4a6d386f37334908efde31332ed6137ecb74
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675270"
---
# <span data-ttu-id="081b0-101">Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="081b0-101">Remove-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="081b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="081b0-102">SYNOPSIS</span></span>
<span data-ttu-id="081b0-103">Eliminare la risorsa gruppo posizionamento di prossimità.</span><span class="sxs-lookup"><span data-stu-id="081b0-103">Delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="081b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="081b0-104">SYNTAX</span></span>

### <span data-ttu-id="081b0-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="081b0-105">DefaultParameter (Default)</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="081b0-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="081b0-106">ResourceIdParameter</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="081b0-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="081b0-107">ObjectParameter</span></span>
```
Remove-AzProximityPlacementGroup [-InputObject] <PSProximityPlacementGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="081b0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="081b0-108">DESCRIPTION</span></span>
<span data-ttu-id="081b0-109">Questo cmdlet eliminerà le risorse del gruppo di posizionamento di prossimità.</span><span class="sxs-lookup"><span data-stu-id="081b0-109">This cmdlet will delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="081b0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="081b0-110">EXAMPLES</span></span>

### <span data-ttu-id="081b0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="081b0-111">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup  -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName  | Remove-AzureRmProximityPlacementGroup
```

<span data-ttu-id="081b0-112">Questo comando rimuove il gruppo di posizionamento di prossimità assegnato.</span><span class="sxs-lookup"><span data-stu-id="081b0-112">This command removes the given proximity placement group.</span></span>

## <span data-ttu-id="081b0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="081b0-113">PARAMETERS</span></span>

### <span data-ttu-id="081b0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="081b0-114">-AsJob</span></span>
<span data-ttu-id="081b0-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="081b0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="081b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="081b0-116">-DefaultProfile</span></span>
<span data-ttu-id="081b0-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="081b0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="081b0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="081b0-118">-Force</span></span>
<span data-ttu-id="081b0-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="081b0-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="081b0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="081b0-120">-InputObject</span></span>
<span data-ttu-id="081b0-121">Oggetto gruppo posizionamento di prossimità PS</span><span class="sxs-lookup"><span data-stu-id="081b0-121">The PS Proximity Placement Group Object</span></span>

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

### <span data-ttu-id="081b0-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="081b0-122">-Name</span></span>
<span data-ttu-id="081b0-123">Nome del gruppo di posizionamento di prossimità.</span><span class="sxs-lookup"><span data-stu-id="081b0-123">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="081b0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="081b0-124">-ResourceGroupName</span></span>
<span data-ttu-id="081b0-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="081b0-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="081b0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="081b0-126">-ResourceId</span></span>
<span data-ttu-id="081b0-127">ID risorsa per il gruppo di posizionamento di prossimità.</span><span class="sxs-lookup"><span data-stu-id="081b0-127">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="081b0-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="081b0-128">-Confirm</span></span>
<span data-ttu-id="081b0-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="081b0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="081b0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="081b0-130">-WhatIf</span></span>
<span data-ttu-id="081b0-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="081b0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="081b0-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="081b0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="081b0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="081b0-133">CommonParameters</span></span>
<span data-ttu-id="081b0-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="081b0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="081b0-135">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="081b0-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="081b0-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="081b0-136">INPUTS</span></span>

### <span data-ttu-id="081b0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="081b0-137">System.String</span></span>

### <span data-ttu-id="081b0-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="081b0-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="081b0-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="081b0-139">OUTPUTS</span></span>

### <span data-ttu-id="081b0-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="081b0-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="081b0-141">Note</span><span class="sxs-lookup"><span data-stu-id="081b0-141">NOTES</span></span>

## <span data-ttu-id="081b0-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="081b0-142">RELATED LINKS</span></span>
