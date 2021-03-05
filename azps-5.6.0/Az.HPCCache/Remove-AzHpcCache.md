---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: 12bf101fb404b02fc70cbec9640f5f2bd976107c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013518"
---
# <span data-ttu-id="8023d-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="8023d-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="8023d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8023d-102">SYNOPSIS</span></span>
<span data-ttu-id="8023d-103">Rimuove una cache HPC.</span><span class="sxs-lookup"><span data-stu-id="8023d-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="8023d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8023d-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8023d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8023d-105">DESCRIPTION</span></span>
<span data-ttu-id="8023d-106">Il cmdlet **Remove-AzHpcCache** rimuove una cache HPC di Azure.</span><span class="sxs-lookup"><span data-stu-id="8023d-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="8023d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8023d-107">EXAMPLES</span></span>

### <span data-ttu-id="8023d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8023d-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="8023d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8023d-109">PARAMETERS</span></span>

### <span data-ttu-id="8023d-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8023d-110">-AsJob</span></span>
<span data-ttu-id="8023d-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8023d-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8023d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8023d-112">-DefaultProfile</span></span>
<span data-ttu-id="8023d-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8023d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8023d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="8023d-114">-Force</span></span>
<span data-ttu-id="8023d-115">Indica che il cmdlet non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="8023d-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="8023d-116">Per impostazione predefinita, questo cmdlet chiede di confermare la rimozione della cache.</span><span class="sxs-lookup"><span data-stu-id="8023d-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="8023d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8023d-117">-Name</span></span>
<span data-ttu-id="8023d-118">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="8023d-118">Name of cache.</span></span>

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

### <span data-ttu-id="8023d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8023d-119">-PassThru</span></span>
<span data-ttu-id="8023d-120">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="8023d-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8023d-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="8023d-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8023d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8023d-122">-ResourceGroupName</span></span>
<span data-ttu-id="8023d-123">Nome del gruppo di risorse da cui si vuole rimuovere la cache.</span><span class="sxs-lookup"><span data-stu-id="8023d-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="8023d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8023d-124">-Confirm</span></span>
<span data-ttu-id="8023d-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8023d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8023d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8023d-126">-WhatIf</span></span>
<span data-ttu-id="8023d-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8023d-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8023d-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8023d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8023d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8023d-129">CommonParameters</span></span>
<span data-ttu-id="8023d-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8023d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8023d-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8023d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8023d-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="8023d-132">INPUTS</span></span>

### <span data-ttu-id="8023d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8023d-133">System.String</span></span>

## <span data-ttu-id="8023d-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8023d-134">OUTPUTS</span></span>

## <span data-ttu-id="8023d-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="8023d-135">NOTES</span></span>

## <span data-ttu-id="8023d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8023d-136">RELATED LINKS</span></span>
