---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 0137a349408234f31f0002849230e023c0544f68
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987081"
---
# <span data-ttu-id="0f482-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="0f482-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="0f482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f482-102">SYNOPSIS</span></span>
<span data-ttu-id="0f482-103">Creare una chiave API Application Insights per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="0f482-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="0f482-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f482-104">SYNTAX</span></span>

### <span data-ttu-id="0f482-105">ComponentNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="0f482-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f482-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f482-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f482-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f482-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f482-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0f482-108">DESCRIPTION</span></span>
<span data-ttu-id="0f482-109">Creare chiavi API di Application Insights per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="0f482-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="0f482-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f482-110">EXAMPLES</span></span>

### <span data-ttu-id="0f482-111">Esempio 1: Creare una nuova chiave API per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="0f482-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="0f482-112">Creare la descrizione della chiave api di Application Insights come "testapiKey" con le autorizzazioni "ReadTelemetry", "WriteAnnotations" per la risorsa "test" nel gruppo di risorse "testGroup".</span><span class="sxs-lookup"><span data-stu-id="0f482-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="0f482-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f482-113">PARAMETERS</span></span>

### <span data-ttu-id="0f482-114">-ApplicationInsightsInsightsIn</span><span class="sxs-lookup"><span data-stu-id="0f482-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="0f482-115">Oggetto componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="0f482-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="0f482-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f482-116">-DefaultProfile</span></span>
<span data-ttu-id="0f482-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f482-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f482-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f482-118">-Description</span></span>
<span data-ttu-id="0f482-119">Descrizione per identificare più facilmente questa chiave API.</span><span class="sxs-lookup"><span data-stu-id="0f482-119">Description to help identify this API key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f482-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0f482-120">-Name</span></span>
<span data-ttu-id="0f482-121">Nome componente.</span><span class="sxs-lookup"><span data-stu-id="0f482-121">Component Name.</span></span>

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

### <span data-ttu-id="0f482-122">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="0f482-122">-Permissions</span></span>
<span data-ttu-id="0f482-123">Autorizzazioni consentite dalla chiave API alle app.</span><span class="sxs-lookup"><span data-stu-id="0f482-123">Permissions that API key allow apps to do.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ReadTelemetry, WriteAnnotations, AuthenticateSDKControlChannel

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f482-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f482-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f482-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0f482-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="0f482-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f482-126">-ResourceId</span></span>
<span data-ttu-id="0f482-127">ID risorsa componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="0f482-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="0f482-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f482-128">-Confirm</span></span>
<span data-ttu-id="0f482-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f482-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f482-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f482-130">-WhatIf</span></span>
<span data-ttu-id="0f482-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f482-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f482-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f482-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f482-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f482-133">CommonParameters</span></span>
<span data-ttu-id="0f482-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f482-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f482-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f482-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f482-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="0f482-136">INPUTS</span></span>

### <span data-ttu-id="0f482-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="0f482-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="0f482-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0f482-138">System.String</span></span>

## <span data-ttu-id="0f482-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f482-139">OUTPUTS</span></span>

### <span data-ttu-id="0f482-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span><span class="sxs-lookup"><span data-stu-id="0f482-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="0f482-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="0f482-141">NOTES</span></span>

## <span data-ttu-id="0f482-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f482-142">RELATED LINKS</span></span>
