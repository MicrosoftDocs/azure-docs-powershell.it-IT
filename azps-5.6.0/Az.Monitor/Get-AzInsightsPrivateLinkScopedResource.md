---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: ff4e75e2301ef9ae2ccd6f2e5064e06aedc2dbd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980045"
---
# <span data-ttu-id="29c1e-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="29c1e-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="29c1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="29c1e-103">Ottieni per la risorsa con ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="29c1e-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="29c1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29c1e-104">SYNTAX</span></span>

### <span data-ttu-id="29c1e-105">ByScopeParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="29c1e-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29c1e-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29c1e-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29c1e-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29c1e-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29c1e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="29c1e-108">DESCRIPTION</span></span>
<span data-ttu-id="29c1e-109">Ottenere o elencare una risorsa con ambito collegamento privato, la risorsa con ambito può essere l'area di lavoro Analisi log o il componente Application Insights</span><span class="sxs-lookup"><span data-stu-id="29c1e-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="29c1e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29c1e-110">EXAMPLES</span></span>

### <span data-ttu-id="29c1e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="29c1e-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="29c1e-112">Elencare le risorse con ambito nell'ambito del collegamento privato "scope_name"</span><span class="sxs-lookup"><span data-stu-id="29c1e-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="29c1e-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="29c1e-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="29c1e-114">Ottenere la risorsa con ambito nell'ambito del collegamento privato "scope_name" con nome "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="29c1e-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="29c1e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29c1e-115">PARAMETERS</span></span>

### <span data-ttu-id="29c1e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29c1e-116">-DefaultProfile</span></span>
<span data-ttu-id="29c1e-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="29c1e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29c1e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29c1e-118">-InputObject</span></span>
<span data-ttu-id="29c1e-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="29c1e-119">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c1e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="29c1e-120">-Name</span></span>
<span data-ttu-id="29c1e-121">Nome risorsa con ambito</span><span class="sxs-lookup"><span data-stu-id="29c1e-121">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c1e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29c1e-122">-ResourceGroupName</span></span>
<span data-ttu-id="29c1e-123">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="29c1e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="29c1e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29c1e-124">-ResourceId</span></span>
<span data-ttu-id="29c1e-125">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="29c1e-125">Resource Id</span></span>

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

### <span data-ttu-id="29c1e-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="29c1e-126">-ScopeName</span></span>
<span data-ttu-id="29c1e-127">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="29c1e-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="29c1e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c1e-128">CommonParameters</span></span>
<span data-ttu-id="29c1e-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29c1e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c1e-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="29c1e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c1e-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="29c1e-131">INPUTS</span></span>

### <span data-ttu-id="29c1e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="29c1e-132">System.String</span></span>

## <span data-ttu-id="29c1e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29c1e-133">OUTPUTS</span></span>

### <span data-ttu-id="29c1e-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="29c1e-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="29c1e-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="29c1e-135">NOTES</span></span>

## <span data-ttu-id="29c1e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29c1e-136">RELATED LINKS</span></span>
