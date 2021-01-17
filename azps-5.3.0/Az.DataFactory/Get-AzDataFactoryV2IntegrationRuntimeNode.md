---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 4d99a495863f93acfb97b290488fd0db24d69444
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487623"
---
# <span data-ttu-id="a15c9-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a15c9-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="a15c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a15c9-102">SYNOPSIS</span></span>
<span data-ttu-id="a15c9-103">Ottiene le informazioni sul nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="a15c9-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="a15c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a15c9-104">SYNTAX</span></span>

### <span data-ttu-id="a15c9-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a15c9-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a15c9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a15c9-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a15c9-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="a15c9-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a15c9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a15c9-108">DESCRIPTION</span></span>
<span data-ttu-id="a15c9-109">Il cmdlet **Get-AzDataFactoryV2IntegrationRuntimeNode** ottiene le informazioni dettagliate di un nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="a15c9-109">The **Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="a15c9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a15c9-110">EXAMPLES</span></span>

### <span data-ttu-id="a15c9-111">Esempio 1: ottiene le informazioni dettagliate di un nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="a15c9-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              :
```

<span data-ttu-id="a15c9-112">Il cmdlet ottiene le informazioni del nodo denominato ' Node_1' in self-hosted Integration Runtime ' test-SelfHost-IR ' in Factory di dati ' test-DF-EU2'.</span><span class="sxs-lookup"><span data-stu-id="a15c9-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="a15c9-113">Esempio 2: ottiene le informazioni dettagliate di un nodo di Integration runtime insieme all'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="a15c9-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              : 167.220.1.167
```

<span data-ttu-id="a15c9-114">Il cmdlet ottiene le informazioni del nodo denominato "Node_1" in self-hosted Integration Runtime "test-SelfHost-IR" in data factory test-DF-EU2 ", incluso l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="a15c9-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="a15c9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a15c9-115">PARAMETERS</span></span>

### <span data-ttu-id="a15c9-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a15c9-116">-DataFactoryName</span></span>
<span data-ttu-id="a15c9-117">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="a15c9-117">The data factory name.</span></span>

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

### <span data-ttu-id="a15c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a15c9-118">-DefaultProfile</span></span>
<span data-ttu-id="a15c9-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a15c9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a15c9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a15c9-120">-InputObject</span></span>
<span data-ttu-id="a15c9-121">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="a15c9-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="a15c9-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="a15c9-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="a15c9-123">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a15c9-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a15c9-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="a15c9-124">-IpAddress</span></span>
<span data-ttu-id="a15c9-125">Indirizzo IP del nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="a15c9-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="a15c9-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="a15c9-126">-Name</span></span>
<span data-ttu-id="a15c9-127">Nome del nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="a15c9-127">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a15c9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a15c9-128">-ResourceGroupName</span></span>
<span data-ttu-id="a15c9-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a15c9-129">The resource group name.</span></span>

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

### <span data-ttu-id="a15c9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a15c9-130">-ResourceId</span></span>
<span data-ttu-id="a15c9-131">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="a15c9-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a15c9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a15c9-132">CommonParameters</span></span>
<span data-ttu-id="a15c9-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a15c9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a15c9-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a15c9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a15c9-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a15c9-135">INPUTS</span></span>

### <span data-ttu-id="a15c9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a15c9-136">System.String</span></span>

### <span data-ttu-id="a15c9-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a15c9-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a15c9-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a15c9-138">OUTPUTS</span></span>

### <span data-ttu-id="a15c9-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a15c9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="a15c9-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a15c9-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="a15c9-141">Note</span><span class="sxs-lookup"><span data-stu-id="a15c9-141">NOTES</span></span>
<span data-ttu-id="a15c9-142">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory, copy, Activities, Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="a15c9-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="a15c9-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a15c9-143">RELATED LINKS</span></span>

[<span data-ttu-id="a15c9-144">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a15c9-144">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()
