---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 7465a74db4da777d60e097fe959ef69bed11918c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180583"
---
# <span data-ttu-id="82c36-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="82c36-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="82c36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82c36-102">SYNOPSIS</span></span>
<span data-ttu-id="82c36-103">Avvia la cache HPC.</span><span class="sxs-lookup"><span data-stu-id="82c36-103">Starts HPC cache.</span></span>

## <span data-ttu-id="82c36-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82c36-104">SYNTAX</span></span>

### <span data-ttu-id="82c36-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="82c36-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82c36-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82c36-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82c36-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82c36-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82c36-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="82c36-108">DESCRIPTION</span></span>
<span data-ttu-id="82c36-109">Il cmdlet **Start-AzHpcCache avvia** una cache HPC di Azure.</span><span class="sxs-lookup"><span data-stu-id="82c36-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="82c36-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82c36-110">EXAMPLES</span></span>

### <span data-ttu-id="82c36-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="82c36-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="82c36-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82c36-112">PARAMETERS</span></span>

### <span data-ttu-id="82c36-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82c36-113">-AsJob</span></span>
<span data-ttu-id="82c36-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="82c36-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82c36-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c36-115">-DefaultProfile</span></span>
<span data-ttu-id="82c36-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82c36-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82c36-117">-Force</span><span class="sxs-lookup"><span data-stu-id="82c36-117">-Force</span></span>
<span data-ttu-id="82c36-118">Indica che il cmdlet non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="82c36-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="82c36-119">Per impostazione predefinita, questo cmdlet chiede di confermare l'avvio della cache.</span><span class="sxs-lookup"><span data-stu-id="82c36-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="82c36-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82c36-120">-InputObject</span></span>
<span data-ttu-id="82c36-121">Oggetto cache da avviare.</span><span class="sxs-lookup"><span data-stu-id="82c36-121">The cache object to start.</span></span>

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

### <span data-ttu-id="82c36-122">-Name</span><span class="sxs-lookup"><span data-stu-id="82c36-122">-Name</span></span>
<span data-ttu-id="82c36-123">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="82c36-123">Name of cache.</span></span>

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

### <span data-ttu-id="82c36-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82c36-124">-PassThru</span></span>
<span data-ttu-id="82c36-125">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="82c36-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="82c36-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="82c36-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="82c36-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82c36-127">-ResourceGroupName</span></span>
<span data-ttu-id="82c36-128">Nome del gruppo di risorse in cui si vuole avviare la cache.</span><span class="sxs-lookup"><span data-stu-id="82c36-128">Name of resource group under which you want to start cache.</span></span>

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

### <span data-ttu-id="82c36-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82c36-129">-ResourceId</span></span>
<span data-ttu-id="82c36-130">ID risorsa della cache</span><span class="sxs-lookup"><span data-stu-id="82c36-130">The resource id of the Cache</span></span>

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

### <span data-ttu-id="82c36-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82c36-131">-Confirm</span></span>
<span data-ttu-id="82c36-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82c36-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82c36-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82c36-133">-WhatIf</span></span>
<span data-ttu-id="82c36-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82c36-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82c36-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82c36-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82c36-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c36-136">CommonParameters</span></span>
<span data-ttu-id="82c36-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82c36-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c36-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82c36-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c36-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="82c36-139">INPUTS</span></span>

### <span data-ttu-id="82c36-140">System.String</span><span class="sxs-lookup"><span data-stu-id="82c36-140">System.String</span></span>

## <span data-ttu-id="82c36-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82c36-141">OUTPUTS</span></span>

## <span data-ttu-id="82c36-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="82c36-142">NOTES</span></span>

## <span data-ttu-id="82c36-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82c36-143">RELATED LINKS</span></span>
