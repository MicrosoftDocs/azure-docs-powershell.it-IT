---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 0ed07bed894d31be68b8fd4b71605e94b19171ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999789"
---
# <span data-ttu-id="bb70b-101">Get-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bb70b-101">Get-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="bb70b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb70b-102">SYNOPSIS</span></span>
<span data-ttu-id="bb70b-103">Ottiene le connessioni endpoint private al servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb70b-103">Gets private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="bb70b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb70b-104">SYNTAX</span></span>

### <span data-ttu-id="bb70b-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bb70b-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb70b-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb70b-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb70b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb70b-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb70b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bb70b-108">DESCRIPTION</span></span>
<span data-ttu-id="bb70b-109">Il cmdlet **Get-AzSearchPrivateEndpointConnection** ottiene le connessioni degli endpoint privati al servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb70b-109">The **Get-AzSearchPrivateEndpointConnection** cmdlet gets the private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="bb70b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb70b-110">EXAMPLES</span></span>

### <span data-ttu-id="bb70b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bb70b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Name                                                          Id
----                                                          --
arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="bb70b-112">L'esempio ottiene tutte le connessioni degli endpoint privati al servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb70b-112">The example gets all the private endpoint connections to the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="bb70b-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bb70b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266  | ConvertTo-Json

{
  "Name": "arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "PrivateEndpoint": {
    "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann2/providers/Microsoft.Network/privateEndpoints/arjagann-test-cuseuap-pe"
  },
  "PrivateLinkServiceConnectionState": {
    "Status": 1,
    "Description": "Auto-approved",
    "ActionsRequired": "None"
  }
}
```

<span data-ttu-id="bb70b-114">L'esempio ottiene una specifica connessione all'endpoint privato per nome (convertita in JSON per facilitare la lettura) nel servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb70b-114">The example gets a specific private endpoint connection by name (converted to JSON for ease of reading) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="bb70b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb70b-115">PARAMETERS</span></span>

### <span data-ttu-id="bb70b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb70b-116">-DefaultProfile</span></span>
<span data-ttu-id="bb70b-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb70b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb70b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bb70b-118">-Name</span></span>
<span data-ttu-id="bb70b-119">Nome della connessione all'endpoint privato del servizio Cognitivo di Azure</span><span class="sxs-lookup"><span data-stu-id="bb70b-119">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb70b-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bb70b-120">-ParentObject</span></span>
<span data-ttu-id="bb70b-121">Oggetto di input del servizio di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb70b-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb70b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb70b-122">-ResourceGroupName</span></span>
<span data-ttu-id="bb70b-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bb70b-123">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb70b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb70b-124">-ResourceId</span></span>
<span data-ttu-id="bb70b-125">ID risorsa del servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="bb70b-125">Private link service resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb70b-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="bb70b-126">-ServiceName</span></span>
<span data-ttu-id="bb70b-127">Nome del servizio di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb70b-127">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb70b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb70b-128">-Confirm</span></span>
<span data-ttu-id="bb70b-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb70b-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb70b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb70b-130">-WhatIf</span></span>
<span data-ttu-id="bb70b-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb70b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb70b-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb70b-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb70b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb70b-133">CommonParameters</span></span>
<span data-ttu-id="bb70b-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb70b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb70b-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bb70b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb70b-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="bb70b-136">INPUTS</span></span>

### <span data-ttu-id="bb70b-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="bb70b-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="bb70b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bb70b-138">System.String</span></span>

## <span data-ttu-id="bb70b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb70b-139">OUTPUTS</span></span>

### <span data-ttu-id="bb70b-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bb70b-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="bb70b-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="bb70b-141">NOTES</span></span>

## <span data-ttu-id="bb70b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb70b-142">RELATED LINKS</span></span>

[<span data-ttu-id="bb70b-143">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="bb70b-143">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="bb70b-144">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="bb70b-144">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)
