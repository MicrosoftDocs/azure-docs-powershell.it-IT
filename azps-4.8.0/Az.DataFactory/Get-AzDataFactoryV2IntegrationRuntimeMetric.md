---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 9b82d302bba1c2f51de3748fb9c335dd0db2699d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190486"
---
# <span data-ttu-id="476df-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="476df-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="476df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="476df-102">SYNOPSIS</span></span>
<span data-ttu-id="476df-103">Ottiene i dati metrici per un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="476df-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="476df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="476df-104">SYNTAX</span></span>

### <span data-ttu-id="476df-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="476df-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="476df-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="476df-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="476df-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="476df-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="476df-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="476df-108">DESCRIPTION</span></span>
<span data-ttu-id="476df-109">Il cmdlet Get-AzDataFactoryV2IntegrationRuntimeMetric ottiene i dati metrici relativi a Integration Runtime in una data factory.</span><span class="sxs-lookup"><span data-stu-id="476df-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="476df-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="476df-110">EXAMPLES</span></span>

### <span data-ttu-id="476df-111">Esempio 1: ottenere la metrica di Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="476df-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="476df-112">Questo comando Visualizza i dati metrici relativi al runtime di integrazione denominato "test-SelfHost-IR" nell'abbonamento per il gruppo di risorse denominato "RG-test-dfv2" e data factory denominato "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="476df-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="476df-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="476df-113">PARAMETERS</span></span>

### <span data-ttu-id="476df-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="476df-114">-DataFactoryName</span></span>
<span data-ttu-id="476df-115">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="476df-115">The data factory name.</span></span>

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

### <span data-ttu-id="476df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="476df-116">-DefaultProfile</span></span>
<span data-ttu-id="476df-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="476df-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="476df-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="476df-118">-InputObject</span></span>
<span data-ttu-id="476df-119">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="476df-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="476df-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="476df-120">-Name</span></span>
<span data-ttu-id="476df-121">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="476df-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="476df-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="476df-122">-ResourceGroupName</span></span>
<span data-ttu-id="476df-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="476df-123">The resource group name.</span></span>

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

### <span data-ttu-id="476df-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="476df-124">-ResourceId</span></span>
<span data-ttu-id="476df-125">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="476df-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="476df-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="476df-126">CommonParameters</span></span>
<span data-ttu-id="476df-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="476df-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="476df-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="476df-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="476df-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="476df-129">INPUTS</span></span>

### <span data-ttu-id="476df-130">System. String</span><span class="sxs-lookup"><span data-stu-id="476df-130">System.String</span></span>

### <span data-ttu-id="476df-131">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="476df-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="476df-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="476df-132">OUTPUTS</span></span>

### <span data-ttu-id="476df-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="476df-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="476df-134">Note</span><span class="sxs-lookup"><span data-stu-id="476df-134">NOTES</span></span>

## <span data-ttu-id="476df-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="476df-135">RELATED LINKS</span></span>

[<span data-ttu-id="476df-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="476df-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()
