---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: f7d9181b5ec79434928fc8d291025aea9480b8e9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867122"
---
# <span data-ttu-id="4c021-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4c021-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="4c021-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c021-102">SYNOPSIS</span></span>
<span data-ttu-id="4c021-103">Aggiorna un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="4c021-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c021-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c021-104">SYNTAX</span></span>

### <span data-ttu-id="4c021-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c021-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c021-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="4c021-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c021-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c021-107">DESCRIPTION</span></span>
<span data-ttu-id="4c021-108">Il cmdlet **Update-AzureRmAvailabilitySet** aggiorna un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="4c021-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="4c021-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c021-109">EXAMPLES</span></span>

### <span data-ttu-id="4c021-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4c021-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="4c021-111">Questo comando Aggiorna il set di disponibilità denominato "AvSet01" nel gruppo di risorse denominato "ResourceGroup01" in un set di disponibilità gestita.</span><span class="sxs-lookup"><span data-stu-id="4c021-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="4c021-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c021-112">PARAMETERS</span></span>

### <span data-ttu-id="4c021-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c021-113">-AsJob</span></span>
<span data-ttu-id="4c021-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="4c021-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c021-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4c021-115">-AvailabilitySet</span></span>
<span data-ttu-id="4c021-116">Specifica l'oggetto set di disponibilità da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="4c021-116">Specifies the availability set object to be updated.</span></span>

```yaml
Type: PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c021-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c021-117">-DefaultProfile</span></span>
<span data-ttu-id="4c021-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c021-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c021-119">-Managed</span><span class="sxs-lookup"><span data-stu-id="4c021-119">-Managed</span></span>
<span data-ttu-id="4c021-120">Set di disponibilità gestita</span><span class="sxs-lookup"><span data-stu-id="4c021-120">Managed Availability Set</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c021-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="4c021-121">-Sku</span></span>
<span data-ttu-id="4c021-122">Nome della SKU</span><span class="sxs-lookup"><span data-stu-id="4c021-122">The Name of Sku</span></span>

```yaml
Type: String
Parameter Sets: SkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c021-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4c021-123">-Confirm</span></span>
<span data-ttu-id="4c021-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c021-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c021-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c021-125">-WhatIf</span></span>
<span data-ttu-id="4c021-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c021-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c021-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c021-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c021-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c021-128">CommonParameters</span></span>
<span data-ttu-id="4c021-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c021-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c021-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c021-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c021-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c021-131">INPUTS</span></span>

### <span data-ttu-id="4c021-132">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4c021-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="4c021-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c021-133">OUTPUTS</span></span>

### <span data-ttu-id="4c021-134">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4c021-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="4c021-135">Note</span><span class="sxs-lookup"><span data-stu-id="4c021-135">NOTES</span></span>

## <span data-ttu-id="4c021-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c021-136">RELATED LINKS</span></span>

