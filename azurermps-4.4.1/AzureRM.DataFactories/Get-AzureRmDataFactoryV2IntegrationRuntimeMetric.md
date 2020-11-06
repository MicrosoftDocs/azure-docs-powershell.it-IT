---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: aba54b47a5d335bb4f6ef1fbbf7bef66fa694aaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510719"
---
# <span data-ttu-id="319f0-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="319f0-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="319f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="319f0-102">SYNOPSIS</span></span>
<span data-ttu-id="319f0-103">Ottiene i dati metrici per un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="319f0-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="319f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="319f0-104">SYNTAX</span></span>

### <span data-ttu-id="319f0-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="319f0-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="319f0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="319f0-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="319f0-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="319f0-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="319f0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="319f0-108">DESCRIPTION</span></span>
<span data-ttu-id="319f0-109">Il cmdlet Get-AzureRmDataFactoryV2IntegrationRuntimeMetric ottiene i dati metrici relativi a Integration Runtime in una data factory.</span><span class="sxs-lookup"><span data-stu-id="319f0-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="319f0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="319f0-110">EXAMPLES</span></span>

### <span data-ttu-id="319f0-111">Esempio 1: ottenere la metrica di Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="319f0-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="319f0-112">Questo comando Visualizza i dati metrici relativi al runtime di integrazione denominato "test-SelfHost-IR" nell'abbonamento per il gruppo di risorse denominato "RG-test-dfv2" e data factory denominato "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="319f0-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="319f0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="319f0-113">PARAMETERS</span></span>

### <span data-ttu-id="319f0-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="319f0-114">-DataFactoryName</span></span>
<span data-ttu-id="319f0-115">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="319f0-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319f0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="319f0-116">-InputObject</span></span>
<span data-ttu-id="319f0-117">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="319f0-117">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="319f0-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="319f0-118">-Name</span></span>
<span data-ttu-id="319f0-119">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="319f0-119">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319f0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="319f0-120">-ResourceGroupName</span></span>
<span data-ttu-id="319f0-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="319f0-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319f0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="319f0-122">-ResourceId</span></span>
<span data-ttu-id="319f0-123">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="319f0-123">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319f0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="319f0-124">-DefaultProfile</span></span>
<span data-ttu-id="319f0-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="319f0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="319f0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="319f0-126">CommonParameters</span></span>
<span data-ttu-id="319f0-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="319f0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="319f0-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="319f0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="319f0-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="319f0-129">INPUTS</span></span>

### <span data-ttu-id="319f0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="319f0-130">System.String</span></span>
<span data-ttu-id="319f0-131">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="319f0-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="319f0-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="319f0-132">OUTPUTS</span></span>

### <span data-ttu-id="319f0-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="319f0-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="319f0-134">Note</span><span class="sxs-lookup"><span data-stu-id="319f0-134">NOTES</span></span>

## <span data-ttu-id="319f0-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="319f0-135">RELATED LINKS</span></span>

[<span data-ttu-id="319f0-136">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="319f0-136">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

