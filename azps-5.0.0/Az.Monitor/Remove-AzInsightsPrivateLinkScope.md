---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 358eb796a156949520cf8cf0c073ee08a6537e2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203367"
---
# <span data-ttu-id="0c8be-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0c8be-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="0c8be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c8be-102">SYNOPSIS</span></span>
<span data-ttu-id="0c8be-103">eliminare l'ambito del collegamento privato</span><span class="sxs-lookup"><span data-stu-id="0c8be-103">delete private link scope</span></span>

## <span data-ttu-id="0c8be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c8be-104">SYNTAX</span></span>

### <span data-ttu-id="0c8be-105">ByResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c8be-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c8be-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c8be-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c8be-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c8be-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c8be-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c8be-108">DESCRIPTION</span></span>
<span data-ttu-id="0c8be-109">eliminare l'ambito del collegamento privato</span><span class="sxs-lookup"><span data-stu-id="0c8be-109">delete private link scope</span></span>

## <span data-ttu-id="0c8be-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c8be-110">EXAMPLES</span></span>

### <span data-ttu-id="0c8be-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0c8be-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="0c8be-112">eliminare l'ambito dei collegamenti privati con il nome "scope_name" in gruppo risorse "rg_name"</span><span class="sxs-lookup"><span data-stu-id="0c8be-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="0c8be-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0c8be-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="0c8be-114">eliminare l'ambito dei collegamenti privati con ID risorsa</span><span class="sxs-lookup"><span data-stu-id="0c8be-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="0c8be-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0c8be-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="0c8be-116">eliminare l'ambito dei collegamenti privati con l'oggetto ambito del collegamento privato di input</span><span class="sxs-lookup"><span data-stu-id="0c8be-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="0c8be-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c8be-117">PARAMETERS</span></span>

### <span data-ttu-id="0c8be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c8be-118">-DefaultProfile</span></span>
<span data-ttu-id="0c8be-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c8be-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c8be-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c8be-120">-InputObject</span></span>
<span data-ttu-id="0c8be-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0c8be-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="0c8be-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c8be-122">-Name</span></span>
<span data-ttu-id="0c8be-123">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="0c8be-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="0c8be-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c8be-124">-ResourceGroupName</span></span>
<span data-ttu-id="0c8be-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="0c8be-125">Resource Group Name</span></span>

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

### <span data-ttu-id="0c8be-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c8be-126">-ResourceId</span></span>
<span data-ttu-id="0c8be-127">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="0c8be-127">Resource Id</span></span>

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

### <span data-ttu-id="0c8be-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c8be-128">-Confirm</span></span>
<span data-ttu-id="0c8be-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c8be-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c8be-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c8be-130">-WhatIf</span></span>
<span data-ttu-id="0c8be-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c8be-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c8be-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c8be-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c8be-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c8be-133">CommonParameters</span></span>
<span data-ttu-id="0c8be-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c8be-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c8be-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c8be-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c8be-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c8be-136">INPUTS</span></span>

### <span data-ttu-id="0c8be-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0c8be-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="0c8be-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0c8be-138">System.String</span></span>

## <span data-ttu-id="0c8be-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c8be-139">OUTPUTS</span></span>

### <span data-ttu-id="0c8be-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c8be-140">System.Boolean</span></span>

## <span data-ttu-id="0c8be-141">Note</span><span class="sxs-lookup"><span data-stu-id="0c8be-141">NOTES</span></span>

## <span data-ttu-id="0c8be-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c8be-142">RELATED LINKS</span></span>
