---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: faadb14259dd397f713480c771d2d450260d99cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209387"
---
# <span data-ttu-id="d9c2f-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="d9c2f-101">New-AzHpcCache</span></span>

## <span data-ttu-id="d9c2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c2f-103">Crea una cache HPC.</span><span class="sxs-lookup"><span data-stu-id="d9c2f-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="d9c2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9c2f-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9c2f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d9c2f-105">DESCRIPTION</span></span>
<span data-ttu-id="d9c2f-106">Il cmdlet **New-AzHpcCache crea** una cache HPC di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9c2f-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="d9c2f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9c2f-107">EXAMPLES</span></span>

### <span data-ttu-id="d9c2f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d9c2f-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="d9c2f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9c2f-109">PARAMETERS</span></span>

### <span data-ttu-id="d9c2f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9c2f-110">-AsJob</span></span>
<span data-ttu-id="d9c2f-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d9c2f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9c2f-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="d9c2f-112">-CacheSize</span></span>
<span data-ttu-id="d9c2f-113">CacheSize.</span><span class="sxs-lookup"><span data-stu-id="d9c2f-113">CacheSize.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c2f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c2f-114">-DefaultProfile</span></span>
<span data-ttu-id="d9c2f-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9c2f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9c2f-116">-Location</span><span class="sxs-lookup"><span data-stu-id="d9c2f-116">-Location</span></span>
<span data-ttu-id="d9c2f-117">Posizione.</span><span class="sxs-lookup"><span data-stu-id="d9c2f-117">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c2f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d9c2f-118">-Name</span></span>
<span data-ttu-id="d9c2f-119">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="d9c2f-119">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c2f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9c2f-120">-ResourceGroupName</span></span>
<span data-ttu-id="d9c2f-121">Nome del gruppo di risorse in cui si vuole creare la cache.</span><span class="sxs-lookup"><span data-stu-id="d9c2f-121">Name of resource group under which you want to create cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c2f-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="d9c2f-122">-Sku</span></span>
<span data-ttu-id="d9c2f-123">SKU.</span><span class="sxs-lookup"><span data-stu-id="d9c2f-123">Sku.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c2f-124">-SubnetUri</span><span class="sxs-lookup"><span data-stu-id="d9c2f-124">-SubnetUri</span></span>
<span data-ttu-id="d9c2f-125">SubnetURI.</span><span class="sxs-lookup"><span data-stu-id="d9c2f-125">SubnetURI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c2f-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="d9c2f-126">-Tag</span></span>
<span data-ttu-id="d9c2f-127">I tag da associare alla cache HPC.</span><span class="sxs-lookup"><span data-stu-id="d9c2f-127">The tags to associate with HPC Cache.</span></span>

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

### <span data-ttu-id="d9c2f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9c2f-128">-Confirm</span></span>
<span data-ttu-id="d9c2f-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9c2f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9c2f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9c2f-130">-WhatIf</span></span>
<span data-ttu-id="d9c2f-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9c2f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9c2f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9c2f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9c2f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c2f-133">CommonParameters</span></span>
<span data-ttu-id="d9c2f-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9c2f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c2f-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d9c2f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c2f-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="d9c2f-136">INPUTS</span></span>

### <span data-ttu-id="d9c2f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d9c2f-137">System.String</span></span>

### <span data-ttu-id="d9c2f-138">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d9c2f-138">System.Int32</span></span>

## <span data-ttu-id="d9c2f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9c2f-139">OUTPUTS</span></span>

### <span data-ttu-id="d9c2f-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="d9c2f-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="d9c2f-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="d9c2f-141">NOTES</span></span>

## <span data-ttu-id="d9c2f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9c2f-142">RELATED LINKS</span></span>
