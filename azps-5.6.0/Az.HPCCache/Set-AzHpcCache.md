---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 9ad46b21990e6a864408536bf56bb09c2d0b3dc3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013502"
---
# <span data-ttu-id="d17ec-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="d17ec-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="d17ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d17ec-102">SYNOPSIS</span></span>
<span data-ttu-id="d17ec-103">Aggiorna i tag in una cache HPC.</span><span class="sxs-lookup"><span data-stu-id="d17ec-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="d17ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d17ec-104">SYNTAX</span></span>

### <span data-ttu-id="d17ec-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d17ec-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d17ec-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d17ec-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d17ec-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d17ec-107">DESCRIPTION</span></span>
<span data-ttu-id="d17ec-108">Il cmdlet **Set-AzHpcCache** aggiorna i tag della cache HPC di Azure.</span><span class="sxs-lookup"><span data-stu-id="d17ec-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="d17ec-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d17ec-109">EXAMPLES</span></span>

### <span data-ttu-id="d17ec-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d17ec-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="d17ec-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d17ec-111">PARAMETERS</span></span>

### <span data-ttu-id="d17ec-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d17ec-112">-AsJob</span></span>
<span data-ttu-id="d17ec-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d17ec-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d17ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d17ec-114">-DefaultProfile</span></span>
<span data-ttu-id="d17ec-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d17ec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d17ec-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d17ec-116">-InputObject</span></span>
<span data-ttu-id="d17ec-117">Oggetto cache da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="d17ec-117">The cache object to update.</span></span>

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

### <span data-ttu-id="d17ec-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d17ec-118">-Name</span></span>
<span data-ttu-id="d17ec-119">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="d17ec-119">Name of cache.</span></span>

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

### <span data-ttu-id="d17ec-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d17ec-120">-ResourceGroupName</span></span>
<span data-ttu-id="d17ec-121">Nome del gruppo di risorse in cui si vuole aggiornare la cache.</span><span class="sxs-lookup"><span data-stu-id="d17ec-121">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="d17ec-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="d17ec-122">-Tag</span></span>
<span data-ttu-id="d17ec-123">I tag da associare alla cache HPC.</span><span class="sxs-lookup"><span data-stu-id="d17ec-123">The tags to associate with HPC Cache.</span></span> 

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d17ec-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d17ec-124">-Confirm</span></span>
<span data-ttu-id="d17ec-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d17ec-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d17ec-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d17ec-126">-WhatIf</span></span>
<span data-ttu-id="d17ec-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d17ec-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d17ec-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d17ec-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d17ec-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d17ec-129">CommonParameters</span></span>
<span data-ttu-id="d17ec-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d17ec-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d17ec-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d17ec-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d17ec-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="d17ec-132">INPUTS</span></span>

### <span data-ttu-id="d17ec-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d17ec-133">System.String</span></span>

### <span data-ttu-id="d17ec-134">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d17ec-134">System.Int32</span></span>

## <span data-ttu-id="d17ec-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d17ec-135">OUTPUTS</span></span>

### <span data-ttu-id="d17ec-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="d17ec-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="d17ec-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="d17ec-137">NOTES</span></span>

## <span data-ttu-id="d17ec-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d17ec-138">RELATED LINKS</span></span>
