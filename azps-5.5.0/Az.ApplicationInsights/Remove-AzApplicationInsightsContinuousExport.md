---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 6138d3d454a23cdbdbaa67d7ee668c5ffa752b4a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210235"
---
# <span data-ttu-id="976a5-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="976a5-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="976a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="976a5-102">SYNOPSIS</span></span>
<span data-ttu-id="976a5-103">Rimuovere una configurazione di esportazione continua in una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="976a5-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="976a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="976a5-104">SYNTAX</span></span>

### <span data-ttu-id="976a5-105">ComponentNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="976a5-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="976a5-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="976a5-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="976a5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="976a5-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="976a5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="976a5-108">DESCRIPTION</span></span>
<span data-ttu-id="976a5-109">Rimuovere una configurazione di esportazione continua in una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="976a5-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="976a5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="976a5-110">EXAMPLES</span></span>

### <span data-ttu-id="976a5-111">Esempio 1: Rimuovere una configurazione di esportazione continua in una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="976a5-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="976a5-112">Rimuovere la configurazione continua di Application Insights con id esportazione "uGOoki0jQsyEs3IdQ83Q4QsNr4=" per la risorsa denominata "test" nel gruppo di risorse "gruppo di test"</span><span class="sxs-lookup"><span data-stu-id="976a5-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="976a5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="976a5-113">PARAMETERS</span></span>

### <span data-ttu-id="976a5-114">-ApplicationInsightsInsightsIn</span><span class="sxs-lookup"><span data-stu-id="976a5-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="976a5-115">Oggetto componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="976a5-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="976a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="976a5-116">-DefaultProfile</span></span>
<span data-ttu-id="976a5-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="976a5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="976a5-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="976a5-118">-ExportId</span></span>
<span data-ttu-id="976a5-119">ID di esportazione continua di Application Insights.</span><span class="sxs-lookup"><span data-stu-id="976a5-119">Application Insights Continuous Export ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="976a5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="976a5-120">-Name</span></span>
<span data-ttu-id="976a5-121">Nome del componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="976a5-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="976a5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="976a5-122">-PassThru</span></span>
<span data-ttu-id="976a5-123">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="976a5-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="976a5-124">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="976a5-124">This parameter is optional.</span></span> <span data-ttu-id="976a5-125">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="976a5-125">Default value is false.</span></span>

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

### <span data-ttu-id="976a5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="976a5-126">-ResourceGroupName</span></span>
<span data-ttu-id="976a5-127">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="976a5-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="976a5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="976a5-128">-ResourceId</span></span>
<span data-ttu-id="976a5-129">ID risorsa componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="976a5-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="976a5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="976a5-130">-Confirm</span></span>
<span data-ttu-id="976a5-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="976a5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="976a5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="976a5-132">-WhatIf</span></span>
<span data-ttu-id="976a5-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="976a5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="976a5-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="976a5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="976a5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="976a5-135">CommonParameters</span></span>
<span data-ttu-id="976a5-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="976a5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="976a5-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="976a5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="976a5-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="976a5-138">INPUTS</span></span>

### <span data-ttu-id="976a5-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="976a5-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="976a5-140">System.String</span><span class="sxs-lookup"><span data-stu-id="976a5-140">System.String</span></span>

## <span data-ttu-id="976a5-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="976a5-141">OUTPUTS</span></span>

### <span data-ttu-id="976a5-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="976a5-142">System.Boolean</span></span>

## <span data-ttu-id="976a5-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="976a5-143">NOTES</span></span>

## <span data-ttu-id="976a5-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="976a5-144">RELATED LINKS</span></span>
