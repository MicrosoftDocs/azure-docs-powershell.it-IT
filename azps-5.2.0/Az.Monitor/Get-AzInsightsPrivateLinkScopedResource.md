---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: f3d00ba82bbafce42cca49c60d443cd244f83df3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367622"
---
# <span data-ttu-id="304b5-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="304b5-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="304b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="304b5-102">SYNOPSIS</span></span>
<span data-ttu-id="304b5-103">Ottenere una risorsa con ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="304b5-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="304b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="304b5-104">SYNTAX</span></span>

### <span data-ttu-id="304b5-105">ByScopeParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="304b5-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="304b5-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="304b5-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="304b5-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="304b5-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="304b5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="304b5-108">DESCRIPTION</span></span>
<span data-ttu-id="304b5-109">Get o List per la risorsa con ambito collegamento privato, la risorsa con ambito può essere un componente di area di lavoro analisi log o Application Insights</span><span class="sxs-lookup"><span data-stu-id="304b5-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="304b5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="304b5-110">EXAMPLES</span></span>

### <span data-ttu-id="304b5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="304b5-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="304b5-112">Elenco delle risorse nell'ambito di un collegamento privato "scope_name"</span><span class="sxs-lookup"><span data-stu-id="304b5-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="304b5-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="304b5-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="304b5-114">Ottenere la risorsa con ambito in ambito di collegamento privato "scope_name" con il nome "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="304b5-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="304b5-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="304b5-115">PARAMETERS</span></span>

### <span data-ttu-id="304b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="304b5-116">-DefaultProfile</span></span>
<span data-ttu-id="304b5-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="304b5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="304b5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="304b5-118">-InputObject</span></span>
<span data-ttu-id="304b5-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="304b5-119">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="304b5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="304b5-120">-Name</span></span>
<span data-ttu-id="304b5-121">Nome risorsa con ambito</span><span class="sxs-lookup"><span data-stu-id="304b5-121">Scoped resource Name</span></span>

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

### <span data-ttu-id="304b5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="304b5-122">-ResourceGroupName</span></span>
<span data-ttu-id="304b5-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="304b5-123">Resource Group Name</span></span>

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

### <span data-ttu-id="304b5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="304b5-124">-ResourceId</span></span>
<span data-ttu-id="304b5-125">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="304b5-125">Resource Id</span></span>

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

### <span data-ttu-id="304b5-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="304b5-126">-ScopeName</span></span>
<span data-ttu-id="304b5-127">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="304b5-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="304b5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="304b5-128">CommonParameters</span></span>
<span data-ttu-id="304b5-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="304b5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="304b5-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="304b5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="304b5-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="304b5-131">INPUTS</span></span>

### <span data-ttu-id="304b5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="304b5-132">System.String</span></span>

## <span data-ttu-id="304b5-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="304b5-133">OUTPUTS</span></span>

### <span data-ttu-id="304b5-134">icrosoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="304b5-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="304b5-135">Note</span><span class="sxs-lookup"><span data-stu-id="304b5-135">NOTES</span></span>

## <span data-ttu-id="304b5-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="304b5-136">RELATED LINKS</span></span>
