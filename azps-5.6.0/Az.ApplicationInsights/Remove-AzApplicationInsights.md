---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: 089561268233876976598f3cf74cd0a52fef8402
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004846"
---
# <span data-ttu-id="27dc0-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="27dc0-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="27dc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="27dc0-103">Rimuovere una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="27dc0-103">Remove an application insights resource</span></span>

## <span data-ttu-id="27dc0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27dc0-104">SYNTAX</span></span>

### <span data-ttu-id="27dc0-105">ComponentNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27dc0-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27dc0-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27dc0-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27dc0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27dc0-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27dc0-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="27dc0-108">DESCRIPTION</span></span>
<span data-ttu-id="27dc0-109">Rimuovere una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="27dc0-109">Remove an application insights resource</span></span>

## <span data-ttu-id="27dc0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27dc0-110">EXAMPLES</span></span>

### <span data-ttu-id="27dc0-111">Esempio 1: Rimuovere una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="27dc0-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="27dc0-112">Rimuovere una risorsa Application Insights denominata "test" nel gruppo di risorse "gruppo di test"</span><span class="sxs-lookup"><span data-stu-id="27dc0-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="27dc0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27dc0-113">PARAMETERS</span></span>

### <span data-ttu-id="27dc0-114">-ApplicationInsightsInsightsIn</span><span class="sxs-lookup"><span data-stu-id="27dc0-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="27dc0-115">Oggetto componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="27dc0-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="27dc0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27dc0-116">-DefaultProfile</span></span>
<span data-ttu-id="27dc0-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27dc0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27dc0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="27dc0-118">-Name</span></span>
<span data-ttu-id="27dc0-119">Nome del componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="27dc0-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="27dc0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27dc0-120">-PassThru</span></span>
<span data-ttu-id="27dc0-121">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="27dc0-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="27dc0-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="27dc0-122">This parameter is optional.</span></span> <span data-ttu-id="27dc0-123">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="27dc0-123">Default value is false.</span></span>

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

### <span data-ttu-id="27dc0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27dc0-124">-ResourceGroupName</span></span>
<span data-ttu-id="27dc0-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="27dc0-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="27dc0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27dc0-126">-ResourceId</span></span>
<span data-ttu-id="27dc0-127">ID risorsa componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="27dc0-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="27dc0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27dc0-128">-Confirm</span></span>
<span data-ttu-id="27dc0-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27dc0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27dc0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27dc0-130">-WhatIf</span></span>
<span data-ttu-id="27dc0-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27dc0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27dc0-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27dc0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27dc0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27dc0-133">CommonParameters</span></span>
<span data-ttu-id="27dc0-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27dc0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27dc0-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="27dc0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27dc0-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="27dc0-136">INPUTS</span></span>

### <span data-ttu-id="27dc0-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="27dc0-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="27dc0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="27dc0-138">System.String</span></span>

## <span data-ttu-id="27dc0-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27dc0-139">OUTPUTS</span></span>

### <span data-ttu-id="27dc0-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="27dc0-140">System.Boolean</span></span>

## <span data-ttu-id="27dc0-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="27dc0-141">NOTES</span></span>

## <span data-ttu-id="27dc0-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27dc0-142">RELATED LINKS</span></span>
