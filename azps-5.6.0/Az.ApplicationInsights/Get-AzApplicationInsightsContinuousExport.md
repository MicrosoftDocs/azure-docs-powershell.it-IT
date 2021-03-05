---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 63c31e07313f7e6ad3e1eea25977e85f3e4c6b53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965245"
---
# <span data-ttu-id="a949b-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="a949b-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="a949b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a949b-102">SYNOPSIS</span></span>
<span data-ttu-id="a949b-103">Ottenere informazioni dettagliate sull'applicazione per la configurazione continua dell'esportazione per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="a949b-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="a949b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a949b-104">SYNTAX</span></span>

### <span data-ttu-id="a949b-105">ComponentNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="a949b-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a949b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a949b-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a949b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a949b-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a949b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a949b-108">DESCRIPTION</span></span>
<span data-ttu-id="a949b-109">Ottenere informazioni dettagliate sull'applicazione per la configurazione continua dell'esportazione per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="a949b-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="a949b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a949b-110">EXAMPLES</span></span>

### <span data-ttu-id="a949b-111">Esempio 1 Ottenere l'esportazione continua per una risorsa application Insights</span><span class="sxs-lookup"><span data-stu-id="a949b-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="a949b-112">Ottenere informazioni dettagliate sull'applicazione per le configurazioni di esportazione continue per la risorsa denominata "test" nel gruppo di risorse "gruppo di test"</span><span class="sxs-lookup"><span data-stu-id="a949b-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="a949b-113">Esempio 2: Ottenere l'esportazione continua per una risorsa application Insights</span><span class="sxs-lookup"><span data-stu-id="a949b-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

ExportId                         : ZJrfffySPdtG3ESn3iRxVIEFuNY=
StorageName                      : targetaccount
ContainerName                    : continuousexport
DocumentTypes                    : Request, Performance Counter
DestinationStorageSubscriptionId : {subid}
DestinationStorageLocationId     : eastus
DestinationStorageAccountId      : /subscriptions/{subid}/resourceGroups/targetstorage/providers/Microsoft.Storage/storageAccounts/targetaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="a949b-114">Ottenere informazioni dettagliate sull'applicazione per la configurazione continua dell'esportazione con ID esportazione "ZJrfffySPdtG3ESn3iRxVIEFuNY=" per la risorsa denominata "test" nel gruppo di risorse "gruppo di test"</span><span class="sxs-lookup"><span data-stu-id="a949b-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="a949b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a949b-115">PARAMETERS</span></span>

### <span data-ttu-id="a949b-116">-ApplicationInsightsInsightsIn</span><span class="sxs-lookup"><span data-stu-id="a949b-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="a949b-117">Oggetto componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="a949b-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="a949b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a949b-118">-DefaultProfile</span></span>
<span data-ttu-id="a949b-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a949b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a949b-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="a949b-120">-ExportId</span></span>
<span data-ttu-id="a949b-121">ID di esportazione continua di Application Insights.</span><span class="sxs-lookup"><span data-stu-id="a949b-121">Application Insights Continuous Export Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a949b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a949b-122">-Name</span></span>
<span data-ttu-id="a949b-123">Nome del componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="a949b-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="a949b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a949b-124">-ResourceGroupName</span></span>
<span data-ttu-id="a949b-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a949b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a949b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a949b-126">-ResourceId</span></span>
<span data-ttu-id="a949b-127">ID risorsa componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="a949b-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="a949b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a949b-128">CommonParameters</span></span>
<span data-ttu-id="a949b-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a949b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a949b-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a949b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a949b-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="a949b-131">INPUTS</span></span>

### <span data-ttu-id="a949b-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="a949b-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="a949b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a949b-133">System.String</span></span>

## <span data-ttu-id="a949b-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a949b-134">OUTPUTS</span></span>

### <span data-ttu-id="a949b-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="a949b-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="a949b-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="a949b-136">NOTES</span></span>

## <span data-ttu-id="a949b-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a949b-137">RELATED LINKS</span></span>
