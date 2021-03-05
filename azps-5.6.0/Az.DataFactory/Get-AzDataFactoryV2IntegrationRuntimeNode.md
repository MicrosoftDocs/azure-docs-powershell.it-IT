---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: a3b3c25ce424085597de7396be469356f3d3f1c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975166"
---
# <span data-ttu-id="65c4f-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="65c4f-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="65c4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="65c4f-103">Recupera le informazioni sul nodo di runtime dell'integrazione.</span><span class="sxs-lookup"><span data-stu-id="65c4f-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="65c4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65c4f-104">SYNTAX</span></span>

### <span data-ttu-id="65c4f-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="65c4f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65c4f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="65c4f-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65c4f-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="65c4f-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65c4f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="65c4f-108">DESCRIPTION</span></span>
<span data-ttu-id="65c4f-109">Il cmdlet **Get-AzDataFactoryV2IntegrationRuntimeNode** ottiene le informazioni dettagliate di un nodo di runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="65c4f-109">The **Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="65c4f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65c4f-110">EXAMPLES</span></span>

### <span data-ttu-id="65c4f-111">Esempio 1: recupera le informazioni dettagliate di un nodo di runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="65c4f-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
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

<span data-ttu-id="65c4f-112">Il cmdlet ottiene le informazioni sul nodo denominato "Node_1" nel runtime di integrazione self-hosted 'test-selfhost-ir' nel data factory 'test-df-eu2'.</span><span class="sxs-lookup"><span data-stu-id="65c4f-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="65c4f-113">Esempio 2: recupera le informazioni dettagliate di un nodo di runtime di integrazione con l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="65c4f-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
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

<span data-ttu-id="65c4f-114">Il cmdlet ottiene le informazioni sul nodo denominato "Node_1" nel runtime di integrazione self-hosted 'test-selfhost-ir' nel data factory 'test-df-eu2', incluso l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="65c4f-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="65c4f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65c4f-115">PARAMETERS</span></span>

### <span data-ttu-id="65c4f-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="65c4f-116">-DataFactoryName</span></span>
<span data-ttu-id="65c4f-117">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="65c4f-117">The data factory name.</span></span>

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

### <span data-ttu-id="65c4f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65c4f-118">-DefaultProfile</span></span>
<span data-ttu-id="65c4f-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65c4f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65c4f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65c4f-120">-InputObject</span></span>
<span data-ttu-id="65c4f-121">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="65c4f-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="65c4f-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="65c4f-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="65c4f-123">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="65c4f-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="65c4f-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="65c4f-124">-IpAddress</span></span>
<span data-ttu-id="65c4f-125">Indirizzo IP del nodo di runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="65c4f-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="65c4f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="65c4f-126">-Name</span></span>
<span data-ttu-id="65c4f-127">Nome del nodo di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="65c4f-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="65c4f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65c4f-128">-ResourceGroupName</span></span>
<span data-ttu-id="65c4f-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="65c4f-129">The resource group name.</span></span>

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

### <span data-ttu-id="65c4f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65c4f-130">-ResourceId</span></span>
<span data-ttu-id="65c4f-131">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="65c4f-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="65c4f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c4f-132">CommonParameters</span></span>
<span data-ttu-id="65c4f-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65c4f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c4f-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65c4f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c4f-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="65c4f-135">INPUTS</span></span>

### <span data-ttu-id="65c4f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="65c4f-136">System.String</span></span>

### <span data-ttu-id="65c4f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="65c4f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="65c4f-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65c4f-138">OUTPUTS</span></span>

### <span data-ttu-id="65c4f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="65c4f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="65c4f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="65c4f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="65c4f-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="65c4f-141">NOTES</span></span>
<span data-ttu-id="65c4f-142">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori, copia, attività, runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="65c4f-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="65c4f-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65c4f-143">RELATED LINKS</span></span>

[<span data-ttu-id="65c4f-144">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="65c4f-144">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()
