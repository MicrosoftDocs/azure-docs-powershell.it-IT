---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: c7b33e3f2afd013b6fd54f6d425c0aa1d0d08bd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521728"
---
# <span data-ttu-id="66bf0-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="66bf0-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="66bf0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="66bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="66bf0-103">Aggiorna un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="66bf0-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66bf0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66bf0-104">SYNTAX</span></span>

### <span data-ttu-id="66bf0-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="66bf0-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66bf0-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="66bf0-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66bf0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66bf0-107">DESCRIPTION</span></span>
<span data-ttu-id="66bf0-108">Il cmdlet **Update-AzureRmAvailabilitySet** aggiorna un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="66bf0-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="66bf0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66bf0-109">EXAMPLES</span></span>

### <span data-ttu-id="66bf0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="66bf0-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="66bf0-111">Questo comando Aggiorna il set di disponibilità denominato "AvSet01" nel gruppo di risorse denominato "ResourceGroup01" in un set di disponibilità gestita.</span><span class="sxs-lookup"><span data-stu-id="66bf0-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="66bf0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="66bf0-112">PARAMETERS</span></span>

### <span data-ttu-id="66bf0-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="66bf0-113">-AvailabilitySet</span></span>
<span data-ttu-id="66bf0-114">Specifica l'oggetto set di disponibilità da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="66bf0-114">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="66bf0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66bf0-115">-DefaultProfile</span></span>
<span data-ttu-id="66bf0-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="66bf0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66bf0-117">-Managed</span><span class="sxs-lookup"><span data-stu-id="66bf0-117">-Managed</span></span>
<span data-ttu-id="66bf0-118">Set di disponibilità gestita</span><span class="sxs-lookup"><span data-stu-id="66bf0-118">Managed Availability Set</span></span>

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

### <span data-ttu-id="66bf0-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="66bf0-119">-Sku</span></span>
<span data-ttu-id="66bf0-120">Nome della SKU</span><span class="sxs-lookup"><span data-stu-id="66bf0-120">The Name of Sku</span></span>

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

### <span data-ttu-id="66bf0-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="66bf0-121">-Confirm</span></span>
<span data-ttu-id="66bf0-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66bf0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66bf0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66bf0-123">-WhatIf</span></span>
<span data-ttu-id="66bf0-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66bf0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66bf0-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66bf0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66bf0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66bf0-126">CommonParameters</span></span>
<span data-ttu-id="66bf0-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66bf0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66bf0-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66bf0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66bf0-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="66bf0-129">INPUTS</span></span>

### <span data-ttu-id="66bf0-130">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="66bf0-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="66bf0-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66bf0-131">OUTPUTS</span></span>

### <span data-ttu-id="66bf0-132">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="66bf0-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="66bf0-133">Note</span><span class="sxs-lookup"><span data-stu-id="66bf0-133">NOTES</span></span>

## <span data-ttu-id="66bf0-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66bf0-134">RELATED LINKS</span></span>

