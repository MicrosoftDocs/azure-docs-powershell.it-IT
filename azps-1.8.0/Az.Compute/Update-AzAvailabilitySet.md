---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 4051cbb697625f527afdf2e189953c4d6e776214
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836611"
---
# <span data-ttu-id="95fb4-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="95fb4-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="95fb4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="95fb4-103">Aggiorna un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="95fb4-103">Updates an availability set.</span></span>

## <span data-ttu-id="95fb4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95fb4-104">SYNTAX</span></span>

### <span data-ttu-id="95fb4-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="95fb4-105">SkuParameterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95fb4-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="95fb4-106">ManagedParamterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95fb4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95fb4-107">DESCRIPTION</span></span>
<span data-ttu-id="95fb4-108">Il cmdlet **Update-AzAvailabilitySet** aggiorna un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="95fb4-108">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="95fb4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95fb4-109">EXAMPLES</span></span>

### <span data-ttu-id="95fb4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="95fb4-110">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="95fb4-111">Questo comando Aggiorna il set di disponibilità denominato "AvSet01" nel gruppo di risorse denominato "ResourceGroup01" in un set di disponibilità gestita.</span><span class="sxs-lookup"><span data-stu-id="95fb4-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="95fb4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95fb4-112">PARAMETERS</span></span>

### <span data-ttu-id="95fb4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95fb4-113">-AsJob</span></span>
<span data-ttu-id="95fb4-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="95fb4-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="95fb4-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="95fb4-115">-AvailabilitySet</span></span>
<span data-ttu-id="95fb4-116">Specifica l'oggetto set di disponibilità da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="95fb4-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="95fb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95fb4-117">-DefaultProfile</span></span>
<span data-ttu-id="95fb4-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95fb4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95fb4-119">-Managed</span><span class="sxs-lookup"><span data-stu-id="95fb4-119">-Managed</span></span>
<span data-ttu-id="95fb4-120">Set di disponibilità gestita</span><span class="sxs-lookup"><span data-stu-id="95fb4-120">Managed Availability Set</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95fb4-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="95fb4-121">-Sku</span></span>
<span data-ttu-id="95fb4-122">Nome della SKU</span><span class="sxs-lookup"><span data-stu-id="95fb4-122">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: SkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95fb4-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="95fb4-123">-Tag</span></span>
<span data-ttu-id="95fb4-124">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="95fb4-124">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="95fb4-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="95fb4-125">-Confirm</span></span>
<span data-ttu-id="95fb4-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95fb4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95fb4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95fb4-127">-WhatIf</span></span>
<span data-ttu-id="95fb4-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95fb4-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95fb4-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95fb4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95fb4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95fb4-130">CommonParameters</span></span>
<span data-ttu-id="95fb4-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95fb4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95fb4-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95fb4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95fb4-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95fb4-133">INPUTS</span></span>

### <span data-ttu-id="95fb4-134">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="95fb4-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="95fb4-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95fb4-135">OUTPUTS</span></span>

### <span data-ttu-id="95fb4-136">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="95fb4-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="95fb4-137">Note</span><span class="sxs-lookup"><span data-stu-id="95fb4-137">NOTES</span></span>

## <span data-ttu-id="95fb4-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95fb4-138">RELATED LINKS</span></span>
