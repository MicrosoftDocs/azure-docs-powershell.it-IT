---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 358eb796a156949520cf8cf0c073ee08a6537e2f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345499"
---
# <span data-ttu-id="9a380-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="9a380-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="9a380-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a380-102">SYNOPSIS</span></span>
<span data-ttu-id="9a380-103">eliminare l'ambito del collegamento privato</span><span class="sxs-lookup"><span data-stu-id="9a380-103">delete private link scope</span></span>

## <span data-ttu-id="9a380-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a380-104">SYNTAX</span></span>

### <span data-ttu-id="9a380-105">ByResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9a380-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a380-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a380-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a380-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a380-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a380-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a380-108">DESCRIPTION</span></span>
<span data-ttu-id="9a380-109">eliminare l'ambito del collegamento privato</span><span class="sxs-lookup"><span data-stu-id="9a380-109">delete private link scope</span></span>

## <span data-ttu-id="9a380-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a380-110">EXAMPLES</span></span>

### <span data-ttu-id="9a380-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9a380-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="9a380-112">eliminare l'ambito dei collegamenti privati con il nome "scope_name" in gruppo risorse "rg_name"</span><span class="sxs-lookup"><span data-stu-id="9a380-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="9a380-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9a380-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="9a380-114">eliminare l'ambito dei collegamenti privati con ID risorsa</span><span class="sxs-lookup"><span data-stu-id="9a380-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="9a380-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9a380-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="9a380-116">eliminare l'ambito dei collegamenti privati con l'oggetto ambito del collegamento privato di input</span><span class="sxs-lookup"><span data-stu-id="9a380-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="9a380-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a380-117">PARAMETERS</span></span>

### <span data-ttu-id="9a380-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a380-118">-DefaultProfile</span></span>
<span data-ttu-id="9a380-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a380-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a380-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a380-120">-InputObject</span></span>
<span data-ttu-id="9a380-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="9a380-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="9a380-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a380-122">-Name</span></span>
<span data-ttu-id="9a380-123">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="9a380-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="9a380-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a380-124">-ResourceGroupName</span></span>
<span data-ttu-id="9a380-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="9a380-125">Resource Group Name</span></span>

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

### <span data-ttu-id="9a380-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a380-126">-ResourceId</span></span>
<span data-ttu-id="9a380-127">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="9a380-127">Resource Id</span></span>

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

### <span data-ttu-id="9a380-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9a380-128">-Confirm</span></span>
<span data-ttu-id="9a380-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a380-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a380-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a380-130">-WhatIf</span></span>
<span data-ttu-id="9a380-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a380-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a380-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a380-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a380-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a380-133">CommonParameters</span></span>
<span data-ttu-id="9a380-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a380-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a380-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a380-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a380-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a380-136">INPUTS</span></span>

### <span data-ttu-id="9a380-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="9a380-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="9a380-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9a380-138">System.String</span></span>

## <span data-ttu-id="9a380-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a380-139">OUTPUTS</span></span>

### <span data-ttu-id="9a380-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a380-140">System.Boolean</span></span>

## <span data-ttu-id="9a380-141">Note</span><span class="sxs-lookup"><span data-stu-id="9a380-141">NOTES</span></span>

## <span data-ttu-id="9a380-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a380-142">RELATED LINKS</span></span>
