---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 22813d762fe575f7f34b6c8eb81f1b5c1c167047
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193307"
---
# <span data-ttu-id="15e2d-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="15e2d-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="15e2d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="15e2d-102">SYNOPSIS</span></span>
<span data-ttu-id="15e2d-103">Interrompe la cache HPC.</span><span class="sxs-lookup"><span data-stu-id="15e2d-103">Stops HPC cache.</span></span>

## <span data-ttu-id="15e2d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15e2d-104">SYNTAX</span></span>

### <span data-ttu-id="15e2d-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="15e2d-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15e2d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15e2d-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15e2d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15e2d-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15e2d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15e2d-108">DESCRIPTION</span></span>
<span data-ttu-id="15e2d-109">Il cmdlet **Stop-AzHpcCache** interrompe una cache HPC di Azure.</span><span class="sxs-lookup"><span data-stu-id="15e2d-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="15e2d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15e2d-110">EXAMPLES</span></span>

### <span data-ttu-id="15e2d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="15e2d-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="15e2d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15e2d-112">PARAMETERS</span></span>

### <span data-ttu-id="15e2d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15e2d-113">-DefaultProfile</span></span>
<span data-ttu-id="15e2d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15e2d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15e2d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="15e2d-115">-Force</span></span>
<span data-ttu-id="15e2d-116">Indica che il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="15e2d-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="15e2d-117">Per impostazione predefinita, questo cmdlet richiede di confermare che si vuole arrestare la cache.</span><span class="sxs-lookup"><span data-stu-id="15e2d-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="15e2d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15e2d-118">-InputObject</span></span>
<span data-ttu-id="15e2d-119">L'oggetto cache da interrompere.</span><span class="sxs-lookup"><span data-stu-id="15e2d-119">The cache object to stop.</span></span>

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

### <span data-ttu-id="15e2d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="15e2d-120">-Name</span></span>
<span data-ttu-id="15e2d-121">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="15e2d-121">Name of cache.</span></span>

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

### <span data-ttu-id="15e2d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15e2d-122">-PassThru</span></span>
<span data-ttu-id="15e2d-123">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="15e2d-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="15e2d-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="15e2d-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="15e2d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15e2d-125">-ResourceGroupName</span></span>
<span data-ttu-id="15e2d-126">Nome del gruppo di risorse in cui si vuole interrompere la cache.</span><span class="sxs-lookup"><span data-stu-id="15e2d-126">Name of resource group under which you want to stop cache.</span></span>

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

### <span data-ttu-id="15e2d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15e2d-127">-ResourceId</span></span>
<span data-ttu-id="15e2d-128">ID risorsa della cache</span><span class="sxs-lookup"><span data-stu-id="15e2d-128">The resource id of the Cache</span></span>

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

### <span data-ttu-id="15e2d-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="15e2d-129">-Confirm</span></span>
<span data-ttu-id="15e2d-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15e2d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15e2d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15e2d-131">-WhatIf</span></span>
<span data-ttu-id="15e2d-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15e2d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15e2d-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15e2d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15e2d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15e2d-134">CommonParameters</span></span>
<span data-ttu-id="15e2d-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15e2d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15e2d-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15e2d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15e2d-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="15e2d-137">INPUTS</span></span>

### <span data-ttu-id="15e2d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="15e2d-138">System.String</span></span>

## <span data-ttu-id="15e2d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15e2d-139">OUTPUTS</span></span>

## <span data-ttu-id="15e2d-140">Note</span><span class="sxs-lookup"><span data-stu-id="15e2d-140">NOTES</span></span>

## <span data-ttu-id="15e2d-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15e2d-141">RELATED LINKS</span></span>