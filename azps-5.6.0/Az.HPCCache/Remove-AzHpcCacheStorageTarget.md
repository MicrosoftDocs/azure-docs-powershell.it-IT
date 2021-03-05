---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: 2de3856a51ce8b55d6db7a82f6e50027b60d9d87
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013517"
---
# <span data-ttu-id="b5b06-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="b5b06-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="b5b06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5b06-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b06-103">Rimuove un target di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b5b06-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="b5b06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5b06-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5b06-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b5b06-105">DESCRIPTION</span></span>
<span data-ttu-id="b5b06-106">Il cmdlet **Remove-AzHpcCacheStorageTarget rimuove** una destinazione di archiviazione dalla cache di Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="b5b06-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="b5b06-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5b06-107">EXAMPLES</span></span>

### <span data-ttu-id="b5b06-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b5b06-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="b5b06-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5b06-109">PARAMETERS</span></span>

### <span data-ttu-id="b5b06-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5b06-110">-AsJob</span></span>
<span data-ttu-id="b5b06-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b5b06-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5b06-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="b5b06-112">-CacheName</span></span>
<span data-ttu-id="b5b06-113">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="b5b06-113">Name of cache.</span></span>

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

### <span data-ttu-id="b5b06-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b06-114">-DefaultProfile</span></span>
<span data-ttu-id="b5b06-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5b06-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5b06-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b5b06-116">-Force</span></span>
<span data-ttu-id="b5b06-117">Indica che il cmdlet non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="b5b06-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="b5b06-118">Per impostazione predefinita, questo cmdlet chiede di confermare la rimozione della destinazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b5b06-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="b5b06-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b5b06-119">-Name</span></span>
<span data-ttu-id="b5b06-120">Nome della destinazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b5b06-120">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageTargetName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b06-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5b06-121">-PassThru</span></span>
<span data-ttu-id="b5b06-122">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b5b06-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b5b06-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b5b06-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b5b06-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5b06-124">-ResourceGroupName</span></span>
<span data-ttu-id="b5b06-125">Nome del gruppo di risorse in cui si vuole rimuovere la destinazione di archiviazione dalla cache.</span><span class="sxs-lookup"><span data-stu-id="b5b06-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="b5b06-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5b06-126">-Confirm</span></span>
<span data-ttu-id="b5b06-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b06-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5b06-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5b06-128">-WhatIf</span></span>
<span data-ttu-id="b5b06-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5b06-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5b06-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5b06-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5b06-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b06-131">CommonParameters</span></span>
<span data-ttu-id="b5b06-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b06-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b06-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b5b06-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b06-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="b5b06-134">INPUTS</span></span>

### <span data-ttu-id="b5b06-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b5b06-135">System.String</span></span>

## <span data-ttu-id="b5b06-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5b06-136">OUTPUTS</span></span>

## <span data-ttu-id="b5b06-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="b5b06-137">NOTES</span></span>

## <span data-ttu-id="b5b06-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5b06-138">RELATED LINKS</span></span>
