---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 93e97906fc7e985d522f5af9d678392741a9022b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474054"
---
# <span data-ttu-id="0da6c-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0da6c-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="0da6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0da6c-102">SYNOPSIS</span></span>
<span data-ttu-id="0da6c-103">Aggiornamento per l'ambito dei collegamenti privati</span><span class="sxs-lookup"><span data-stu-id="0da6c-103">Update for private link scope</span></span>

## <span data-ttu-id="0da6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0da6c-104">SYNTAX</span></span>

### <span data-ttu-id="0da6c-105">ByResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0da6c-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0da6c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0da6c-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0da6c-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0da6c-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0da6c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0da6c-108">DESCRIPTION</span></span>
<span data-ttu-id="0da6c-109">Aggiornamento per l'ambito dei collegamenti privati</span><span class="sxs-lookup"><span data-stu-id="0da6c-109">Update for private link scope</span></span>

## <span data-ttu-id="0da6c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0da6c-110">EXAMPLES</span></span>

### <span data-ttu-id="0da6c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0da6c-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="0da6c-112">aggiornare l'ambito dei collegamenti privati con il nome "scope_name" in gruppo risorse "rg_name" per usare il tag "Key: value"</span><span class="sxs-lookup"><span data-stu-id="0da6c-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="0da6c-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0da6c-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="0da6c-114">aggiornare l'ambito dei collegamenti privati con l'ID risorsa per usare il tag "Key: value"</span><span class="sxs-lookup"><span data-stu-id="0da6c-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="0da6c-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0da6c-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="0da6c-116">aggiornare l'ambito dei collegamenti privati con l'oggetto ambito del collegamento privato di input per usare il tag "Key: value"</span><span class="sxs-lookup"><span data-stu-id="0da6c-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="0da6c-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0da6c-117">PARAMETERS</span></span>

### <span data-ttu-id="0da6c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da6c-118">-DefaultProfile</span></span>
<span data-ttu-id="0da6c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0da6c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0da6c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0da6c-120">-InputObject</span></span>
<span data-ttu-id="0da6c-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0da6c-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="0da6c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0da6c-122">-Name</span></span>
<span data-ttu-id="0da6c-123">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="0da6c-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="0da6c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da6c-124">-ResourceGroupName</span></span>
<span data-ttu-id="0da6c-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="0da6c-125">Resource Group Name</span></span>

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

### <span data-ttu-id="0da6c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0da6c-126">-ResourceId</span></span>
<span data-ttu-id="0da6c-127">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="0da6c-127">Resource Id</span></span>

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

### <span data-ttu-id="0da6c-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="0da6c-128">-Tags</span></span>
<span data-ttu-id="0da6c-129">Tag</span><span class="sxs-lookup"><span data-stu-id="0da6c-129">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da6c-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0da6c-130">-Confirm</span></span>
<span data-ttu-id="0da6c-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0da6c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0da6c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0da6c-132">-WhatIf</span></span>
<span data-ttu-id="0da6c-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0da6c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0da6c-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0da6c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0da6c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da6c-135">CommonParameters</span></span>
<span data-ttu-id="0da6c-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0da6c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da6c-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0da6c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da6c-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0da6c-138">INPUTS</span></span>

### <span data-ttu-id="0da6c-139">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0da6c-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="0da6c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0da6c-140">System.String</span></span>

## <span data-ttu-id="0da6c-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0da6c-141">OUTPUTS</span></span>

### <span data-ttu-id="0da6c-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0da6c-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="0da6c-143">Note</span><span class="sxs-lookup"><span data-stu-id="0da6c-143">NOTES</span></span>

## <span data-ttu-id="0da6c-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0da6c-144">RELATED LINKS</span></span>
