---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 7465a74db4da777d60e097fe959ef69bed11918c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200853"
---
# <span data-ttu-id="2d24e-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="2d24e-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="2d24e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d24e-102">SYNOPSIS</span></span>
<span data-ttu-id="2d24e-103">Avvia la cache HPC.</span><span class="sxs-lookup"><span data-stu-id="2d24e-103">Starts HPC cache.</span></span>

## <span data-ttu-id="2d24e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d24e-104">SYNTAX</span></span>

### <span data-ttu-id="2d24e-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2d24e-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d24e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d24e-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d24e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d24e-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d24e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d24e-108">DESCRIPTION</span></span>
<span data-ttu-id="2d24e-109">Il cmdlet **Start-AzHpcCache** avvia una cache HPC di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d24e-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="2d24e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d24e-110">EXAMPLES</span></span>

### <span data-ttu-id="2d24e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2d24e-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="2d24e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d24e-112">PARAMETERS</span></span>

### <span data-ttu-id="2d24e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d24e-113">-AsJob</span></span>
<span data-ttu-id="2d24e-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2d24e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d24e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d24e-115">-DefaultProfile</span></span>
<span data-ttu-id="2d24e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2d24e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d24e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2d24e-117">-Force</span></span>
<span data-ttu-id="2d24e-118">Indica che il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="2d24e-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="2d24e-119">Per impostazione predefinita, questo cmdlet richiede di confermare che si vuole avviare la cache.</span><span class="sxs-lookup"><span data-stu-id="2d24e-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="2d24e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d24e-120">-InputObject</span></span>
<span data-ttu-id="2d24e-121">L'oggetto cache da avviare.</span><span class="sxs-lookup"><span data-stu-id="2d24e-121">The cache object to start.</span></span>

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

### <span data-ttu-id="2d24e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d24e-122">-Name</span></span>
<span data-ttu-id="2d24e-123">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="2d24e-123">Name of cache.</span></span>

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

### <span data-ttu-id="2d24e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d24e-124">-PassThru</span></span>
<span data-ttu-id="2d24e-125">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="2d24e-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2d24e-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="2d24e-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2d24e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d24e-127">-ResourceGroupName</span></span>
<span data-ttu-id="2d24e-128">Nome del gruppo di risorse in cui si vuole avviare la cache.</span><span class="sxs-lookup"><span data-stu-id="2d24e-128">Name of resource group under which you want to start cache.</span></span>

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

### <span data-ttu-id="2d24e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d24e-129">-ResourceId</span></span>
<span data-ttu-id="2d24e-130">ID risorsa della cache</span><span class="sxs-lookup"><span data-stu-id="2d24e-130">The resource id of the Cache</span></span>

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

### <span data-ttu-id="2d24e-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2d24e-131">-Confirm</span></span>
<span data-ttu-id="2d24e-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d24e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d24e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d24e-133">-WhatIf</span></span>
<span data-ttu-id="2d24e-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d24e-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d24e-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d24e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d24e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d24e-136">CommonParameters</span></span>
<span data-ttu-id="2d24e-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d24e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d24e-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d24e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d24e-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d24e-139">INPUTS</span></span>

### <span data-ttu-id="2d24e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2d24e-140">System.String</span></span>

## <span data-ttu-id="2d24e-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d24e-141">OUTPUTS</span></span>

## <span data-ttu-id="2d24e-142">Note</span><span class="sxs-lookup"><span data-stu-id="2d24e-142">NOTES</span></span>

## <span data-ttu-id="2d24e-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d24e-143">RELATED LINKS</span></span>
