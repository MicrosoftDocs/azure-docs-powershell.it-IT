---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 7e460c866912387b05a55b6fd228c65ef9b68348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508292"
---
# <span data-ttu-id="9d581-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9d581-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="9d581-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d581-102">SYNOPSIS</span></span>
<span data-ttu-id="9d581-103">Aggiorna un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="9d581-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d581-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d581-104">SYNTAX</span></span>

### <span data-ttu-id="9d581-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d581-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d581-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="9d581-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d581-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d581-107">DESCRIPTION</span></span>
<span data-ttu-id="9d581-108">Il cmdlet **Update-AzureRmAvailabilitySet** aggiorna un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="9d581-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="9d581-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d581-109">EXAMPLES</span></span>

### <span data-ttu-id="9d581-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9d581-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="9d581-111">Questo comando Aggiorna il set di disponibilità denominato "AvSet01" nel gruppo di risorse denominato "ResourceGroup01" in un set di disponibilità gestita.</span><span class="sxs-lookup"><span data-stu-id="9d581-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="9d581-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d581-112">PARAMETERS</span></span>

### <span data-ttu-id="9d581-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9d581-113">-AvailabilitySet</span></span>
<span data-ttu-id="9d581-114">Specifica l'oggetto set di disponibilità da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="9d581-114">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="9d581-115">-Managed</span><span class="sxs-lookup"><span data-stu-id="9d581-115">-Managed</span></span>
<span data-ttu-id="9d581-116">Set di disponibilità gestita</span><span class="sxs-lookup"><span data-stu-id="9d581-116">Managed Availability Set</span></span>

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

### <span data-ttu-id="9d581-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="9d581-117">-Sku</span></span>
<span data-ttu-id="9d581-118">Nome della SKU</span><span class="sxs-lookup"><span data-stu-id="9d581-118">The Name of Sku</span></span>

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

### <span data-ttu-id="9d581-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9d581-119">-Confirm</span></span>
<span data-ttu-id="9d581-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d581-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d581-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d581-121">-WhatIf</span></span>
<span data-ttu-id="9d581-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d581-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d581-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d581-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d581-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d581-124">CommonParameters</span></span>
<span data-ttu-id="9d581-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d581-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d581-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d581-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d581-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d581-127">INPUTS</span></span>

### <span data-ttu-id="9d581-128">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9d581-128">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="9d581-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d581-129">OUTPUTS</span></span>

### <span data-ttu-id="9d581-130">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9d581-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="9d581-131">Note</span><span class="sxs-lookup"><span data-stu-id="9d581-131">NOTES</span></span>

## <span data-ttu-id="9d581-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d581-132">RELATED LINKS</span></span>

