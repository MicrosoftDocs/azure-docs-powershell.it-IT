---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 2afb8ebfa1305e736a226f48022f4c56ded2d809
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182278"
---
# <span data-ttu-id="4fe33-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="4fe33-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="4fe33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fe33-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe33-103">Creare una chiave API di Application Insights per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="4fe33-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="4fe33-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4fe33-104">SYNTAX</span></span>

### <span data-ttu-id="4fe33-105">ComponentNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4fe33-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fe33-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fe33-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fe33-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fe33-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fe33-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4fe33-108">DESCRIPTION</span></span>
<span data-ttu-id="4fe33-109">Creare chiavi API di Application Insights per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="4fe33-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="4fe33-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4fe33-110">EXAMPLES</span></span>

### <span data-ttu-id="4fe33-111">Esempio 1: Creare una nuova chiave API per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="4fe33-111">Example 1 Create a new Api Key for an application insights resource</span></span>
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

<span data-ttu-id="4fe33-112">Creare la descrizione della chiave api di Application Insights come "testapiKey" con le autorizzazioni "ReadTelemetry", "WriteAnnotations" per la risorsa "test" nel gruppo di risorse "testGroup".</span><span class="sxs-lookup"><span data-stu-id="4fe33-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="4fe33-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fe33-113">PARAMETERS</span></span>

### <span data-ttu-id="4fe33-114">-ApplicationInsightsInsightsIn</span><span class="sxs-lookup"><span data-stu-id="4fe33-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="4fe33-115">Oggetto componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="4fe33-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="4fe33-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fe33-116">-DefaultProfile</span></span>
<span data-ttu-id="4fe33-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4fe33-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fe33-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fe33-118">-Description</span></span>
<span data-ttu-id="4fe33-119">Descrizione per identificare più facilmente questa chiave API.</span><span class="sxs-lookup"><span data-stu-id="4fe33-119">Description to help identify this API key.</span></span>

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

### <span data-ttu-id="4fe33-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4fe33-120">-Name</span></span>
<span data-ttu-id="4fe33-121">Nome componente.</span><span class="sxs-lookup"><span data-stu-id="4fe33-121">Component Name.</span></span>

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

### <span data-ttu-id="4fe33-122">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="4fe33-122">-Permissions</span></span>
<span data-ttu-id="4fe33-123">Autorizzazioni consentite dalla chiave API alle app.</span><span class="sxs-lookup"><span data-stu-id="4fe33-123">Permissions that API key allow apps to do.</span></span>

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

### <span data-ttu-id="4fe33-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fe33-124">-ResourceGroupName</span></span>
<span data-ttu-id="4fe33-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4fe33-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="4fe33-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fe33-126">-ResourceId</span></span>
<span data-ttu-id="4fe33-127">ID risorsa componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="4fe33-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="4fe33-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fe33-128">-Confirm</span></span>
<span data-ttu-id="4fe33-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fe33-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fe33-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fe33-130">-WhatIf</span></span>
<span data-ttu-id="4fe33-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4fe33-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fe33-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4fe33-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fe33-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe33-133">CommonParameters</span></span>
<span data-ttu-id="4fe33-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fe33-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe33-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fe33-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe33-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="4fe33-136">INPUTS</span></span>

### <span data-ttu-id="4fe33-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="4fe33-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="4fe33-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4fe33-138">System.String</span></span>

## <span data-ttu-id="4fe33-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4fe33-139">OUTPUTS</span></span>

### <span data-ttu-id="4fe33-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span><span class="sxs-lookup"><span data-stu-id="4fe33-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="4fe33-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="4fe33-141">NOTES</span></span>

## <span data-ttu-id="4fe33-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4fe33-142">RELATED LINKS</span></span>
