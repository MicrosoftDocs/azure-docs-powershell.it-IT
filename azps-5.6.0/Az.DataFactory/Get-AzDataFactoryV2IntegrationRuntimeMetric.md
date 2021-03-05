---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 12810756f1ebe3e3bf345519d981b660f4c61aa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975246"
---
# <span data-ttu-id="2a49e-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="2a49e-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="2a49e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a49e-102">SYNOPSIS</span></span>
<span data-ttu-id="2a49e-103">Recupera i dati della metrica per un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="2a49e-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="2a49e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a49e-104">SYNTAX</span></span>

### <span data-ttu-id="2a49e-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2a49e-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a49e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a49e-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a49e-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="2a49e-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a49e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2a49e-108">DESCRIPTION</span></span>
<span data-ttu-id="2a49e-109">Il Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet recupera i dati della metrica sul runtime di integrazione in un data factory.</span><span class="sxs-lookup"><span data-stu-id="2a49e-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="2a49e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a49e-110">EXAMPLES</span></span>

### <span data-ttu-id="2a49e-111">Esempio 1: Ottenere la metrica di runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="2a49e-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="2a49e-112">Questo comando visualizza i dati di metrica relativi al runtime di integrazione denominato "test-selfhost-ir" nella sottoscrizione per il gruppo di risorse denominato "rg-test-dfv2" e il data factory denominato "test-df-eu2".</span><span class="sxs-lookup"><span data-stu-id="2a49e-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="2a49e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a49e-113">PARAMETERS</span></span>

### <span data-ttu-id="2a49e-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2a49e-114">-DataFactoryName</span></span>
<span data-ttu-id="2a49e-115">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="2a49e-115">The data factory name.</span></span>

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

### <span data-ttu-id="2a49e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a49e-116">-DefaultProfile</span></span>
<span data-ttu-id="2a49e-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a49e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a49e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a49e-118">-InputObject</span></span>
<span data-ttu-id="2a49e-119">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="2a49e-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="2a49e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2a49e-120">-Name</span></span>
<span data-ttu-id="2a49e-121">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="2a49e-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="2a49e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a49e-122">-ResourceGroupName</span></span>
<span data-ttu-id="2a49e-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2a49e-123">The resource group name.</span></span>

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

### <span data-ttu-id="2a49e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a49e-124">-ResourceId</span></span>
<span data-ttu-id="2a49e-125">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="2a49e-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2a49e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a49e-126">CommonParameters</span></span>
<span data-ttu-id="2a49e-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a49e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a49e-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a49e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a49e-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="2a49e-129">INPUTS</span></span>

### <span data-ttu-id="2a49e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2a49e-130">System.String</span></span>

### <span data-ttu-id="2a49e-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2a49e-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2a49e-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a49e-132">OUTPUTS</span></span>

### <span data-ttu-id="2a49e-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="2a49e-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="2a49e-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="2a49e-134">NOTES</span></span>

## <span data-ttu-id="2a49e-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a49e-135">RELATED LINKS</span></span>

[<span data-ttu-id="2a49e-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2a49e-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

