---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 96c635caef26a1dc90ae2646cb4899012105f526
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684619"
---
# <span data-ttu-id="1c2af-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1c2af-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="1c2af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c2af-102">SYNOPSIS</span></span>
<span data-ttu-id="1c2af-103">Ottiene informazioni sulle risorse di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="1c2af-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="1c2af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c2af-104">SYNTAX</span></span>

### <span data-ttu-id="1c2af-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c2af-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c2af-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1c2af-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c2af-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="1c2af-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c2af-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c2af-108">DESCRIPTION</span></span>
<span data-ttu-id="1c2af-109">Il cmdlet Get-AzDataFactoryV2IntegrationRuntime ottiene informazioni sui runtime di integrazione in una data factory.</span><span class="sxs-lookup"><span data-stu-id="1c2af-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="1c2af-110">Se specifichi il nome di un runtime di integrazione, questo cmdlet ottiene le informazioni su tale runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1c2af-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="1c2af-111">Se non specifichi un nome, questo cmdlet recupera informazioni su tutti i runtime di integrazione in una data factory.</span><span class="sxs-lookup"><span data-stu-id="1c2af-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="1c2af-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c2af-112">EXAMPLES</span></span>

### <span data-ttu-id="1c2af-113">Esempio 1: elencare tutti i runtime di integrazione in una data factory</span><span class="sxs-lookup"><span data-stu-id="1c2af-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="1c2af-114">Elenca tutti i runtime di integrazione nella data factory denominata ' test-DF-EU2'.</span><span class="sxs-lookup"><span data-stu-id="1c2af-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="1c2af-115">Esempio 2: get Managed Integration Runtime dedicato</span><span class="sxs-lookup"><span data-stu-id="1c2af-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="1c2af-116">Questo comando Visualizza le informazioni sul runtime di integrazione denominato ' test-Dedicated-IR ' nell'abbonamento per il gruppo di risorse denominato ' RG-test-dfv2' e data factory denominato ' test-DF-EU2'.</span><span class="sxs-lookup"><span data-stu-id="1c2af-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="1c2af-117">Esempio 3: get Managed Integration Runtime dedicato con lo stato dei dettagli</span><span class="sxs-lookup"><span data-stu-id="1c2af-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

    CreateTime                   : 
    Nodes                        : 
    OtherErrors                  : 
    LastOperation                : 
    State                        : Initial
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="1c2af-118">Questo comando Visualizza le informazioni sul runtime di integrazione denominato ' test-Dedicated-IR ' nell'abbonamento per il gruppo di risorse denominato ' RG-test-dfv2' e data factory denominato ' test-DF-EU2'.</span><span class="sxs-lookup"><span data-stu-id="1c2af-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="1c2af-119">Esempio 4: Get self-hosted Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="1c2af-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="1c2af-120">Questo comando Visualizza le informazioni sul runtime di integrazione denominato ' test-Dedicated-IR ' nell'abbonamento per il gruppo di risorse denominato ' RG-test-dfv2' e data factory denominato ' test-DF-EU2'.</span><span class="sxs-lookup"><span data-stu-id="1c2af-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="1c2af-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c2af-121">PARAMETERS</span></span>

### <span data-ttu-id="1c2af-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1c2af-122">-DataFactoryName</span></span>
<span data-ttu-id="1c2af-123">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="1c2af-123">The data factory name.</span></span>

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

### <span data-ttu-id="1c2af-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c2af-124">-DefaultProfile</span></span>
<span data-ttu-id="1c2af-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c2af-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c2af-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c2af-126">-InputObject</span></span>
<span data-ttu-id="1c2af-127">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="1c2af-127">The integration runtime object.</span></span>

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

### <span data-ttu-id="1c2af-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c2af-128">-Name</span></span>
<span data-ttu-id="1c2af-129">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1c2af-129">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c2af-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c2af-130">-ResourceGroupName</span></span>
<span data-ttu-id="1c2af-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1c2af-131">The resource group name.</span></span>

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

### <span data-ttu-id="1c2af-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c2af-132">-ResourceId</span></span>
<span data-ttu-id="1c2af-133">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="1c2af-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1c2af-134">-Stato</span><span class="sxs-lookup"><span data-stu-id="1c2af-134">-Status</span></span>
<span data-ttu-id="1c2af-135">Stato di dettaglio di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="1c2af-135">The integration runtime detail status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c2af-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c2af-136">CommonParameters</span></span>
<span data-ttu-id="1c2af-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c2af-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c2af-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c2af-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c2af-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c2af-139">INPUTS</span></span>

### <span data-ttu-id="1c2af-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1c2af-140">System.String</span></span>

### <span data-ttu-id="1c2af-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1c2af-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1c2af-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c2af-142">OUTPUTS</span></span>

### <span data-ttu-id="1c2af-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1c2af-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="1c2af-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1c2af-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="1c2af-145">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1c2af-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="1c2af-146">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1c2af-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="1c2af-147">Note</span><span class="sxs-lookup"><span data-stu-id="1c2af-147">NOTES</span></span>
<span data-ttu-id="1c2af-148">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory, copy, Activities, Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="1c2af-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="1c2af-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c2af-149">RELATED LINKS</span></span>

[<span data-ttu-id="1c2af-150">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1c2af-150">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="1c2af-151">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1c2af-151">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
