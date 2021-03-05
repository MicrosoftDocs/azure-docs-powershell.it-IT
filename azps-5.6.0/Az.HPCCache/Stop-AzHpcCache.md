---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 2d3fd9d44a06c8538233b1f130010e905055912e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013422"
---
# <span data-ttu-id="b73e1-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="b73e1-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="b73e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b73e1-102">SYNOPSIS</span></span>
<span data-ttu-id="b73e1-103">Interrompe la cache HPC.</span><span class="sxs-lookup"><span data-stu-id="b73e1-103">Stops HPC cache.</span></span>

## <span data-ttu-id="b73e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b73e1-104">SYNTAX</span></span>

### <span data-ttu-id="b73e1-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b73e1-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b73e1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b73e1-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b73e1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b73e1-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b73e1-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b73e1-108">DESCRIPTION</span></span>
<span data-ttu-id="b73e1-109">Il cmdlet **Stop-AzHpcCache interrompe** una cache HPC di Azure.</span><span class="sxs-lookup"><span data-stu-id="b73e1-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="b73e1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b73e1-110">EXAMPLES</span></span>

### <span data-ttu-id="b73e1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b73e1-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="b73e1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b73e1-112">PARAMETERS</span></span>

### <span data-ttu-id="b73e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b73e1-113">-DefaultProfile</span></span>
<span data-ttu-id="b73e1-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b73e1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b73e1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b73e1-115">-Force</span></span>
<span data-ttu-id="b73e1-116">Indica che il cmdlet non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="b73e1-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="b73e1-117">Per impostazione predefinita, questo cmdlet chiede di confermare l'interruzione della cache.</span><span class="sxs-lookup"><span data-stu-id="b73e1-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="b73e1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b73e1-118">-InputObject</span></span>
<span data-ttu-id="b73e1-119">Oggetto cache da interrompere.</span><span class="sxs-lookup"><span data-stu-id="b73e1-119">The cache object to stop.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b73e1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b73e1-120">-Name</span></span>
<span data-ttu-id="b73e1-121">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="b73e1-121">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b73e1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b73e1-122">-PassThru</span></span>
<span data-ttu-id="b73e1-123">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b73e1-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b73e1-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b73e1-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b73e1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b73e1-125">-ResourceGroupName</span></span>
<span data-ttu-id="b73e1-126">Nome del gruppo di risorse in cui si vuole interrompere la cache.</span><span class="sxs-lookup"><span data-stu-id="b73e1-126">Name of resource group under which you want to stop cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b73e1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b73e1-127">-ResourceId</span></span>
<span data-ttu-id="b73e1-128">ID risorsa della cache</span><span class="sxs-lookup"><span data-stu-id="b73e1-128">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b73e1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b73e1-129">-Confirm</span></span>
<span data-ttu-id="b73e1-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b73e1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b73e1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b73e1-131">-WhatIf</span></span>
<span data-ttu-id="b73e1-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b73e1-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b73e1-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b73e1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b73e1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b73e1-134">CommonParameters</span></span>
<span data-ttu-id="b73e1-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b73e1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b73e1-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b73e1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b73e1-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="b73e1-137">INPUTS</span></span>

### <span data-ttu-id="b73e1-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b73e1-138">System.String</span></span>

## <span data-ttu-id="b73e1-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b73e1-139">OUTPUTS</span></span>

## <span data-ttu-id="b73e1-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="b73e1-140">NOTES</span></span>

## <span data-ttu-id="b73e1-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b73e1-141">RELATED LINKS</span></span>
