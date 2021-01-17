---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: fd4dc0dd771029951da4ae375141cc526301de34
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486867"
---
# <span data-ttu-id="788e9-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="788e9-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="788e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="788e9-102">SYNOPSIS</span></span>
<span data-ttu-id="788e9-103">creare per la risorsa con ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="788e9-103">create for private link scoped resource</span></span>

## <span data-ttu-id="788e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="788e9-104">SYNTAX</span></span>

### <span data-ttu-id="788e9-105">ByResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="788e9-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="788e9-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="788e9-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="788e9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="788e9-107">DESCRIPTION</span></span>
<span data-ttu-id="788e9-108">creare per la risorsa con ambito collegamento privato, la risorsa con ambito può essere il componente area di lavoro analisi log o approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="788e9-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="788e9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="788e9-109">EXAMPLES</span></span>

### <span data-ttu-id="788e9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="788e9-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="788e9-111">creare una risorsa con ambito "scoped_resource_name" collegata al componente Insights applicazione "ai_name"</span><span class="sxs-lookup"><span data-stu-id="788e9-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="788e9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="788e9-112">PARAMETERS</span></span>

### <span data-ttu-id="788e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="788e9-113">-DefaultProfile</span></span>
<span data-ttu-id="788e9-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="788e9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="788e9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="788e9-115">-InputObject</span></span>
<span data-ttu-id="788e9-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="788e9-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="788e9-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="788e9-117">-LinkedResourceId</span></span>
<span data-ttu-id="788e9-118">ID risorsa LA/AI da collegare</span><span class="sxs-lookup"><span data-stu-id="788e9-118">LA/AI Resource Id to Link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788e9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="788e9-119">-Name</span></span>
<span data-ttu-id="788e9-120">Nome risorsa con ambito</span><span class="sxs-lookup"><span data-stu-id="788e9-120">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788e9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="788e9-121">-ResourceGroupName</span></span>
<span data-ttu-id="788e9-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="788e9-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788e9-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="788e9-123">-ScopeName</span></span>
<span data-ttu-id="788e9-124">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="788e9-124">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788e9-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="788e9-125">-Confirm</span></span>
<span data-ttu-id="788e9-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="788e9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="788e9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="788e9-127">-WhatIf</span></span>
<span data-ttu-id="788e9-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="788e9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="788e9-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="788e9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="788e9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="788e9-130">CommonParameters</span></span>
<span data-ttu-id="788e9-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="788e9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="788e9-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="788e9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="788e9-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="788e9-133">INPUTS</span></span>

### <span data-ttu-id="788e9-134">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="788e9-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="788e9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="788e9-135">System.String</span></span>

## <span data-ttu-id="788e9-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="788e9-136">OUTPUTS</span></span>

### <span data-ttu-id="788e9-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="788e9-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="788e9-138">Note</span><span class="sxs-lookup"><span data-stu-id="788e9-138">NOTES</span></span>

## <span data-ttu-id="788e9-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="788e9-139">RELATED LINKS</span></span>
