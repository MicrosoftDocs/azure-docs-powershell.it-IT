---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: faadb14259dd397f713480c771d2d450260d99cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201276"
---
# <span data-ttu-id="24657-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="24657-101">New-AzHpcCache</span></span>

## <span data-ttu-id="24657-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24657-102">SYNOPSIS</span></span>
<span data-ttu-id="24657-103">Crea una cache HPC.</span><span class="sxs-lookup"><span data-stu-id="24657-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="24657-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24657-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24657-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24657-105">DESCRIPTION</span></span>
<span data-ttu-id="24657-106">Il cmdlet **New-AzHpcCache** crea una cache HPC di Azure.</span><span class="sxs-lookup"><span data-stu-id="24657-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="24657-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24657-107">EXAMPLES</span></span>

### <span data-ttu-id="24657-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="24657-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="24657-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24657-109">PARAMETERS</span></span>

### <span data-ttu-id="24657-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24657-110">-AsJob</span></span>
<span data-ttu-id="24657-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="24657-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24657-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="24657-112">-CacheSize</span></span>
<span data-ttu-id="24657-113">CacheSize.</span><span class="sxs-lookup"><span data-stu-id="24657-113">CacheSize.</span></span>

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

### <span data-ttu-id="24657-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24657-114">-DefaultProfile</span></span>
<span data-ttu-id="24657-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24657-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24657-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="24657-116">-Location</span></span>
<span data-ttu-id="24657-117">Posizione.</span><span class="sxs-lookup"><span data-stu-id="24657-117">Location.</span></span>

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

### <span data-ttu-id="24657-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="24657-118">-Name</span></span>
<span data-ttu-id="24657-119">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="24657-119">Name of cache.</span></span>

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

### <span data-ttu-id="24657-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24657-120">-ResourceGroupName</span></span>
<span data-ttu-id="24657-121">Nome del gruppo di risorse in cui si vuole creare la cache.</span><span class="sxs-lookup"><span data-stu-id="24657-121">Name of resource group under which you want to create cache.</span></span>

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

### <span data-ttu-id="24657-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="24657-122">-Sku</span></span>
<span data-ttu-id="24657-123">SKU.</span><span class="sxs-lookup"><span data-stu-id="24657-123">Sku.</span></span>

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

### <span data-ttu-id="24657-124">-SubnetUri</span><span class="sxs-lookup"><span data-stu-id="24657-124">-SubnetUri</span></span>
<span data-ttu-id="24657-125">SubnetURI.</span><span class="sxs-lookup"><span data-stu-id="24657-125">SubnetURI.</span></span>

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

### <span data-ttu-id="24657-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="24657-126">-Tag</span></span>
<span data-ttu-id="24657-127">Tag da associare alla cache HPC.</span><span class="sxs-lookup"><span data-stu-id="24657-127">The tags to associate with HPC Cache.</span></span>

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

### <span data-ttu-id="24657-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="24657-128">-Confirm</span></span>
<span data-ttu-id="24657-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24657-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24657-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24657-130">-WhatIf</span></span>
<span data-ttu-id="24657-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24657-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24657-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24657-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24657-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24657-133">CommonParameters</span></span>
<span data-ttu-id="24657-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24657-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24657-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24657-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24657-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24657-136">INPUTS</span></span>

### <span data-ttu-id="24657-137">System. String</span><span class="sxs-lookup"><span data-stu-id="24657-137">System.String</span></span>

### <span data-ttu-id="24657-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="24657-138">System.Int32</span></span>

## <span data-ttu-id="24657-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24657-139">OUTPUTS</span></span>

### <span data-ttu-id="24657-140">Microsoft. Azure. PowerShell. Cmdlets. HPCCache. Models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="24657-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="24657-141">Note</span><span class="sxs-lookup"><span data-stu-id="24657-141">NOTES</span></span>

## <span data-ttu-id="24657-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24657-142">RELATED LINKS</span></span>
