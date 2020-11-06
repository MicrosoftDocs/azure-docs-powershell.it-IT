---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 3e28cacc8dc6a27f20a93beb3e48ddcc0d0697cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518816"
---
# <span data-ttu-id="1d9a5-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1d9a5-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="1d9a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d9a5-102">SYNOPSIS</span></span>
<span data-ttu-id="1d9a5-103">Aggiorna un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d9a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d9a5-104">SYNTAX</span></span>

### <span data-ttu-id="1d9a5-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d9a5-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d9a5-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="1d9a5-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d9a5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d9a5-107">DESCRIPTION</span></span>
<span data-ttu-id="1d9a5-108">Il cmdlet **Update-AzureRmAvailabilitySet** aggiorna un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="1d9a5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d9a5-109">EXAMPLES</span></span>

### <span data-ttu-id="1d9a5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1d9a5-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="1d9a5-111">Questo comando Aggiorna il set di disponibilità denominato "AvSet01" nel gruppo di risorse denominato "ResourceGroup01" in un set di disponibilità gestita.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="1d9a5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d9a5-112">PARAMETERS</span></span>

### <span data-ttu-id="1d9a5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d9a5-113">-AsJob</span></span>
<span data-ttu-id="1d9a5-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1d9a5-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1d9a5-115">-AvailabilitySet</span></span>
<span data-ttu-id="1d9a5-116">Specifica l'oggetto set di disponibilità da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="1d9a5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d9a5-117">-DefaultProfile</span></span>
<span data-ttu-id="1d9a5-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d9a5-119">-Managed</span><span class="sxs-lookup"><span data-stu-id="1d9a5-119">-Managed</span></span>
<span data-ttu-id="1d9a5-120">Set di disponibilità gestita</span><span class="sxs-lookup"><span data-stu-id="1d9a5-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="1d9a5-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="1d9a5-121">-Sku</span></span>
<span data-ttu-id="1d9a5-122">Nome della SKU</span><span class="sxs-lookup"><span data-stu-id="1d9a5-122">The Name of Sku</span></span>

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

### <span data-ttu-id="1d9a5-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="1d9a5-123">-Tag</span></span>
<span data-ttu-id="1d9a5-124">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-124">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="1d9a5-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1d9a5-125">-Confirm</span></span>
<span data-ttu-id="1d9a5-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d9a5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d9a5-127">-WhatIf</span></span>
<span data-ttu-id="1d9a5-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d9a5-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d9a5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d9a5-130">CommonParameters</span></span>
<span data-ttu-id="1d9a5-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d9a5-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d9a5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d9a5-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d9a5-133">INPUTS</span></span>

### <span data-ttu-id="1d9a5-134">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1d9a5-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="1d9a5-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d9a5-135">OUTPUTS</span></span>

### <span data-ttu-id="1d9a5-136">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1d9a5-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="1d9a5-137">Note</span><span class="sxs-lookup"><span data-stu-id="1d9a5-137">NOTES</span></span>

## <span data-ttu-id="1d9a5-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d9a5-138">RELATED LINKS</span></span>
