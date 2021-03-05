---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
ms.openlocfilehash: f208722a065399c12facce6907bbcad3b64d46e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965277"
---
# <span data-ttu-id="11cdb-101">Get-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="11cdb-101">Get-AzApplicationInsights</span></span>

## <span data-ttu-id="11cdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11cdb-102">SYNOPSIS</span></span>
<span data-ttu-id="11cdb-103">Ottenere risorse di Application Insights</span><span class="sxs-lookup"><span data-stu-id="11cdb-103">Get application insights resources</span></span>

## <span data-ttu-id="11cdb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11cdb-104">SYNTAX</span></span>

### <span data-ttu-id="11cdb-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="11cdb-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="11cdb-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="11cdb-106">ComponentNameParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11cdb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11cdb-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11cdb-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="11cdb-108">DESCRIPTION</span></span>
<span data-ttu-id="11cdb-109">Ottenere informazioni dettagliate sull'applicazione in un gruppo di risorse o in una risorsa specifica</span><span class="sxs-lookup"><span data-stu-id="11cdb-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="11cdb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11cdb-110">EXAMPLES</span></span>

### <span data-ttu-id="11cdb-111">Esempio 1: Ottenere informazioni dettagliate sull'applicazione</span><span class="sxs-lookup"><span data-stu-id="11cdb-111">Example 1 Get application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test"

Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
```

<span data-ttu-id="11cdb-112">Ottenere la risorsa Application Insights denominata "test" nel gruppo di risorse "testgroup"</span><span class="sxs-lookup"><span data-stu-id="11cdb-112">Get application insights resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="11cdb-113">Esempio 2: Ottenere informazioni sulla risorsa Application Insights con informazioni sul piano di prezzi</span><span class="sxs-lookup"><span data-stu-id="11cdb-113">Example 2 Get application insights resource with pricing plan information</span></span>
```
PS C:\> Get-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -IncludePricingPlan

Cap                            : 330
ResetTime                      : 0
StopSendNotificationWhenHitCap : True
CapExpirationTime              :
IsCapped                       : False
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
PricingPlan        : Basic
```

<span data-ttu-id="11cdb-114">Ottenere informazioni dettagliate sull'applicazione e includere informazioni sul piano dei prezzi per la risorsa denominata "test" nel gruppo di risorse "gruppo di test"</span><span class="sxs-lookup"><span data-stu-id="11cdb-114">Get application insights resource and include pricing plan information for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="11cdb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11cdb-115">PARAMETERS</span></span>

### <span data-ttu-id="11cdb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11cdb-116">-DefaultProfile</span></span>
<span data-ttu-id="11cdb-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11cdb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11cdb-118">-Full</span><span class="sxs-lookup"><span data-stu-id="11cdb-118">-Full</span></span>
<span data-ttu-id="11cdb-119">Se specificato, il piano per la tornata dei prezzi/ il limite giornaliero e lo stato del componente Application Insights verranno tornati.</span><span class="sxs-lookup"><span data-stu-id="11cdb-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ComponentNameParameterSet, ResourceIdParameterSet
Aliases: IncludeDailyCap, IncludeDailyCapStatus, IncludePricingPlan

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11cdb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="11cdb-120">-Name</span></span>
<span data-ttu-id="11cdb-121">Nome della risorsa Application Insights.</span><span class="sxs-lookup"><span data-stu-id="11cdb-121">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="11cdb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11cdb-122">-ResourceGroupName</span></span>
<span data-ttu-id="11cdb-123">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="11cdb-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="11cdb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11cdb-124">-ResourceId</span></span>
<span data-ttu-id="11cdb-125">ID risorsa componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="11cdb-125">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="11cdb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11cdb-126">CommonParameters</span></span>
<span data-ttu-id="11cdb-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11cdb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11cdb-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="11cdb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11cdb-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="11cdb-129">INPUTS</span></span>

### <span data-ttu-id="11cdb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="11cdb-130">System.String</span></span>

## <span data-ttu-id="11cdb-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11cdb-131">OUTPUTS</span></span>

### <span data-ttu-id="11cdb-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="11cdb-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="11cdb-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="11cdb-133">NOTES</span></span>

## <span data-ttu-id="11cdb-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11cdb-134">RELATED LINKS</span></span>
