---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 5525dc4613fc1d6bccc56e27de065151b1890f7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190488"
---
# <span data-ttu-id="bf5e1-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bf5e1-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="bf5e1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bf5e1-102">SYNOPSIS</span></span>
<span data-ttu-id="bf5e1-103">Ottiene informazioni sulle risorse di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="bf5e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf5e1-104">SYNTAX</span></span>

### <span data-ttu-id="bf5e1-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bf5e1-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf5e1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bf5e1-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf5e1-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="bf5e1-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf5e1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf5e1-108">DESCRIPTION</span></span>
<span data-ttu-id="bf5e1-109">Il cmdlet Get-AzDataFactoryV2IntegrationRuntime ottiene informazioni sui runtime di integrazione in una data factory.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="bf5e1-110">Se specifichi il nome di un runtime di integrazione, questo cmdlet ottiene le informazioni su tale runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="bf5e1-111">Se non specifichi un nome, questo cmdlet recupera informazioni su tutti i runtime di integrazione in una data factory.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="bf5e1-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf5e1-112">EXAMPLES</span></span>

### <span data-ttu-id="bf5e1-113">Esempio 1: elencare tutti i runtime di integrazione in una data factory</span><span class="sxs-lookup"><span data-stu-id="bf5e1-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="bf5e1-114">Elenca tutti i runtime di integrazione nella data factory denominata ' test-DF-EU2'.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="bf5e1-115">Esempio 2: get Managed Integration Runtime dedicato</span><span class="sxs-lookup"><span data-stu-id="bf5e1-115">Example 2: Get managed dedicated integration runtime</span></span>
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
    PublicIPs                    : 
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="bf5e1-116">Questo comando Visualizza le informazioni sul runtime di integrazione denominato ' test-Dedicated-IR ' nell'abbonamento per il gruppo di risorse denominato ' RG-test-dfv2' e data factory denominato ' test-DF-EU2'.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="bf5e1-117">Esempio 3: get Managed Integration Runtime dedicato con lo stato dei dettagli</span><span class="sxs-lookup"><span data-stu-id="bf5e1-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
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
    PublicIPs                    : 
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="bf5e1-118">Questo comando Visualizza le informazioni sul runtime di integrazione denominato ' test-Dedicated-IR ' nell'abbonamento per il gruppo di risorse denominato ' RG-test-dfv2' e data factory denominato ' test-DF-EU2'.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="bf5e1-119">Esempio 4: Get self-hosted Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="bf5e1-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="bf5e1-120">Questo comando Visualizza le informazioni sul runtime di integrazione denominato ' test-Dedicated-IR ' nell'abbonamento per il gruppo di risorse denominato ' RG-test-dfv2' e data factory denominato ' test-DF-EU2'.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="bf5e1-121">Esempio 5: ottenere un runtime di integrazione autonomo con lo stato dei dettagli</span><span class="sxs-lookup"><span data-stu-id="bf5e1-121">Example 5: Get self-hosted integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir -Status

    State                     : Online
    Version                   : 4.2.7233.1
    CreateTime                : 9/26/2019 6:00:08 AM
    AutoUpdate                : Off
    ScheduledUpdateDate       :
    UpdateDelayOffset         : 03:00:00
    LocalTimeZoneOffset       : 08:00:00
    InternalChannelEncryption :
    Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
    ServiceUrls               : {}
    Nodes                     : {}
    Links                     : {}
    AutoUpdateETA             :
    LatestVersion             : 4.3.7265.1
    PushedVersion             : 4.3.7265.1
    TaskQueueId               : fe2d60b5-86f5-58bf-bdae-7ef698284088
    VersionStatus             : UpdateAvailable
    Name                      : test-selfhost-ir
    Type                      : SelfHosted
    ResourceGroupName         : rg-test-dfv2
    DataFactoryName           : test-df-eu2
    Description               :
    Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
```

## <span data-ttu-id="bf5e1-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bf5e1-122">PARAMETERS</span></span>

### <span data-ttu-id="bf5e1-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="bf5e1-123">-DataFactoryName</span></span>
<span data-ttu-id="bf5e1-124">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-124">The data factory name.</span></span>

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

### <span data-ttu-id="bf5e1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf5e1-125">-DefaultProfile</span></span>
<span data-ttu-id="bf5e1-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf5e1-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf5e1-127">-InputObject</span></span>
<span data-ttu-id="bf5e1-128">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-128">The integration runtime object.</span></span>

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

### <span data-ttu-id="bf5e1-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf5e1-129">-Name</span></span>
<span data-ttu-id="bf5e1-130">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-130">The integration runtime name.</span></span>

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

### <span data-ttu-id="bf5e1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf5e1-131">-ResourceGroupName</span></span>
<span data-ttu-id="bf5e1-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-132">The resource group name.</span></span>

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

### <span data-ttu-id="bf5e1-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf5e1-133">-ResourceId</span></span>
<span data-ttu-id="bf5e1-134">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="bf5e1-135">-Stato</span><span class="sxs-lookup"><span data-stu-id="bf5e1-135">-Status</span></span>
<span data-ttu-id="bf5e1-136">Stato di dettaglio di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-136">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="bf5e1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf5e1-137">CommonParameters</span></span>
<span data-ttu-id="bf5e1-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf5e1-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf5e1-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf5e1-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bf5e1-140">INPUTS</span></span>

### <span data-ttu-id="bf5e1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bf5e1-141">System.String</span></span>

### <span data-ttu-id="bf5e1-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bf5e1-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="bf5e1-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf5e1-143">OUTPUTS</span></span>

### <span data-ttu-id="bf5e1-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bf5e1-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="bf5e1-145">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bf5e1-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="bf5e1-146">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bf5e1-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="bf5e1-147">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bf5e1-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="bf5e1-148">Note</span><span class="sxs-lookup"><span data-stu-id="bf5e1-148">NOTES</span></span>
<span data-ttu-id="bf5e1-149">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory, copy, Activities, Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="bf5e1-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="bf5e1-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf5e1-150">RELATED LINKS</span></span>

[<span data-ttu-id="bf5e1-151">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bf5e1-151">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="bf5e1-152">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bf5e1-152">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
