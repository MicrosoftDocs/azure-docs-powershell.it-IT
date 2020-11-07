---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864243"
---
# <span data-ttu-id="a5c29-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="a5c29-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="a5c29-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5c29-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c29-103">Elimina per la risorsa con ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="a5c29-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="a5c29-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5c29-104">SYNTAX</span></span>

### <span data-ttu-id="a5c29-105">ByScopeParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a5c29-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c29-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5c29-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c29-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5c29-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5c29-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5c29-108">DESCRIPTION</span></span>
<span data-ttu-id="a5c29-109">Elimina per la risorsa con ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="a5c29-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="a5c29-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5c29-110">EXAMPLES</span></span>

### <span data-ttu-id="a5c29-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a5c29-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="a5c29-112">eliminare una risorsa con ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="a5c29-112">delete private link scoped resource</span></span>

## <span data-ttu-id="a5c29-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5c29-113">PARAMETERS</span></span>

### <span data-ttu-id="a5c29-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c29-114">-DefaultProfile</span></span>
<span data-ttu-id="a5c29-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5c29-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5c29-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5c29-116">-InputObject</span></span>
<span data-ttu-id="a5c29-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a5c29-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="a5c29-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5c29-118">-Name</span></span>
<span data-ttu-id="a5c29-119">Nome risorsa con ambito</span><span class="sxs-lookup"><span data-stu-id="a5c29-119">Scoped resource Name</span></span>

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

### <span data-ttu-id="a5c29-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c29-120">-ResourceGroupName</span></span>
<span data-ttu-id="a5c29-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a5c29-121">Resource Group Name</span></span>

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

### <span data-ttu-id="a5c29-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5c29-122">-ResourceId</span></span>
<span data-ttu-id="a5c29-123">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="a5c29-123">Resource Id</span></span>

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

### <span data-ttu-id="a5c29-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="a5c29-124">-ScopeName</span></span>
<span data-ttu-id="a5c29-125">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="a5c29-125">Private Link Scope Name</span></span>

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

### <span data-ttu-id="a5c29-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a5c29-126">-Confirm</span></span>
<span data-ttu-id="a5c29-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5c29-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5c29-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5c29-128">-WhatIf</span></span>
<span data-ttu-id="a5c29-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5c29-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5c29-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5c29-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5c29-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c29-131">CommonParameters</span></span>
<span data-ttu-id="a5c29-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5c29-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c29-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5c29-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c29-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5c29-134">INPUTS</span></span>

### <span data-ttu-id="a5c29-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a5c29-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="a5c29-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a5c29-136">System.String</span></span>

## <span data-ttu-id="a5c29-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5c29-137">OUTPUTS</span></span>

### <span data-ttu-id="a5c29-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5c29-138">System.Boolean</span></span>

## <span data-ttu-id="a5c29-139">Note</span><span class="sxs-lookup"><span data-stu-id="a5c29-139">NOTES</span></span>

## <span data-ttu-id="a5c29-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5c29-140">RELATED LINKS</span></span>
