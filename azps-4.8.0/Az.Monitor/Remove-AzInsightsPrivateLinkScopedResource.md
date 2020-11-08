---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189575"
---
# <span data-ttu-id="426f2-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="426f2-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="426f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="426f2-102">SYNOPSIS</span></span>
<span data-ttu-id="426f2-103">Elimina per la risorsa con ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="426f2-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="426f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="426f2-104">SYNTAX</span></span>

### <span data-ttu-id="426f2-105">ByScopeParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="426f2-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="426f2-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="426f2-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="426f2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="426f2-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="426f2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="426f2-108">DESCRIPTION</span></span>
<span data-ttu-id="426f2-109">Elimina per la risorsa con ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="426f2-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="426f2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="426f2-110">EXAMPLES</span></span>

### <span data-ttu-id="426f2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="426f2-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="426f2-112">eliminare una risorsa con ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="426f2-112">delete private link scoped resource</span></span>

## <span data-ttu-id="426f2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="426f2-113">PARAMETERS</span></span>

### <span data-ttu-id="426f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="426f2-114">-DefaultProfile</span></span>
<span data-ttu-id="426f2-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="426f2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="426f2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="426f2-116">-InputObject</span></span>
<span data-ttu-id="426f2-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="426f2-117">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="426f2-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="426f2-118">-Name</span></span>
<span data-ttu-id="426f2-119">Nome risorsa con ambito</span><span class="sxs-lookup"><span data-stu-id="426f2-119">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426f2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="426f2-120">-ResourceGroupName</span></span>
<span data-ttu-id="426f2-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="426f2-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426f2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="426f2-122">-ResourceId</span></span>
<span data-ttu-id="426f2-123">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="426f2-123">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426f2-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="426f2-124">-ScopeName</span></span>
<span data-ttu-id="426f2-125">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="426f2-125">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426f2-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="426f2-126">-Confirm</span></span>
<span data-ttu-id="426f2-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="426f2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="426f2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="426f2-128">-WhatIf</span></span>
<span data-ttu-id="426f2-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="426f2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="426f2-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="426f2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="426f2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="426f2-131">CommonParameters</span></span>
<span data-ttu-id="426f2-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="426f2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="426f2-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="426f2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="426f2-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="426f2-134">INPUTS</span></span>

### <span data-ttu-id="426f2-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="426f2-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="426f2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="426f2-136">System.String</span></span>

## <span data-ttu-id="426f2-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="426f2-137">OUTPUTS</span></span>

### <span data-ttu-id="426f2-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="426f2-138">System.Boolean</span></span>

## <span data-ttu-id="426f2-139">Note</span><span class="sxs-lookup"><span data-stu-id="426f2-139">NOTES</span></span>

## <span data-ttu-id="426f2-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="426f2-140">RELATED LINKS</span></span>
