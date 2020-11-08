---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 3faa93ced76fee1a1023011e1570c3819f6c2013
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031436"
---
# <span data-ttu-id="e28d6-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e28d6-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="e28d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e28d6-102">SYNOPSIS</span></span>
<span data-ttu-id="e28d6-103">Creare una nuova risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="e28d6-103">Create a new application insights resource</span></span>

## <span data-ttu-id="e28d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e28d6-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e28d6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e28d6-105">DESCRIPTION</span></span>
<span data-ttu-id="e28d6-106">Creare una nuova risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="e28d6-106">Create a new application insights resource</span></span>

## <span data-ttu-id="e28d6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e28d6-107">EXAMPLES</span></span>

### <span data-ttu-id="e28d6-108">Esempio 1 creare una nuova risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="e28d6-108">Example 1 Create a new application insights resource</span></span>
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

<span data-ttu-id="e28d6-109">Aggiungere una nuova risorsa approfondimenti applicazione denominata "test" nel gruppo risorse "testgroup" con il tipo "Java"</span><span class="sxs-lookup"><span data-stu-id="e28d6-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java"</span></span>

## <span data-ttu-id="e28d6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e28d6-110">PARAMETERS</span></span>

### <span data-ttu-id="e28d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e28d6-111">-DefaultProfile</span></span>
<span data-ttu-id="e28d6-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e28d6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e28d6-113">-Tipo</span><span class="sxs-lookup"><span data-stu-id="e28d6-113">-Kind</span></span>
<span data-ttu-id="e28d6-114">Tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="e28d6-114">Application kind.</span></span>

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

### <span data-ttu-id="e28d6-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e28d6-115">-Location</span></span>
<span data-ttu-id="e28d6-116">Percorso delle risorse dell'applicazione Insights.</span><span class="sxs-lookup"><span data-stu-id="e28d6-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="e28d6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e28d6-117">-Name</span></span>
<span data-ttu-id="e28d6-118">Nome risorsa informazioni approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="e28d6-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="e28d6-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="e28d6-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="e28d6-120">Tipo di accesso alla rete per l'accesso all'ingestione di Insight per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e28d6-120">The network access type for accessing Application Insights ingestion.</span></span> <span data-ttu-id="e28d6-121">Il valore deve essere "Enabled" o "disabled"</span><span class="sxs-lookup"><span data-stu-id="e28d6-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="e28d6-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="e28d6-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="e28d6-123">Tipo di accesso alla rete per l'accesso alla query Insights dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e28d6-123">The network access type for accessing Application Insights query.</span></span> <span data-ttu-id="e28d6-124">Il valore deve essere "Enabled" o "disabled"</span><span class="sxs-lookup"><span data-stu-id="e28d6-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="e28d6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e28d6-125">-ResourceGroupName</span></span>
<span data-ttu-id="e28d6-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e28d6-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="e28d6-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e28d6-127">-RetentionInDays</span></span>
<span data-ttu-id="e28d6-128">Conservazione in giorni, 90 per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e28d6-128">Retention In Days, 90 by default.</span></span>

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

### <span data-ttu-id="e28d6-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="e28d6-129">-Tag</span></span>
<span data-ttu-id="e28d6-130">Tag del componente.</span><span class="sxs-lookup"><span data-stu-id="e28d6-130">Component Tags.</span></span>

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

### <span data-ttu-id="e28d6-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e28d6-131">-Confirm</span></span>
<span data-ttu-id="e28d6-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e28d6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e28d6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e28d6-133">-WhatIf</span></span>
<span data-ttu-id="e28d6-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e28d6-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e28d6-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e28d6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e28d6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e28d6-136">CommonParameters</span></span>
<span data-ttu-id="e28d6-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e28d6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e28d6-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e28d6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e28d6-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e28d6-139">INPUTS</span></span>

### <span data-ttu-id="e28d6-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e28d6-140">None</span></span>

## <span data-ttu-id="e28d6-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e28d6-141">OUTPUTS</span></span>

### <span data-ttu-id="e28d6-142">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e28d6-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="e28d6-143">Note</span><span class="sxs-lookup"><span data-stu-id="e28d6-143">NOTES</span></span>

## <span data-ttu-id="e28d6-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e28d6-144">RELATED LINKS</span></span>
