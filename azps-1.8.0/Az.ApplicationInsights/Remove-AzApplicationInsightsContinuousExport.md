---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 0265a273cb575d2cc3a165afae8f7a2090499cdc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685117"
---
# <span data-ttu-id="efc0f-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="efc0f-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="efc0f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="efc0f-102">SYNOPSIS</span></span>
<span data-ttu-id="efc0f-103">Rimuovere una configurazione di esportazione cotinuous in una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="efc0f-103">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="efc0f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="efc0f-104">SYNTAX</span></span>

### <span data-ttu-id="efc0f-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="efc0f-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="efc0f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efc0f-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="efc0f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efc0f-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efc0f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efc0f-108">DESCRIPTION</span></span>
<span data-ttu-id="efc0f-109">Rimuovere una configurazione di esportazione cotinuous in una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="efc0f-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="efc0f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="efc0f-110">EXAMPLES</span></span>

### <span data-ttu-id="efc0f-111">Esempio 1 rimuovere una configurazione di esportazione cotinuous in una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="efc0f-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="efc0f-112">Rimuovere le informazioni approfondite dell'applicazione configurazione di esportazione continua con l'ID esportazione "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" per la risorsa denominata "test" nel gruppo risorse "testgroup"</span><span class="sxs-lookup"><span data-stu-id="efc0f-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="efc0f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="efc0f-113">PARAMETERS</span></span>

### <span data-ttu-id="efc0f-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="efc0f-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="efc0f-115">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="efc0f-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="efc0f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc0f-116">-DefaultProfile</span></span>
<span data-ttu-id="efc0f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="efc0f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efc0f-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="efc0f-118">-ExportId</span></span>
<span data-ttu-id="efc0f-119">ID dell'esportazione continuo dell'applicazione Insights.</span><span class="sxs-lookup"><span data-stu-id="efc0f-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="efc0f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="efc0f-120">-Name</span></span>
<span data-ttu-id="efc0f-121">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="efc0f-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="efc0f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efc0f-122">-PassThru</span></span>
<span data-ttu-id="efc0f-123">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="efc0f-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="efc0f-124">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="efc0f-124">This parameter is optional.</span></span> <span data-ttu-id="efc0f-125">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="efc0f-125">Default value is false.</span></span>

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

### <span data-ttu-id="efc0f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc0f-126">-ResourceGroupName</span></span>
<span data-ttu-id="efc0f-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="efc0f-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="efc0f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efc0f-128">-ResourceId</span></span>
<span data-ttu-id="efc0f-129">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="efc0f-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="efc0f-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="efc0f-130">-Confirm</span></span>
<span data-ttu-id="efc0f-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efc0f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efc0f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efc0f-132">-WhatIf</span></span>
<span data-ttu-id="efc0f-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efc0f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efc0f-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efc0f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efc0f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc0f-135">CommonParameters</span></span>
<span data-ttu-id="efc0f-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc0f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc0f-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efc0f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc0f-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="efc0f-138">INPUTS</span></span>

### <span data-ttu-id="efc0f-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="efc0f-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="efc0f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="efc0f-140">System.String</span></span>

## <span data-ttu-id="efc0f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="efc0f-141">OUTPUTS</span></span>

### <span data-ttu-id="efc0f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="efc0f-142">System.Boolean</span></span>

## <span data-ttu-id="efc0f-143">Note</span><span class="sxs-lookup"><span data-stu-id="efc0f-143">NOTES</span></span>

## <span data-ttu-id="efc0f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="efc0f-144">RELATED LINKS</span></span>