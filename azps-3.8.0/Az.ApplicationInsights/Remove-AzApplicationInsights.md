---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: d9aa737a34e106fc8514c0e9bbbcfb70b73f015a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022101"
---
# <span data-ttu-id="db6bc-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="db6bc-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="db6bc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db6bc-102">SYNOPSIS</span></span>
<span data-ttu-id="db6bc-103">Rimuovere una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="db6bc-103">Remove an application insights resource</span></span>

## <span data-ttu-id="db6bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db6bc-104">SYNTAX</span></span>

### <span data-ttu-id="db6bc-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db6bc-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db6bc-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db6bc-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db6bc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db6bc-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db6bc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db6bc-108">DESCRIPTION</span></span>
<span data-ttu-id="db6bc-109">Rimuovere una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="db6bc-109">Remove an application insights resource</span></span>

## <span data-ttu-id="db6bc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db6bc-110">EXAMPLES</span></span>

### <span data-ttu-id="db6bc-111">Esempio 1 rimuovere una risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="db6bc-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="db6bc-112">Rimuovere una risorsa Insights applicazione denominata "test" nel gruppo risorse "testgroup"</span><span class="sxs-lookup"><span data-stu-id="db6bc-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="db6bc-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db6bc-113">PARAMETERS</span></span>

### <span data-ttu-id="db6bc-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="db6bc-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="db6bc-115">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="db6bc-115">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db6bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6bc-116">-DefaultProfile</span></span>
<span data-ttu-id="db6bc-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db6bc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db6bc-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="db6bc-118">-Name</span></span>
<span data-ttu-id="db6bc-119">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="db6bc-119">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6bc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db6bc-120">-PassThru</span></span>
<span data-ttu-id="db6bc-121">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="db6bc-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="db6bc-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="db6bc-122">This parameter is optional.</span></span> <span data-ttu-id="db6bc-123">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="db6bc-123">Default value is false.</span></span>

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

### <span data-ttu-id="db6bc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db6bc-124">-ResourceGroupName</span></span>
<span data-ttu-id="db6bc-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db6bc-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6bc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db6bc-126">-ResourceId</span></span>
<span data-ttu-id="db6bc-127">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="db6bc-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db6bc-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db6bc-128">-Confirm</span></span>
<span data-ttu-id="db6bc-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db6bc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db6bc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db6bc-130">-WhatIf</span></span>
<span data-ttu-id="db6bc-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db6bc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db6bc-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db6bc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db6bc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6bc-133">CommonParameters</span></span>
<span data-ttu-id="db6bc-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db6bc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6bc-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db6bc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6bc-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db6bc-136">INPUTS</span></span>

### <span data-ttu-id="db6bc-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="db6bc-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="db6bc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="db6bc-138">System.String</span></span>

## <span data-ttu-id="db6bc-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db6bc-139">OUTPUTS</span></span>

### <span data-ttu-id="db6bc-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db6bc-140">System.Boolean</span></span>

## <span data-ttu-id="db6bc-141">Note</span><span class="sxs-lookup"><span data-stu-id="db6bc-141">NOTES</span></span>

## <span data-ttu-id="db6bc-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db6bc-142">RELATED LINKS</span></span>
