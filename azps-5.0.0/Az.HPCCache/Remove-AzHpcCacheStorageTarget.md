---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: a3603a1884318f567908937ab880182e0df5ee57
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201269"
---
# <span data-ttu-id="2d7b2-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="2d7b2-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="2d7b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d7b2-102">SYNOPSIS</span></span>
<span data-ttu-id="2d7b2-103">Rimuove una destinazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2d7b2-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="2d7b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d7b2-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d7b2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d7b2-105">DESCRIPTION</span></span>
<span data-ttu-id="2d7b2-106">Il cmdlet **Remove-AzHpcCacheStorageTarget** rimuove una destinazione di archiviazione dalla cache di Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="2d7b2-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="2d7b2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d7b2-107">EXAMPLES</span></span>

### <span data-ttu-id="2d7b2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2d7b2-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="2d7b2-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d7b2-109">PARAMETERS</span></span>

### <span data-ttu-id="2d7b2-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d7b2-110">-AsJob</span></span>
<span data-ttu-id="2d7b2-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2d7b2-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d7b2-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="2d7b2-112">-CacheName</span></span>
<span data-ttu-id="2d7b2-113">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="2d7b2-113">Name of cache.</span></span>

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

### <span data-ttu-id="2d7b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d7b2-114">-DefaultProfile</span></span>
<span data-ttu-id="2d7b2-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2d7b2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d7b2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2d7b2-116">-Force</span></span>
<span data-ttu-id="2d7b2-117">Indica che il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="2d7b2-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="2d7b2-118">Per impostazione predefinita, questo cmdlet richiede di confermare che si vuole rimuovere la destinazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2d7b2-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="2d7b2-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d7b2-119">-Name</span></span>
<span data-ttu-id="2d7b2-120">Nome della destinazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2d7b2-120">Name of storage target.</span></span>

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

### <span data-ttu-id="2d7b2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d7b2-121">-PassThru</span></span>
<span data-ttu-id="2d7b2-122">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="2d7b2-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2d7b2-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="2d7b2-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2d7b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d7b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="2d7b2-125">Nome del gruppo di risorse in cui si vuole rimuovere la destinazione di archiviazione dalla cache.</span><span class="sxs-lookup"><span data-stu-id="2d7b2-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="2d7b2-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2d7b2-126">-Confirm</span></span>
<span data-ttu-id="2d7b2-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d7b2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d7b2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d7b2-128">-WhatIf</span></span>
<span data-ttu-id="2d7b2-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d7b2-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d7b2-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d7b2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d7b2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d7b2-131">CommonParameters</span></span>
<span data-ttu-id="2d7b2-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d7b2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d7b2-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d7b2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d7b2-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d7b2-134">INPUTS</span></span>

### <span data-ttu-id="2d7b2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2d7b2-135">System.String</span></span>

## <span data-ttu-id="2d7b2-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d7b2-136">OUTPUTS</span></span>

## <span data-ttu-id="2d7b2-137">Note</span><span class="sxs-lookup"><span data-stu-id="2d7b2-137">NOTES</span></span>

## <span data-ttu-id="2d7b2-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d7b2-138">RELATED LINKS</span></span>
