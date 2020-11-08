---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/update-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
ms.openlocfilehash: 8f84323df269d8e0fbd0f60525e54595ef89f3e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193306"
---
# <span data-ttu-id="fc8f9-101">Update-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="fc8f9-101">Update-AzHpcCache</span></span>

## <span data-ttu-id="fc8f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc8f9-102">SYNOPSIS</span></span>
<span data-ttu-id="fc8f9-103">Aggiorna una cache HPC.</span><span class="sxs-lookup"><span data-stu-id="fc8f9-103">Updates a HPC Cache.</span></span>

## <span data-ttu-id="fc8f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc8f9-104">SYNTAX</span></span>

### <span data-ttu-id="fc8f9-105">FlushParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fc8f9-105">FlushParameterSet (Default)</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Flush] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc8f9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc8f9-106">ByResourceIdParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc8f9-107">UpgradeParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc8f9-107">UpgradeParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Upgrade] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc8f9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc8f9-108">ByObjectParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -InputObject <PSHPCCache> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc8f9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc8f9-109">DESCRIPTION</span></span>
<span data-ttu-id="fc8f9-110">Il cmdlet **Update-AzHpcCache** aggiorna una cache HPC di Azure.</span><span class="sxs-lookup"><span data-stu-id="fc8f9-110">The **Update-AzHpcCache** cmdlet updates a Azure HPC Cache.</span></span>

## <span data-ttu-id="fc8f9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc8f9-111">EXAMPLES</span></span>

### <span data-ttu-id="fc8f9-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fc8f9-112">Example 1</span></span>
```powershell
PS C:\> Update-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="fc8f9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc8f9-113">PARAMETERS</span></span>

### <span data-ttu-id="fc8f9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc8f9-114">-AsJob</span></span>
<span data-ttu-id="fc8f9-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fc8f9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc8f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc8f9-116">-DefaultProfile</span></span>
<span data-ttu-id="fc8f9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc8f9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc8f9-118">-Flush</span><span class="sxs-lookup"><span data-stu-id="fc8f9-118">-Flush</span></span>
<span data-ttu-id="fc8f9-119">Svuota la cache HPC.</span><span class="sxs-lookup"><span data-stu-id="fc8f9-119">Flushes HPC Cache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FlushParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc8f9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fc8f9-120">-Force</span></span>
<span data-ttu-id="fc8f9-121">Indica che il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="fc8f9-121">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="fc8f9-122">Per impostazione predefinita, questo cmdlet richiede di confermare che si vuole aggiornare la cache.</span><span class="sxs-lookup"><span data-stu-id="fc8f9-122">By default, this cmdlet prompts you to confirm that you want to update the cache.</span></span>

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

### <span data-ttu-id="fc8f9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc8f9-123">-InputObject</span></span>
<span data-ttu-id="fc8f9-124">L'oggetto cache da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="fc8f9-124">The cache object to update.</span></span>

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

### <span data-ttu-id="fc8f9-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc8f9-125">-Name</span></span>
<span data-ttu-id="fc8f9-126">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="fc8f9-126">Name of cache.</span></span>

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

### <span data-ttu-id="fc8f9-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc8f9-127">-PassThru</span></span>
<span data-ttu-id="fc8f9-128">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="fc8f9-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fc8f9-129">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="fc8f9-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fc8f9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc8f9-130">-ResourceGroupName</span></span>
<span data-ttu-id="fc8f9-131">Nome del gruppo di risorse in cui si vuole aggiornare la cache.</span><span class="sxs-lookup"><span data-stu-id="fc8f9-131">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="fc8f9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc8f9-132">-ResourceId</span></span>
<span data-ttu-id="fc8f9-133">ID risorsa della cache</span><span class="sxs-lookup"><span data-stu-id="fc8f9-133">The resource id of the Cache</span></span>

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

### <span data-ttu-id="fc8f9-134">-Upgrade</span><span class="sxs-lookup"><span data-stu-id="fc8f9-134">-Upgrade</span></span>
<span data-ttu-id="fc8f9-135">Aggiornare HpcCache.</span><span class="sxs-lookup"><span data-stu-id="fc8f9-135">Upgrade HpcCache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpgradeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc8f9-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fc8f9-136">-Confirm</span></span>
<span data-ttu-id="fc8f9-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc8f9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc8f9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc8f9-138">-WhatIf</span></span>
<span data-ttu-id="fc8f9-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc8f9-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc8f9-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc8f9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc8f9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc8f9-141">CommonParameters</span></span>
<span data-ttu-id="fc8f9-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc8f9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc8f9-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc8f9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc8f9-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc8f9-144">INPUTS</span></span>

### <span data-ttu-id="fc8f9-145">System. String</span><span class="sxs-lookup"><span data-stu-id="fc8f9-145">System.String</span></span>

## <span data-ttu-id="fc8f9-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc8f9-146">OUTPUTS</span></span>

## <span data-ttu-id="fc8f9-147">Note</span><span class="sxs-lookup"><span data-stu-id="fc8f9-147">NOTES</span></span>

## <span data-ttu-id="fc8f9-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc8f9-148">RELATED LINKS</span></span>
