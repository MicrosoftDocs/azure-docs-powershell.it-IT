---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: 944c029b4085316225887b821c4f6c8f52e7f92b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176343"
---
# <span data-ttu-id="bd6c9-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="bd6c9-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="bd6c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd6c9-102">SYNOPSIS</span></span>
<span data-ttu-id="bd6c9-103">Ottenere consigli aggregati sulla sicurezza IoT</span><span class="sxs-lookup"><span data-stu-id="bd6c9-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="bd6c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd6c9-104">SYNTAX</span></span>

### <span data-ttu-id="bd6c9-105">SolutionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bd6c9-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd6c9-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="bd6c9-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd6c9-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bd6c9-107">DESCRIPTION</span></span>
<span data-ttu-id="bd6c9-108">Il Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet restituisce uno o più consigli aggregati nei dispositivi dell'hub iot.</span><span class="sxs-lookup"><span data-stu-id="bd6c9-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="bd6c9-109">Il nome di un suggerimento aggregato è il relativo tipo</span><span class="sxs-lookup"><span data-stu-id="bd6c9-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="bd6c9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd6c9-110">EXAMPLES</span></span>

### <span data-ttu-id="bd6c9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bd6c9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name IoT_OpenPorts

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedRecommendations/IoT_OpenPorts"
Name: "IoT_OpenPorts"
Type: "Microsoft.Security/IoTSecurityAggregatedRecommendation"
RecommendationName: "IoT_OpenPorts"
RecommendationDisplayName: "Device has open ports"
RecommendationTypeId: ""
DetectedBy: "IoTSecurity"
HealthyDevices: -1
UnhealthyDeviceCount: 5
RemediationSteps: "Review open ports on the device and make sure they belong to legitimate and necessary processes for the device to function correctly."
ReportedSeverity: "Medium"
Description: "Found a listening endpoint on the device."
LogAnalyticsQuery: "SecurityRecommendation | where tolower(AssessedResourceId) == tolower('/subscriptions/075423e9-7d33-4166-8bdf-3920b04e3735/resourcegroups/iot-hub-demo/providers/microsoft.devices/iothubs/ascforiot-demo') and tolower(RecommendationName) == tolower('IoT_OpenPorts') and TimeGenerated  < now()"
```

<span data-ttu-id="bd6c9-112">Ottenere il suggerimento aggregato "IoT_OpenPorts" nella soluzione di sicurezza "MySolution" e nel gruppo di risorse "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="bd6c9-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="bd6c9-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bd6c9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="bd6c9-114">Ottenere un elenco di suggerimenti aggregati nella soluzione di sicurezza "MySolution" e nel gruppo di risorse "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="bd6c9-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="bd6c9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd6c9-115">PARAMETERS</span></span>

### <span data-ttu-id="bd6c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd6c9-116">-DefaultProfile</span></span>
<span data-ttu-id="bd6c9-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd6c9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd6c9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bd6c9-118">-Name</span></span>
<span data-ttu-id="bd6c9-119">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bd6c9-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6c9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd6c9-120">-ResourceGroupName</span></span>
<span data-ttu-id="bd6c9-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bd6c9-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6c9-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="bd6c9-122">-SolutionName</span></span>
<span data-ttu-id="bd6c9-123">Nome della soluzione</span><span class="sxs-lookup"><span data-stu-id="bd6c9-123">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6c9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd6c9-124">CommonParameters</span></span>
<span data-ttu-id="bd6c9-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd6c9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd6c9-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bd6c9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd6c9-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="bd6c9-127">INPUTS</span></span>

### <span data-ttu-id="bd6c9-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bd6c9-128">None</span></span>

## <span data-ttu-id="bd6c9-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd6c9-129">OUTPUTS</span></span>

### <span data-ttu-id="bd6c9-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="bd6c9-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="bd6c9-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="bd6c9-131">NOTES</span></span>

## <span data-ttu-id="bd6c9-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd6c9-132">RELATED LINKS</span></span>
