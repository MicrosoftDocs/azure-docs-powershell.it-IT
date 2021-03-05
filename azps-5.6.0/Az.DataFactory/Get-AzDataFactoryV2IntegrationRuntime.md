---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 5997ca072ae11407500ceb254dbd16be13382ac8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975262"
---
# <span data-ttu-id="b1a58-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b1a58-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="b1a58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1a58-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a58-103">Ottiene informazioni sulle risorse di runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b1a58-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="b1a58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1a58-104">SYNTAX</span></span>

### <span data-ttu-id="b1a58-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1a58-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1a58-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b1a58-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1a58-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b1a58-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1a58-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b1a58-108">DESCRIPTION</span></span>
<span data-ttu-id="b1a58-109">Il Get-AzDataFactoryV2IntegrationRuntime cmdlet riceve informazioni sui runtime di integrazione in un data factory.</span><span class="sxs-lookup"><span data-stu-id="b1a58-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="b1a58-110">Se si specifica il nome di un runtime di integrazione, questo cmdlet ottiene informazioni su tale runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b1a58-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="b1a58-111">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti i runtime di integrazione in un data factory.</span><span class="sxs-lookup"><span data-stu-id="b1a58-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="b1a58-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1a58-112">EXAMPLES</span></span>

### <span data-ttu-id="b1a58-113">Esempio 1: Elencare tutti i runtime di integrazione in un data factory</span><span class="sxs-lookup"><span data-stu-id="b1a58-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="b1a58-114">Elencare tutti i runtime di integrazione nel data factory denominato "test-df-eu2".</span><span class="sxs-lookup"><span data-stu-id="b1a58-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="b1a58-115">Esempio 2: Ottenere un runtime di integrazione dedicato gestito</span><span class="sxs-lookup"><span data-stu-id="b1a58-115">Example 2: Get managed dedicated integration runtime</span></span>
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

<span data-ttu-id="b1a58-116">Questo comando visualizza informazioni sul runtime di integrazione denominato "test-dedicated-ir" nell'abbonamento per il gruppo di risorse denominato "rg-test-dfv2" e il data factory denominato "test-df-eu2".</span><span class="sxs-lookup"><span data-stu-id="b1a58-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="b1a58-117">Esempio 3: Ottenere un runtime di integrazione dedicato gestito con stato di dettaglio</span><span class="sxs-lookup"><span data-stu-id="b1a58-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
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

<span data-ttu-id="b1a58-118">Questo comando visualizza informazioni sul runtime di integrazione denominato "test-dedicated-ir" nell'abbonamento per il gruppo di risorse denominato "rg-test-dfv2" e il data factory denominato "test-df-eu2".</span><span class="sxs-lookup"><span data-stu-id="b1a58-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="b1a58-119">Esempio 4: Ottenere il runtime di integrazione self-hosted</span><span class="sxs-lookup"><span data-stu-id="b1a58-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="b1a58-120">Questo comando visualizza informazioni sul runtime di integrazione denominato "test-dedicated-ir" nell'abbonamento per il gruppo di risorse denominato "rg-test-dfv2" e il data factory denominato "test-df-eu2".</span><span class="sxs-lookup"><span data-stu-id="b1a58-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="b1a58-121">Esempio 5: Ottenere il runtime di integrazione self-hosted con stato di dettaglio</span><span class="sxs-lookup"><span data-stu-id="b1a58-121">Example 5: Get self-hosted integration runtime with detail status</span></span>
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

## <span data-ttu-id="b1a58-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1a58-122">PARAMETERS</span></span>

### <span data-ttu-id="b1a58-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b1a58-123">-DataFactoryName</span></span>
<span data-ttu-id="b1a58-124">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="b1a58-124">The data factory name.</span></span>

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

### <span data-ttu-id="b1a58-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a58-125">-DefaultProfile</span></span>
<span data-ttu-id="b1a58-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1a58-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1a58-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1a58-127">-InputObject</span></span>
<span data-ttu-id="b1a58-128">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b1a58-128">The integration runtime object.</span></span>

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

### <span data-ttu-id="b1a58-129">-Name</span><span class="sxs-lookup"><span data-stu-id="b1a58-129">-Name</span></span>
<span data-ttu-id="b1a58-130">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b1a58-130">The integration runtime name.</span></span>

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

### <span data-ttu-id="b1a58-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1a58-131">-ResourceGroupName</span></span>
<span data-ttu-id="b1a58-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b1a58-132">The resource group name.</span></span>

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

### <span data-ttu-id="b1a58-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1a58-133">-ResourceId</span></span>
<span data-ttu-id="b1a58-134">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="b1a58-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b1a58-135">-Stato</span><span class="sxs-lookup"><span data-stu-id="b1a58-135">-Status</span></span>
<span data-ttu-id="b1a58-136">Stato dei dettagli del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b1a58-136">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="b1a58-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a58-137">CommonParameters</span></span>
<span data-ttu-id="b1a58-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1a58-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a58-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1a58-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a58-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="b1a58-140">INPUTS</span></span>

### <span data-ttu-id="b1a58-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b1a58-141">System.String</span></span>

### <span data-ttu-id="b1a58-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b1a58-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b1a58-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1a58-143">OUTPUTS</span></span>

### <span data-ttu-id="b1a58-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b1a58-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="b1a58-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b1a58-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="b1a58-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b1a58-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="b1a58-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b1a58-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="b1a58-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="b1a58-148">NOTES</span></span>
<span data-ttu-id="b1a58-149">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori, copia, attività, runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="b1a58-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="b1a58-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1a58-150">RELATED LINKS</span></span>

[<span data-ttu-id="b1a58-151">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b1a58-151">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="b1a58-152">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b1a58-152">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
