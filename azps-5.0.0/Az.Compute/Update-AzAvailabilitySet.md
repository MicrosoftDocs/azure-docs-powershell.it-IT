---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 689336bb7fbb7ef59be96a5bd6bcbfe49ddb64c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200230"
---
# <span data-ttu-id="91c2a-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="91c2a-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="91c2a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="91c2a-103">Aggiorna un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="91c2a-103">Updates an availability set.</span></span>

## <span data-ttu-id="91c2a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91c2a-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91c2a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91c2a-105">DESCRIPTION</span></span>
<span data-ttu-id="91c2a-106">Il cmdlet **Update-AzAvailabilitySet** aggiorna un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="91c2a-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="91c2a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91c2a-107">EXAMPLES</span></span>

### <span data-ttu-id="91c2a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="91c2a-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="91c2a-109">Questo comando Aggiorna il set di disponibilità denominato "AvSet01" nel gruppo di risorse denominato "ResourceGroup01" in un set di disponibilità gestita.</span><span class="sxs-lookup"><span data-stu-id="91c2a-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="91c2a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91c2a-110">PARAMETERS</span></span>

### <span data-ttu-id="91c2a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91c2a-111">-AsJob</span></span>
<span data-ttu-id="91c2a-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="91c2a-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="91c2a-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="91c2a-113">-AvailabilitySet</span></span>
<span data-ttu-id="91c2a-114">Specifica l'oggetto set di disponibilità da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="91c2a-114">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="91c2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c2a-115">-DefaultProfile</span></span>
<span data-ttu-id="91c2a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91c2a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91c2a-117">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="91c2a-117">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="91c2a-118">ID risorsa del gruppo di posizionamento di prossimità da usare con questo set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="91c2a-118">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="91c2a-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="91c2a-119">-Sku</span></span>
<span data-ttu-id="91c2a-120">Nome della SKU</span><span class="sxs-lookup"><span data-stu-id="91c2a-120">The Name of Sku</span></span>

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

### <span data-ttu-id="91c2a-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="91c2a-121">-Tag</span></span>
<span data-ttu-id="91c2a-122">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="91c2a-122">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="91c2a-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="91c2a-123">-Confirm</span></span>
<span data-ttu-id="91c2a-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91c2a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91c2a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91c2a-125">-WhatIf</span></span>
<span data-ttu-id="91c2a-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91c2a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91c2a-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91c2a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91c2a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c2a-128">CommonParameters</span></span>
<span data-ttu-id="91c2a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91c2a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c2a-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91c2a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c2a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91c2a-131">INPUTS</span></span>

### <span data-ttu-id="91c2a-132">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="91c2a-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="91c2a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91c2a-133">OUTPUTS</span></span>

### <span data-ttu-id="91c2a-134">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="91c2a-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="91c2a-135">Note</span><span class="sxs-lookup"><span data-stu-id="91c2a-135">NOTES</span></span>

## <span data-ttu-id="91c2a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91c2a-136">RELATED LINKS</span></span>