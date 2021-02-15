---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: f3d00ba82bbafce42cca49c60d443cd244f83df3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207139"
---
# <span data-ttu-id="bbf26-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="bbf26-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="bbf26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbf26-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf26-103">Ottieni per risorsa con ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="bbf26-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="bbf26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbf26-104">SYNTAX</span></span>

### <span data-ttu-id="bbf26-105">ByScopeParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bbf26-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbf26-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbf26-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbf26-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbf26-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bbf26-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bbf26-108">DESCRIPTION</span></span>
<span data-ttu-id="bbf26-109">Ottenere o elencare una risorsa con ambito collegamento privato, la risorsa con ambito può essere l'area di lavoro Analisi log o il componente Application Insights</span><span class="sxs-lookup"><span data-stu-id="bbf26-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="bbf26-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbf26-110">EXAMPLES</span></span>

### <span data-ttu-id="bbf26-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bbf26-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="bbf26-112">Elencare le risorse con ambito nell'ambito del collegamento privato "scope_name"</span><span class="sxs-lookup"><span data-stu-id="bbf26-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="bbf26-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bbf26-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="bbf26-114">Ottenere la risorsa con ambito nell'ambito del collegamento privato "scope_name" con nome "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="bbf26-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="bbf26-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbf26-115">PARAMETERS</span></span>

### <span data-ttu-id="bbf26-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf26-116">-DefaultProfile</span></span>
<span data-ttu-id="bbf26-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bbf26-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbf26-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbf26-118">-InputObject</span></span>
<span data-ttu-id="bbf26-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="bbf26-119">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="bbf26-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bbf26-120">-Name</span></span>
<span data-ttu-id="bbf26-121">Nome risorsa con ambito</span><span class="sxs-lookup"><span data-stu-id="bbf26-121">Scoped resource Name</span></span>

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

### <span data-ttu-id="bbf26-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbf26-122">-ResourceGroupName</span></span>
<span data-ttu-id="bbf26-123">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="bbf26-123">Resource Group Name</span></span>

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

### <span data-ttu-id="bbf26-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbf26-124">-ResourceId</span></span>
<span data-ttu-id="bbf26-125">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="bbf26-125">Resource Id</span></span>

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

### <span data-ttu-id="bbf26-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="bbf26-126">-ScopeName</span></span>
<span data-ttu-id="bbf26-127">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="bbf26-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="bbf26-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf26-128">CommonParameters</span></span>
<span data-ttu-id="bbf26-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbf26-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf26-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bbf26-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf26-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="bbf26-131">INPUTS</span></span>

### <span data-ttu-id="bbf26-132">System.String</span><span class="sxs-lookup"><span data-stu-id="bbf26-132">System.String</span></span>

## <span data-ttu-id="bbf26-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbf26-133">OUTPUTS</span></span>

### <span data-ttu-id="bbf26-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="bbf26-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="bbf26-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="bbf26-135">NOTES</span></span>

## <span data-ttu-id="bbf26-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbf26-136">RELATED LINKS</span></span>
