---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: a3ee8cdaabfc328574497f27a9b35c93992cb03b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515771"
---
# <span data-ttu-id="148aa-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="148aa-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="148aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="148aa-102">SYNOPSIS</span></span>
<span data-ttu-id="148aa-103">Ottiene i dati metrici per un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="148aa-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="148aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="148aa-104">SYNTAX</span></span>

### <span data-ttu-id="148aa-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="148aa-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="148aa-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="148aa-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="148aa-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="148aa-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="148aa-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="148aa-108">DESCRIPTION</span></span>
<span data-ttu-id="148aa-109">Il cmdlet Get-AzureRmDataFactoryV2IntegrationRuntimeMetric ottiene i dati metrici relativi a Integration Runtime in una data factory.</span><span class="sxs-lookup"><span data-stu-id="148aa-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="148aa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="148aa-110">EXAMPLES</span></span>

### <span data-ttu-id="148aa-111">Esempio 1: ottenere la metrica di Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="148aa-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="148aa-112">Questo comando Visualizza i dati metrici relativi al runtime di integrazione denominato "test-SelfHost-IR" nell'abbonamento per il gruppo di risorse denominato "RG-test-dfv2" e data factory denominato "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="148aa-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="148aa-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="148aa-113">PARAMETERS</span></span>

### <span data-ttu-id="148aa-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="148aa-114">-DataFactoryName</span></span>
<span data-ttu-id="148aa-115">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="148aa-115">The data factory name.</span></span>

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

### <span data-ttu-id="148aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="148aa-116">-DefaultProfile</span></span>
<span data-ttu-id="148aa-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="148aa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="148aa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="148aa-118">-InputObject</span></span>
<span data-ttu-id="148aa-119">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="148aa-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="148aa-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="148aa-120">-Name</span></span>
<span data-ttu-id="148aa-121">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="148aa-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="148aa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="148aa-122">-ResourceGroupName</span></span>
<span data-ttu-id="148aa-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="148aa-123">The resource group name.</span></span>

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

### <span data-ttu-id="148aa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="148aa-124">-ResourceId</span></span>
<span data-ttu-id="148aa-125">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="148aa-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="148aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="148aa-126">CommonParameters</span></span>
<span data-ttu-id="148aa-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="148aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="148aa-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="148aa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="148aa-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="148aa-129">INPUTS</span></span>

### <span data-ttu-id="148aa-130">System. String</span><span class="sxs-lookup"><span data-stu-id="148aa-130">System.String</span></span>
<span data-ttu-id="148aa-131">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="148aa-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="148aa-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="148aa-132">OUTPUTS</span></span>

### <span data-ttu-id="148aa-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="148aa-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="148aa-134">Note</span><span class="sxs-lookup"><span data-stu-id="148aa-134">NOTES</span></span>

## <span data-ttu-id="148aa-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="148aa-135">RELATED LINKS</span></span>

[<span data-ttu-id="148aa-136">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="148aa-136">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

