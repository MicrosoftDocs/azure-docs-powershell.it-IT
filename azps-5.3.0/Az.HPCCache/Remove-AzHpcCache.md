---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: fd01dea04043d8d68009f89823fe34f3695a6d47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473792"
---
# <span data-ttu-id="ad5f7-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="ad5f7-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="ad5f7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad5f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ad5f7-103">Rimuove una cache HPC.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="ad5f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad5f7-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad5f7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad5f7-105">DESCRIPTION</span></span>
<span data-ttu-id="ad5f7-106">Il cmdlet **Remove-AzHpcCache** rimuove una cache HPC di Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="ad5f7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad5f7-107">EXAMPLES</span></span>

### <span data-ttu-id="ad5f7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ad5f7-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="ad5f7-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad5f7-109">PARAMETERS</span></span>

### <span data-ttu-id="ad5f7-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad5f7-110">-AsJob</span></span>
<span data-ttu-id="ad5f7-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ad5f7-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad5f7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad5f7-112">-DefaultProfile</span></span>
<span data-ttu-id="ad5f7-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad5f7-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ad5f7-114">-Force</span></span>
<span data-ttu-id="ad5f7-115">Indica che il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="ad5f7-116">Per impostazione predefinita, questo cmdlet richiede di confermare che si vuole rimuovere la cache.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="ad5f7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad5f7-117">-Name</span></span>
<span data-ttu-id="ad5f7-118">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-118">Name of cache.</span></span>

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

### <span data-ttu-id="ad5f7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad5f7-119">-PassThru</span></span>
<span data-ttu-id="ad5f7-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ad5f7-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ad5f7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad5f7-122">-ResourceGroupName</span></span>
<span data-ttu-id="ad5f7-123">Nome del gruppo di risorse in cui si vuole rimuovere la cache.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="ad5f7-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ad5f7-124">-Confirm</span></span>
<span data-ttu-id="ad5f7-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad5f7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad5f7-126">-WhatIf</span></span>
<span data-ttu-id="ad5f7-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad5f7-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad5f7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad5f7-129">CommonParameters</span></span>
<span data-ttu-id="ad5f7-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad5f7-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad5f7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad5f7-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad5f7-132">INPUTS</span></span>

### <span data-ttu-id="ad5f7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ad5f7-133">System.String</span></span>

## <span data-ttu-id="ad5f7-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad5f7-134">OUTPUTS</span></span>

## <span data-ttu-id="ad5f7-135">Note</span><span class="sxs-lookup"><span data-stu-id="ad5f7-135">NOTES</span></span>

## <span data-ttu-id="ad5f7-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad5f7-136">RELATED LINKS</span></span>
