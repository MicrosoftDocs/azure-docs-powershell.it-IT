---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 95f99f629fd32333e06c6194fcaf51837224f4a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956093"
---
# <span data-ttu-id="dcb4c-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="dcb4c-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="dcb4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcb4c-102">SYNOPSIS</span></span>
<span data-ttu-id="dcb4c-103">Rimuovere una chiave API di Application Insights per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="dcb4c-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="dcb4c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dcb4c-104">SYNTAX</span></span>

### <span data-ttu-id="dcb4c-105">ComponentNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dcb4c-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcb4c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcb4c-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dcb4c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcb4c-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcb4c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dcb4c-108">DESCRIPTION</span></span>
<span data-ttu-id="dcb4c-109">Rimuovere una chiave API di Application Insights per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="dcb4c-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="dcb4c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dcb4c-110">EXAMPLES</span></span>

### <span data-ttu-id="dcb4c-111">Esempio 1: rimuovere una chiave API di Application Insights per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="dcb4c-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="dcb4c-112">Rimuovere la specifica chiave api di Application Insights che id è "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" per la risorsa "test" nel gruppo di risorse "testGroup".</span><span class="sxs-lookup"><span data-stu-id="dcb4c-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="dcb4c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcb4c-113">PARAMETERS</span></span>

### <span data-ttu-id="dcb4c-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="dcb4c-114">-ApiKeyId</span></span>
<span data-ttu-id="dcb4c-115">ID chiave API Application Insights.</span><span class="sxs-lookup"><span data-stu-id="dcb4c-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="dcb4c-116">-ApplicationInsightsInsightsIn</span><span class="sxs-lookup"><span data-stu-id="dcb4c-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="dcb4c-117">Oggetto componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="dcb4c-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="dcb4c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcb4c-118">-DefaultProfile</span></span>
<span data-ttu-id="dcb4c-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dcb4c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcb4c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="dcb4c-120">-Name</span></span>
<span data-ttu-id="dcb4c-121">Nome del componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="dcb4c-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="dcb4c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcb4c-122">-PassThru</span></span>
<span data-ttu-id="dcb4c-123">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="dcb4c-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="dcb4c-124">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="dcb4c-124">This parameter is optional.</span></span> <span data-ttu-id="dcb4c-125">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="dcb4c-125">Default value is false.</span></span>

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

### <span data-ttu-id="dcb4c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcb4c-126">-ResourceGroupName</span></span>
<span data-ttu-id="dcb4c-127">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dcb4c-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="dcb4c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcb4c-128">-ResourceId</span></span>
<span data-ttu-id="dcb4c-129">ID risorsa componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="dcb4c-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="dcb4c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcb4c-130">-Confirm</span></span>
<span data-ttu-id="dcb4c-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcb4c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcb4c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcb4c-132">-WhatIf</span></span>
<span data-ttu-id="dcb4c-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dcb4c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcb4c-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dcb4c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcb4c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcb4c-135">CommonParameters</span></span>
<span data-ttu-id="dcb4c-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcb4c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcb4c-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcb4c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcb4c-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="dcb4c-138">INPUTS</span></span>

### <span data-ttu-id="dcb4c-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="dcb4c-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="dcb4c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="dcb4c-140">System.String</span></span>

## <span data-ttu-id="dcb4c-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dcb4c-141">OUTPUTS</span></span>

### <span data-ttu-id="dcb4c-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dcb4c-142">System.Boolean</span></span>

## <span data-ttu-id="dcb4c-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="dcb4c-143">NOTES</span></span>

## <span data-ttu-id="dcb4c-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dcb4c-144">RELATED LINKS</span></span>
