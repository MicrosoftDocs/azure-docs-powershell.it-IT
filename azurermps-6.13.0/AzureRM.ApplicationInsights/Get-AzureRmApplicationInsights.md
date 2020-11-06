---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsights.md
ms.openlocfilehash: 917c40d5ec4939e3b6c8b5dc31f68088d4380290
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509396"
---
# <span data-ttu-id="0c62f-101">Get-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="0c62f-101">Get-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="0c62f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c62f-102">SYNOPSIS</span></span>
<span data-ttu-id="0c62f-103">Ottenere le risorse per l'Insight delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="0c62f-103">Get application insights resources</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c62f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c62f-104">SYNTAX</span></span>

### <span data-ttu-id="0c62f-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c62f-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c62f-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c62f-106">ComponentNameParameterSet</span></span>
```
Get-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c62f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c62f-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c62f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c62f-108">DESCRIPTION</span></span>
<span data-ttu-id="0c62f-109">Ottenere le risorse per l'Insight delle applicazioni in un gruppo di risorse o in una risorsa specifica</span><span class="sxs-lookup"><span data-stu-id="0c62f-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="0c62f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c62f-110">EXAMPLES</span></span>

### <span data-ttu-id="0c62f-111">Esempio 1 ottenere la risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="0c62f-111">Example 1 Get application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test"

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

<span data-ttu-id="0c62f-112">Ottenere la risorsa Insights applicazione denominata "test" nel gruppo resoruce "testgroup"</span><span class="sxs-lookup"><span data-stu-id="0c62f-112">Get application insights resource named "test" in resoruce group "testgroup"</span></span>

### <span data-ttu-id="0c62f-113">Esempio 2 ottenere la risorsa approfondimenti applicazione con informazioni sul piano dei prezzi</span><span class="sxs-lookup"><span data-stu-id="0c62f-113">Example 2 Get application insights resource with pricing plan information</span></span>
```
PS C:\> Get-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -IncludePricingPlan

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

<span data-ttu-id="0c62f-114">Ottenere le risorse di Insight per le applicazioni e includere informazioni sul piano dei prezzi per le risorse denominate "test" nel gruppo resoruce "testgroup"</span><span class="sxs-lookup"><span data-stu-id="0c62f-114">Get application insights resource and include pricing plan information for resource named "test" in resoruce group "testgroup"</span></span>

## <span data-ttu-id="0c62f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c62f-115">PARAMETERS</span></span>

### <span data-ttu-id="0c62f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c62f-116">-DefaultProfile</span></span>
<span data-ttu-id="0c62f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c62f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c62f-118">-Full</span><span class="sxs-lookup"><span data-stu-id="0c62f-118">-Full</span></span>
<span data-ttu-id="0c62f-119">Se specificato, verrà restituito il piano prezzi/Cap giornaliero e lo stato del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="0c62f-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

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

### <span data-ttu-id="0c62f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c62f-120">-Name</span></span>
<span data-ttu-id="0c62f-121">Nome risorsa informazioni approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="0c62f-121">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="0c62f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c62f-122">-ResourceGroupName</span></span>
<span data-ttu-id="0c62f-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0c62f-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="0c62f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c62f-124">-ResourceId</span></span>
<span data-ttu-id="0c62f-125">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="0c62f-125">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="0c62f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c62f-126">CommonParameters</span></span>
<span data-ttu-id="0c62f-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c62f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c62f-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c62f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c62f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c62f-129">INPUTS</span></span>

### <span data-ttu-id="0c62f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0c62f-130">System.String</span></span>

## <span data-ttu-id="0c62f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c62f-131">OUTPUTS</span></span>

### <span data-ttu-id="0c62f-132">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0c62f-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="0c62f-133">Note</span><span class="sxs-lookup"><span data-stu-id="0c62f-133">NOTES</span></span>

## <span data-ttu-id="0c62f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c62f-134">RELATED LINKS</span></span>