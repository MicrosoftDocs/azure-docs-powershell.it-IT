---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 2b5f01047bf0b86fc885a01f0c58a9ab094f7698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688647"
---
# <span data-ttu-id="1985a-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1985a-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="1985a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1985a-102">SYNOPSIS</span></span>
<span data-ttu-id="1985a-103">Avvia un runtime di integrazione dedicata gestito.</span><span class="sxs-lookup"><span data-stu-id="1985a-103">Starts a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1985a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1985a-104">SYNTAX</span></span>

### <span data-ttu-id="1985a-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1985a-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1985a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1985a-106">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1985a-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="1985a-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="1985a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1985a-108">DESCRIPTION</span></span>
<span data-ttu-id="1985a-109">Il cmdlet **Start-AzureRmDataFactoryV2IntegrationRuntime** avvia un runtime di Integration dedicato gestito.</span><span class="sxs-lookup"><span data-stu-id="1985a-109">The **Start-AzureRmDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="1985a-110">La risorsa viene provisionata e dopo l'operazione lo stato è "iniziato".</span><span class="sxs-lookup"><span data-stu-id="1985a-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="1985a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1985a-111">EXAMPLES</span></span>

### <span data-ttu-id="1985a-112">Esempio 1: avviare un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="1985a-112">Example 1: Start an integration runtime</span></span>
```
PS C:\> Start-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name test-dedicated-ir' -Force

    CreateTime                   : 9/11/2017 2:16:12 PM
    Nodes                        : {tvm-1650185656_1-20170911t141751z}
    OtherErrors                  : {}
    LastOperation                : 
    State                        : Started
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : testsvr.database.windows.net
    CatalogAdminUserName         : admin
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="1985a-113">Questo cmdlet avvia un runtime di integrazione dedicata gestito denominato test-Dedicated-IR.</span><span class="sxs-lookup"><span data-stu-id="1985a-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="1985a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1985a-114">PARAMETERS</span></span>

### <span data-ttu-id="1985a-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1985a-115">-Confirm</span></span>
<span data-ttu-id="1985a-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1985a-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1985a-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1985a-117">-DataFactoryName</span></span>
<span data-ttu-id="1985a-118">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="1985a-118">The data factory name.</span></span>

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

### <span data-ttu-id="1985a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1985a-119">-Force</span></span>
<span data-ttu-id="1985a-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="1985a-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1985a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1985a-121">-InputObject</span></span>
<span data-ttu-id="1985a-122">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="1985a-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="1985a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="1985a-123">-Name</span></span>
<span data-ttu-id="1985a-124">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1985a-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="1985a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1985a-125">-ResourceGroupName</span></span>
<span data-ttu-id="1985a-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1985a-126">The resource group name.</span></span>

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

### <span data-ttu-id="1985a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1985a-127">-ResourceId</span></span>
<span data-ttu-id="1985a-128">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="1985a-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1985a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1985a-129">-WhatIf</span></span>
<span data-ttu-id="1985a-130">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1985a-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="1985a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1985a-131">INPUTS</span></span>

### <span data-ttu-id="1985a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1985a-132">System.String</span></span>
<span data-ttu-id="1985a-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1985a-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1985a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1985a-134">OUTPUTS</span></span>

### <span data-ttu-id="1985a-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="1985a-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="1985a-136">Note</span><span class="sxs-lookup"><span data-stu-id="1985a-136">NOTES</span></span>

## <span data-ttu-id="1985a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1985a-137">RELATED LINKS</span></span>
[<span data-ttu-id="1985a-138">Stop-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1985a-138">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
