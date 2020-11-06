---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: cb5de7f8e0e484c5b9080e3a50871cddca5af173
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517664"
---
# <span data-ttu-id="57cd8-101">Get-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="57cd8-101">Get-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="57cd8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="57cd8-103">Ottenere informazioni sulla configurazione di un'esportazione continua per un'applicazione Insights Resource</span><span class="sxs-lookup"><span data-stu-id="57cd8-103">Get application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57cd8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57cd8-104">SYNTAX</span></span>

### <span data-ttu-id="57cd8-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="57cd8-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57cd8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57cd8-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57cd8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57cd8-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57cd8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57cd8-108">DESCRIPTION</span></span>
<span data-ttu-id="57cd8-109">Ottenere informazioni sulla configurazione di un'esportazione continua per un'applicazione Insights Resource</span><span class="sxs-lookup"><span data-stu-id="57cd8-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="57cd8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57cd8-110">EXAMPLES</span></span>

### <span data-ttu-id="57cd8-111">Esempio 1 ottenere l'esportazione continua per una risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="57cd8-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="57cd8-112">Ottenere le informazioni sulle configurazioni di esportazione continue delle applicazioni per le risorse denominate "test" nel gruppo di risorse "testgroup"</span><span class="sxs-lookup"><span data-stu-id="57cd8-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="57cd8-113">Esempio 2 ottenere l'esportazione continua per una risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="57cd8-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

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

<span data-ttu-id="57cd8-114">Ottenere la configurazione di esportazione continua dell'applicazione con l'ID esportazione "ZJrfffySPdtG3ESn3iRxVIEFuNY =" per la risorsa denominata "test" nel gruppo risorse "testgroup"</span><span class="sxs-lookup"><span data-stu-id="57cd8-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="57cd8-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57cd8-115">PARAMETERS</span></span>

### <span data-ttu-id="57cd8-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="57cd8-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="57cd8-117">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="57cd8-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="57cd8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57cd8-118">-DefaultProfile</span></span>
<span data-ttu-id="57cd8-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57cd8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57cd8-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="57cd8-120">-ExportId</span></span>
<span data-ttu-id="57cd8-121">ID dell'esportazione continuo dell'applicazione Insights.</span><span class="sxs-lookup"><span data-stu-id="57cd8-121">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="57cd8-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="57cd8-122">-Name</span></span>
<span data-ttu-id="57cd8-123">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="57cd8-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="57cd8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57cd8-124">-ResourceGroupName</span></span>
<span data-ttu-id="57cd8-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="57cd8-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="57cd8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57cd8-126">-ResourceId</span></span>
<span data-ttu-id="57cd8-127">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="57cd8-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="57cd8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57cd8-128">CommonParameters</span></span>
<span data-ttu-id="57cd8-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57cd8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57cd8-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57cd8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57cd8-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57cd8-131">INPUTS</span></span>

### <span data-ttu-id="57cd8-132">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="57cd8-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="57cd8-133">Parametri: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="57cd8-133">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="57cd8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="57cd8-134">System.String</span></span>

## <span data-ttu-id="57cd8-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57cd8-135">OUTPUTS</span></span>

### <span data-ttu-id="57cd8-136">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="57cd8-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="57cd8-137">Note</span><span class="sxs-lookup"><span data-stu-id="57cd8-137">NOTES</span></span>

## <span data-ttu-id="57cd8-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57cd8-138">RELATED LINKS</span></span>
