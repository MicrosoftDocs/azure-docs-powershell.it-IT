---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: db0ad78a942905846f764bb5d72a8ef3b209b6a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957790"
---
# <span data-ttu-id="6dab0-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6dab0-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="6dab0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dab0-102">SYNOPSIS</span></span>
<span data-ttu-id="6dab0-103">Creare una nuova risorsa Application Insights</span><span class="sxs-lookup"><span data-stu-id="6dab0-103">Create a new application insights resource</span></span>

## <span data-ttu-id="6dab0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6dab0-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6dab0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6dab0-105">DESCRIPTION</span></span>
<span data-ttu-id="6dab0-106">Creare una nuova risorsa Application Insights</span><span class="sxs-lookup"><span data-stu-id="6dab0-106">Create a new application insights resource</span></span>

## <span data-ttu-id="6dab0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6dab0-107">EXAMPLES</span></span>

### <span data-ttu-id="6dab0-108">Esempio 1: Creare una nuova risorsa application Insights</span><span class="sxs-lookup"><span data-stu-id="6dab0-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test1027
ResourceGroupName  : testgroup
Name               : test1027
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 8323fb13-32aa-46af-b467-8355cf4f8f98
ApplicationType    : web
Tags               : {}
CreationDate       : 10/27/2017 4:56:40 PM
FlowType           :
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 083112ed-ed9b-464e-a9b0-8cf126fbfced
ProvisioningState  : Succeeded
RequestSource      : AzurePowerShell
SamplingPercentage :
TenantId           : {subid}
PublicNetworkAccessForIngestion : Enabled
PublicNetworkAccessForQuery     : Enabled
PrivateLinkScopedResources      :
```

<span data-ttu-id="6dab0-109">Aggiungere una nuova risorsa Application Insights denominata "test" nel gruppo di risorse "testgroup" con il tipo "java"</span><span class="sxs-lookup"><span data-stu-id="6dab0-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java"</span></span>

## <span data-ttu-id="6dab0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6dab0-110">PARAMETERS</span></span>

### <span data-ttu-id="6dab0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dab0-111">-DefaultProfile</span></span>
<span data-ttu-id="6dab0-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6dab0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dab0-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="6dab0-113">-Kind</span></span>
<span data-ttu-id="6dab0-114">Tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="6dab0-114">Application kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dab0-115">-Location</span><span class="sxs-lookup"><span data-stu-id="6dab0-115">-Location</span></span>
<span data-ttu-id="6dab0-116">Posizione delle risorse di Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6dab0-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="6dab0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6dab0-117">-Name</span></span>
<span data-ttu-id="6dab0-118">Nome della risorsa Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6dab0-118">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dab0-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="6dab0-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="6dab0-120">Tipo di accesso di rete per l'accesso all'inserimento di Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6dab0-120">The network access type for accessing Application Insights ingestion.</span></span> <span data-ttu-id="6dab0-121">Il valore deve essere "Abilitato" o "Disabilitato"</span><span class="sxs-lookup"><span data-stu-id="6dab0-121">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dab0-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="6dab0-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="6dab0-123">Tipo di accesso di rete per accedere alla query di Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6dab0-123">The network access type for accessing Application Insights query.</span></span> <span data-ttu-id="6dab0-124">Il valore deve essere "Abilitato" o "Disabilitato"</span><span class="sxs-lookup"><span data-stu-id="6dab0-124">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dab0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dab0-125">-ResourceGroupName</span></span>
<span data-ttu-id="6dab0-126">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6dab0-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dab0-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="6dab0-127">-RetentionInDays</span></span>
<span data-ttu-id="6dab0-128">Conservazione in giorni, 90 per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="6dab0-128">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dab0-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="6dab0-129">-Tag</span></span>
<span data-ttu-id="6dab0-130">Contrassegni componenti.</span><span class="sxs-lookup"><span data-stu-id="6dab0-130">Component Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dab0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6dab0-131">-Confirm</span></span>
<span data-ttu-id="6dab0-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dab0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dab0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dab0-133">-WhatIf</span></span>
<span data-ttu-id="6dab0-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6dab0-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6dab0-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6dab0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dab0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dab0-136">CommonParameters</span></span>
<span data-ttu-id="6dab0-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dab0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dab0-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6dab0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dab0-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="6dab0-139">INPUTS</span></span>

### <span data-ttu-id="6dab0-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6dab0-140">None</span></span>

## <span data-ttu-id="6dab0-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6dab0-141">OUTPUTS</span></span>

### <span data-ttu-id="6dab0-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="6dab0-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="6dab0-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="6dab0-143">NOTES</span></span>

## <span data-ttu-id="6dab0-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6dab0-144">RELATED LINKS</span></span>
