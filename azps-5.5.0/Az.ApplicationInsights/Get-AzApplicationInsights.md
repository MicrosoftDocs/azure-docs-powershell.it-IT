---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
ms.openlocfilehash: 943089433ca7007ef81648846a48ebdd5684bab2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195310"
---
# <span data-ttu-id="3c68c-101">Get-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="3c68c-101">Get-AzApplicationInsights</span></span>

## <span data-ttu-id="3c68c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c68c-102">SYNOPSIS</span></span>
<span data-ttu-id="3c68c-103">Ottenere informazioni dettagliate sull'applicazione</span><span class="sxs-lookup"><span data-stu-id="3c68c-103">Get application insights resources</span></span>

## <span data-ttu-id="3c68c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c68c-104">SYNTAX</span></span>

### <span data-ttu-id="3c68c-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3c68c-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c68c-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c68c-106">ComponentNameParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c68c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c68c-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c68c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3c68c-108">DESCRIPTION</span></span>
<span data-ttu-id="3c68c-109">Ottenere informazioni dettagliate sull'applicazione in un gruppo di risorse o in una risorsa specifica</span><span class="sxs-lookup"><span data-stu-id="3c68c-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="3c68c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c68c-110">EXAMPLES</span></span>

### <span data-ttu-id="3c68c-111">Esempio 1: Ottenere informazioni dettagliate sull'applicazione</span><span class="sxs-lookup"><span data-stu-id="3c68c-111">Example 1 Get application insights resource</span></span>
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

<span data-ttu-id="3c68c-112">Ottenere la risorsa Application Insights denominata "test" nel gruppo di risorse "testgroup"</span><span class="sxs-lookup"><span data-stu-id="3c68c-112">Get application insights resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="3c68c-113">Esempio 2: Ottenere informazioni sulla risorsa Application Insights con informazioni sul piano di prezzi</span><span class="sxs-lookup"><span data-stu-id="3c68c-113">Example 2 Get application insights resource with pricing plan information</span></span>
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

<span data-ttu-id="3c68c-114">Ottenere informazioni dettagliate sull'applicazione e includere informazioni sul piano dei prezzi per la risorsa denominata "test" nel gruppo di risorse "gruppo di test"</span><span class="sxs-lookup"><span data-stu-id="3c68c-114">Get application insights resource and include pricing plan information for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="3c68c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c68c-115">PARAMETERS</span></span>

### <span data-ttu-id="3c68c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c68c-116">-DefaultProfile</span></span>
<span data-ttu-id="3c68c-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c68c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c68c-118">-Full</span><span class="sxs-lookup"><span data-stu-id="3c68c-118">-Full</span></span>
<span data-ttu-id="3c68c-119">Se specificato, il piano per la tornata dei prezzi/ il limite giornaliero e lo stato del componente Application Insights verranno reperti.</span><span class="sxs-lookup"><span data-stu-id="3c68c-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

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

### <span data-ttu-id="3c68c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3c68c-120">-Name</span></span>
<span data-ttu-id="3c68c-121">Nome della risorsa Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3c68c-121">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="3c68c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c68c-122">-ResourceGroupName</span></span>
<span data-ttu-id="3c68c-123">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3c68c-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="3c68c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c68c-124">-ResourceId</span></span>
<span data-ttu-id="3c68c-125">ID risorsa componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3c68c-125">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="3c68c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c68c-126">CommonParameters</span></span>
<span data-ttu-id="3c68c-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c68c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c68c-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3c68c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c68c-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="3c68c-129">INPUTS</span></span>

### <span data-ttu-id="3c68c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3c68c-130">System.String</span></span>

## <span data-ttu-id="3c68c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c68c-131">OUTPUTS</span></span>

### <span data-ttu-id="3c68c-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="3c68c-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="3c68c-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="3c68c-133">NOTES</span></span>

## <span data-ttu-id="3c68c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c68c-134">RELATED LINKS</span></span>
