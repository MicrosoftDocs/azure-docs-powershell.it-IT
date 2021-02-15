---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 53ebb6d1a7bcfc35dafb09c377b2a4a023e327d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182247"
---
# <span data-ttu-id="b0c47-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="b0c47-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="b0c47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0c47-102">SYNOPSIS</span></span>
<span data-ttu-id="b0c47-103">Rimuovere una chiave API di Application Insights per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="b0c47-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="b0c47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0c47-104">SYNTAX</span></span>

### <span data-ttu-id="b0c47-105">ComponentNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b0c47-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0c47-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c47-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0c47-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c47-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0c47-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b0c47-108">DESCRIPTION</span></span>
<span data-ttu-id="b0c47-109">Rimuovere una chiave API di Application Insights per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="b0c47-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="b0c47-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0c47-110">EXAMPLES</span></span>

### <span data-ttu-id="b0c47-111">Esempio 1: rimuovere una chiave API di Application Insights per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="b0c47-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="b0c47-112">Rimuovere la specifica chiave api di Application Insights che id è "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" per la risorsa "test" nel gruppo di risorse "testGroup".</span><span class="sxs-lookup"><span data-stu-id="b0c47-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="b0c47-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0c47-113">PARAMETERS</span></span>

### <span data-ttu-id="b0c47-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="b0c47-114">-ApiKeyId</span></span>
<span data-ttu-id="b0c47-115">ID chiave API Application Insights.</span><span class="sxs-lookup"><span data-stu-id="b0c47-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="b0c47-116">-ApplicationInsightsInsightsIn</span><span class="sxs-lookup"><span data-stu-id="b0c47-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="b0c47-117">Oggetto componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="b0c47-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="b0c47-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0c47-118">-DefaultProfile</span></span>
<span data-ttu-id="b0c47-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0c47-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0c47-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b0c47-120">-Name</span></span>
<span data-ttu-id="b0c47-121">Nome del componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="b0c47-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="b0c47-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0c47-122">-PassThru</span></span>
<span data-ttu-id="b0c47-123">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="b0c47-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="b0c47-124">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b0c47-124">This parameter is optional.</span></span> <span data-ttu-id="b0c47-125">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="b0c47-125">Default value is false.</span></span>

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

### <span data-ttu-id="b0c47-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0c47-126">-ResourceGroupName</span></span>
<span data-ttu-id="b0c47-127">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b0c47-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="b0c47-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0c47-128">-ResourceId</span></span>
<span data-ttu-id="b0c47-129">ID risorsa componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="b0c47-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="b0c47-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0c47-130">-Confirm</span></span>
<span data-ttu-id="b0c47-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0c47-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0c47-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0c47-132">-WhatIf</span></span>
<span data-ttu-id="b0c47-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0c47-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0c47-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0c47-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0c47-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0c47-135">CommonParameters</span></span>
<span data-ttu-id="b0c47-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0c47-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0c47-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0c47-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0c47-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="b0c47-138">INPUTS</span></span>

### <span data-ttu-id="b0c47-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="b0c47-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="b0c47-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b0c47-140">System.String</span></span>

## <span data-ttu-id="b0c47-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0c47-141">OUTPUTS</span></span>

### <span data-ttu-id="b0c47-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b0c47-142">System.Boolean</span></span>

## <span data-ttu-id="b0c47-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="b0c47-143">NOTES</span></span>

## <span data-ttu-id="b0c47-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0c47-144">RELATED LINKS</span></span>
