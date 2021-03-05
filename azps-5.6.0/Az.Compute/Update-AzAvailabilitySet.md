---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 4f268ae4278712e16e8efc126702d0130dc225cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964957"
---
# <span data-ttu-id="ff565-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ff565-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="ff565-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff565-102">SYNOPSIS</span></span>
<span data-ttu-id="ff565-103">Aggiorna un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="ff565-103">Updates an availability set.</span></span>

## <span data-ttu-id="ff565-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff565-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff565-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ff565-105">DESCRIPTION</span></span>
<span data-ttu-id="ff565-106">Il cmdlet **Update-AzAvailabilitySet** aggiorna un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="ff565-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="ff565-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff565-107">EXAMPLES</span></span>

### <span data-ttu-id="ff565-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ff565-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="ff565-109">Questo comando aggiorna il set di disponibilità denominato "AvSet01" nel gruppo di risorse denominato "ResourceGroup01" a un set di disponibilità gestito.</span><span class="sxs-lookup"><span data-stu-id="ff565-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="ff565-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff565-110">PARAMETERS</span></span>

### <span data-ttu-id="ff565-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff565-111">-AsJob</span></span>
<span data-ttu-id="ff565-112">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="ff565-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ff565-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ff565-113">-AvailabilitySet</span></span>
<span data-ttu-id="ff565-114">Specifica l'oggetto del set di disponibilità da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="ff565-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff565-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff565-115">-DefaultProfile</span></span>
<span data-ttu-id="ff565-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff565-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff565-117">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="ff565-117">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="ff565-118">ID risorsa del gruppo di posizionamento di prossimità da usare con questo set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="ff565-118">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff565-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="ff565-119">-Sku</span></span>
<span data-ttu-id="ff565-120">Nome della SKU</span><span class="sxs-lookup"><span data-stu-id="ff565-120">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff565-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="ff565-121">-Tag</span></span>
<span data-ttu-id="ff565-122">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ff565-122">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff565-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff565-123">-Confirm</span></span>
<span data-ttu-id="ff565-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff565-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff565-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff565-125">-WhatIf</span></span>
<span data-ttu-id="ff565-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff565-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff565-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff565-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff565-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff565-128">CommonParameters</span></span>
<span data-ttu-id="ff565-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff565-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff565-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ff565-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff565-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="ff565-131">INPUTS</span></span>

### <span data-ttu-id="ff565-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ff565-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="ff565-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff565-133">OUTPUTS</span></span>

### <span data-ttu-id="ff565-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ff565-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="ff565-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="ff565-135">NOTES</span></span>

## <span data-ttu-id="ff565-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff565-136">RELATED LINKS</span></span>
