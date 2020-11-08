---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: d5711e6bca9b0579b456e4d2b0c5f915b4ad6fe0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031440"
---
# <span data-ttu-id="f385c-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="f385c-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="f385c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f385c-102">SYNOPSIS</span></span>
<span data-ttu-id="f385c-103">Ottenere informazioni sulla configurazione di un'esportazione continua per un'applicazione Insights Resource</span><span class="sxs-lookup"><span data-stu-id="f385c-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="f385c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f385c-104">SYNTAX</span></span>

### <span data-ttu-id="f385c-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f385c-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f385c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f385c-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f385c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f385c-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f385c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f385c-108">DESCRIPTION</span></span>
<span data-ttu-id="f385c-109">Ottenere informazioni sulla configurazione di un'esportazione continua per un'applicazione Insights Resource</span><span class="sxs-lookup"><span data-stu-id="f385c-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="f385c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f385c-110">EXAMPLES</span></span>

### <span data-ttu-id="f385c-111">Esempio 1 ottenere l'esportazione continua per una risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="f385c-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="f385c-112">Ottenere le informazioni sulle configurazioni di esportazione continue delle applicazioni per le risorse denominate "test" nel gruppo di risorse "testgroup"</span><span class="sxs-lookup"><span data-stu-id="f385c-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="f385c-113">Esempio 2 ottenere l'esportazione continua per una risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="f385c-113">Example 2 Get continuous export for an application insights resource</span></span>
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

<span data-ttu-id="f385c-114">Ottenere la configurazione di esportazione continua dell'applicazione con l'ID esportazione "ZJrfffySPdtG3ESn3iRxVIEFuNY =" per la risorsa denominata "test" nel gruppo risorse "testgroup"</span><span class="sxs-lookup"><span data-stu-id="f385c-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="f385c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f385c-115">PARAMETERS</span></span>

### <span data-ttu-id="f385c-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f385c-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="f385c-117">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="f385c-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="f385c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f385c-118">-DefaultProfile</span></span>
<span data-ttu-id="f385c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f385c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f385c-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="f385c-120">-ExportId</span></span>
<span data-ttu-id="f385c-121">ID dell'esportazione continuo dell'applicazione Insights.</span><span class="sxs-lookup"><span data-stu-id="f385c-121">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="f385c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f385c-122">-Name</span></span>
<span data-ttu-id="f385c-123">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="f385c-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="f385c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f385c-124">-ResourceGroupName</span></span>
<span data-ttu-id="f385c-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f385c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f385c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f385c-126">-ResourceId</span></span>
<span data-ttu-id="f385c-127">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="f385c-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="f385c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f385c-128">CommonParameters</span></span>
<span data-ttu-id="f385c-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f385c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f385c-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f385c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f385c-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f385c-131">INPUTS</span></span>

### <span data-ttu-id="f385c-132">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f385c-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="f385c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f385c-133">System.String</span></span>

## <span data-ttu-id="f385c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f385c-134">OUTPUTS</span></span>

### <span data-ttu-id="f385c-135">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="f385c-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="f385c-136">Note</span><span class="sxs-lookup"><span data-stu-id="f385c-136">NOTES</span></span>

## <span data-ttu-id="f385c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f385c-137">RELATED LINKS</span></span>
