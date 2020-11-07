---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: e8bd36cd9c054d155dca034f49be8cd422a244bc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861597"
---
# <span data-ttu-id="aaf27-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="aaf27-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="aaf27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aaf27-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf27-103">Aggiorna un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="aaf27-103">Updates an availability set.</span></span>

## <span data-ttu-id="aaf27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aaf27-104">SYNTAX</span></span>

### <span data-ttu-id="aaf27-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaf27-105">SkuParameterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaf27-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="aaf27-106">ManagedParamterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaf27-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aaf27-107">DESCRIPTION</span></span>
<span data-ttu-id="aaf27-108">Il cmdlet **Update-AzAvailabilitySet** aggiorna un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="aaf27-108">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="aaf27-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aaf27-109">EXAMPLES</span></span>

### <span data-ttu-id="aaf27-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aaf27-110">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="aaf27-111">Questo comando Aggiorna il set di disponibilità denominato "AvSet01" nel gruppo di risorse denominato "ResourceGroup01" in un set di disponibilità gestita.</span><span class="sxs-lookup"><span data-stu-id="aaf27-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="aaf27-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aaf27-112">PARAMETERS</span></span>

### <span data-ttu-id="aaf27-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aaf27-113">-AsJob</span></span>
<span data-ttu-id="aaf27-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="aaf27-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="aaf27-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="aaf27-115">-AvailabilitySet</span></span>
<span data-ttu-id="aaf27-116">Specifica l'oggetto set di disponibilità da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="aaf27-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="aaf27-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf27-117">-DefaultProfile</span></span>
<span data-ttu-id="aaf27-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aaf27-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaf27-119">-Managed</span><span class="sxs-lookup"><span data-stu-id="aaf27-119">-Managed</span></span>
<span data-ttu-id="aaf27-120">Set di disponibilità gestita</span><span class="sxs-lookup"><span data-stu-id="aaf27-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="aaf27-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="aaf27-121">-Sku</span></span>
<span data-ttu-id="aaf27-122">Nome della SKU</span><span class="sxs-lookup"><span data-stu-id="aaf27-122">The Name of Sku</span></span>

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

### <span data-ttu-id="aaf27-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aaf27-123">-Confirm</span></span>
<span data-ttu-id="aaf27-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaf27-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaf27-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaf27-125">-WhatIf</span></span>
<span data-ttu-id="aaf27-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aaf27-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aaf27-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aaf27-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaf27-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf27-128">CommonParameters</span></span>
<span data-ttu-id="aaf27-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaf27-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf27-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaf27-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf27-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aaf27-131">INPUTS</span></span>

### <span data-ttu-id="aaf27-132">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="aaf27-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="aaf27-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aaf27-133">OUTPUTS</span></span>

### <span data-ttu-id="aaf27-134">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="aaf27-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="aaf27-135">Note</span><span class="sxs-lookup"><span data-stu-id="aaf27-135">NOTES</span></span>

## <span data-ttu-id="aaf27-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aaf27-136">RELATED LINKS</span></span>

