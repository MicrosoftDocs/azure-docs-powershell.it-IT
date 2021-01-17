---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 909f3be2e4a08ff1d1b0538b451ffa93f368d211
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328199"
---
# <span data-ttu-id="4a1cf-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="4a1cf-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="4a1cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a1cf-102">SYNOPSIS</span></span>
<span data-ttu-id="4a1cf-103">Aggiorna i tag in una cache HPC.</span><span class="sxs-lookup"><span data-stu-id="4a1cf-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="4a1cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a1cf-104">SYNTAX</span></span>

### <span data-ttu-id="4a1cf-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a1cf-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a1cf-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a1cf-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a1cf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a1cf-107">DESCRIPTION</span></span>
<span data-ttu-id="4a1cf-108">Il cmdlet **set-AzHpcCache** aggiorna i tag della cache di Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="4a1cf-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="4a1cf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a1cf-109">EXAMPLES</span></span>

### <span data-ttu-id="4a1cf-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4a1cf-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="4a1cf-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a1cf-111">PARAMETERS</span></span>

### <span data-ttu-id="4a1cf-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a1cf-112">-AsJob</span></span>
<span data-ttu-id="4a1cf-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4a1cf-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a1cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a1cf-114">-DefaultProfile</span></span>
<span data-ttu-id="4a1cf-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a1cf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a1cf-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a1cf-116">-InputObject</span></span>
<span data-ttu-id="4a1cf-117">L'oggetto cache da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="4a1cf-117">The cache object to update.</span></span>

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

### <span data-ttu-id="4a1cf-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a1cf-118">-Name</span></span>
<span data-ttu-id="4a1cf-119">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="4a1cf-119">Name of cache.</span></span>

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

### <span data-ttu-id="4a1cf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a1cf-120">-ResourceGroupName</span></span>
<span data-ttu-id="4a1cf-121">Nome del gruppo di risorse in cui si vuole aggiornare la cache.</span><span class="sxs-lookup"><span data-stu-id="4a1cf-121">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="4a1cf-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="4a1cf-122">-Tag</span></span>
<span data-ttu-id="4a1cf-123">Tag da associare alla cache HPC.</span><span class="sxs-lookup"><span data-stu-id="4a1cf-123">The tags to associate with HPC Cache.</span></span> 

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

### <span data-ttu-id="4a1cf-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4a1cf-124">-Confirm</span></span>
<span data-ttu-id="4a1cf-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a1cf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a1cf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a1cf-126">-WhatIf</span></span>
<span data-ttu-id="4a1cf-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a1cf-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a1cf-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a1cf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a1cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a1cf-129">CommonParameters</span></span>
<span data-ttu-id="4a1cf-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a1cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a1cf-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a1cf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a1cf-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a1cf-132">INPUTS</span></span>

### <span data-ttu-id="4a1cf-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4a1cf-133">System.String</span></span>

### <span data-ttu-id="4a1cf-134">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4a1cf-134">System.Int32</span></span>

## <span data-ttu-id="4a1cf-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a1cf-135">OUTPUTS</span></span>

### <span data-ttu-id="4a1cf-136">Microsoft. Azure. PowerShell. Cmdlets. HPCCache. Models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="4a1cf-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="4a1cf-137">Note</span><span class="sxs-lookup"><span data-stu-id="4a1cf-137">NOTES</span></span>

## <span data-ttu-id="4a1cf-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a1cf-138">RELATED LINKS</span></span>
