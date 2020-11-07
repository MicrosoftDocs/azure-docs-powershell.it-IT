---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8912717f718bff7c669752e5e49c2796ee94b05b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688656"
---
# <span data-ttu-id="09ff8-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="09ff8-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="09ff8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="09ff8-103">Ottiene i dati metrici per un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="09ff8-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09ff8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09ff8-104">SYNTAX</span></span>

### <span data-ttu-id="09ff8-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="09ff8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="09ff8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="09ff8-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
```

### <span data-ttu-id="09ff8-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="09ff8-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="09ff8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09ff8-108">DESCRIPTION</span></span>
<span data-ttu-id="09ff8-109">Il cmdlet Get-AzureRmDataFactoryV2IntegrationRuntimeMetric ottiene i dati metrici relativi a Integration Runtime in una data factory.</span><span class="sxs-lookup"><span data-stu-id="09ff8-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="09ff8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09ff8-110">EXAMPLES</span></span>

### <span data-ttu-id="09ff8-111">Esempio 1: ottenere la metrica di Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="09ff8-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="09ff8-112">Questo comando Visualizza i dati metrici relativi al runtime di integrazione denominato "test-SelfHost-IR" nell'abbonamento per il gruppo di risorse denominato "RG-test-dfv2" e data factory denominato "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="09ff8-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="09ff8-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09ff8-113">PARAMETERS</span></span>

### <span data-ttu-id="09ff8-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="09ff8-114">-DataFactoryName</span></span>
<span data-ttu-id="09ff8-115">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="09ff8-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09ff8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09ff8-116">-InputObject</span></span>
<span data-ttu-id="09ff8-117">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="09ff8-117">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09ff8-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="09ff8-118">-Name</span></span>
<span data-ttu-id="09ff8-119">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="09ff8-119">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09ff8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09ff8-120">-ResourceGroupName</span></span>
<span data-ttu-id="09ff8-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="09ff8-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09ff8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09ff8-122">-ResourceId</span></span>
<span data-ttu-id="09ff8-123">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="09ff8-123">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="09ff8-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09ff8-124">INPUTS</span></span>

### <span data-ttu-id="09ff8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="09ff8-125">System.String</span></span>
<span data-ttu-id="09ff8-126">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="09ff8-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="09ff8-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09ff8-127">OUTPUTS</span></span>

### <span data-ttu-id="09ff8-128">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="09ff8-128">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>


## <span data-ttu-id="09ff8-129">Note</span><span class="sxs-lookup"><span data-stu-id="09ff8-129">NOTES</span></span>

## <span data-ttu-id="09ff8-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09ff8-130">RELATED LINKS</span></span>
[<span data-ttu-id="09ff8-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="09ff8-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

