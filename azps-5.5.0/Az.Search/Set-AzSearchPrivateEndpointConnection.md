---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: eda4cb403381bd41f7be471b91b2cbba3a6d2ad3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205922"
---
# <span data-ttu-id="cd4ff-101">Set-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd4ff-101">Set-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="cd4ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd4ff-102">SYNOPSIS</span></span>
<span data-ttu-id="cd4ff-103">Aggiornare la connessione dell'endpoint privato al servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="cd4ff-103">Update the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="cd4ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd4ff-104">SYNTAX</span></span>

### <span data-ttu-id="cd4ff-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd4ff-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd4ff-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd4ff-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd4ff-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd4ff-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceId] <String> -Status <PSPrivateLinkServiceConnectionStatus>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd4ff-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd4ff-108">InputObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 -InputObject <PSPrivateEndpointConnection> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd4ff-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cd4ff-109">DESCRIPTION</span></span>
<span data-ttu-id="cd4ff-110">**Set-AzSearchPrivateEndpointConnection** aggiorna la connessione dell'endpoint privato al servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="cd4ff-110">The **Set-AzSearchPrivateEndpointConnection** updates the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="cd4ff-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd4ff-111">EXAMPLES</span></span>

### <span data-ttu-id="cd4ff-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd4ff-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 -Status Rejected  -Description "Rejected" | ConvertTo-Json

{
  "Name": "arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "PrivateEndpoint": {
    "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann2/providers/Microsoft.Network/privateEndpoints/arjagann-test-cuseuap-pe"
  },
  "PrivateLinkServiceConnectionState": {
    "Status": 2,
    "Description": "Rejected",
    "ActionsRequired": "None"
  }
}
```

<span data-ttu-id="cd4ff-113">Questo esempio aggiorna lo stato di una connessione endpoint privata del servizio Ricerca cognitiva di Azure in modo che sia "Rifiutato".</span><span class="sxs-lookup"><span data-stu-id="cd4ff-113">This example updates a private endpoint connection's status of the Azure Cognitive Search service to be "Rejected".</span></span>

## <span data-ttu-id="cd4ff-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd4ff-114">PARAMETERS</span></span>

### <span data-ttu-id="cd4ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd4ff-115">-DefaultProfile</span></span>
<span data-ttu-id="cd4ff-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd4ff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd4ff-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd4ff-117">-Description</span></span>
<span data-ttu-id="cd4ff-118">Descrizione della connessione all'endpoint privato</span><span class="sxs-lookup"><span data-stu-id="cd4ff-118">Private endpoint connection description</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4ff-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd4ff-119">-InputObject</span></span>
<span data-ttu-id="cd4ff-120">Oggetto di input della connessione all'endpoint privato</span><span class="sxs-lookup"><span data-stu-id="cd4ff-120">Private endpoint connection input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd4ff-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cd4ff-121">-Name</span></span>
<span data-ttu-id="cd4ff-122">Nome della connessione all'endpoint privato del servizio Cognitivo di Azure</span><span class="sxs-lookup"><span data-stu-id="cd4ff-122">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4ff-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cd4ff-123">-ParentObject</span></span>
<span data-ttu-id="cd4ff-124">Oggetto di input del servizio ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="cd4ff-124">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd4ff-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd4ff-125">-ResourceGroupName</span></span>
<span data-ttu-id="cd4ff-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd4ff-126">Resource Group name.</span></span>

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

### <span data-ttu-id="cd4ff-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd4ff-127">-ResourceId</span></span>
<span data-ttu-id="cd4ff-128">ID risorsa del servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="cd4ff-128">Private link service resource id</span></span>

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

### <span data-ttu-id="cd4ff-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cd4ff-129">-ServiceName</span></span>
<span data-ttu-id="cd4ff-130">Nome del servizio Di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="cd4ff-130">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="cd4ff-131">-Stato</span><span class="sxs-lookup"><span data-stu-id="cd4ff-131">-Status</span></span>
<span data-ttu-id="cd4ff-132">Stato della connessione al servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="cd4ff-132">Private link service connection status</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateLinkServiceConnectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Pending, Approved, Rejected, Disconnected

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4ff-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd4ff-133">-Confirm</span></span>
<span data-ttu-id="cd4ff-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd4ff-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd4ff-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd4ff-135">-WhatIf</span></span>
<span data-ttu-id="cd4ff-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd4ff-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd4ff-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd4ff-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd4ff-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd4ff-138">CommonParameters</span></span>
<span data-ttu-id="cd4ff-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd4ff-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd4ff-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cd4ff-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd4ff-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="cd4ff-141">INPUTS</span></span>

### <span data-ttu-id="cd4ff-142">System.String</span><span class="sxs-lookup"><span data-stu-id="cd4ff-142">System.String</span></span>

## <span data-ttu-id="cd4ff-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd4ff-143">OUTPUTS</span></span>

### <span data-ttu-id="cd4ff-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd4ff-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="cd4ff-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="cd4ff-145">NOTES</span></span>

## <span data-ttu-id="cd4ff-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd4ff-146">RELATED LINKS</span></span>

[<span data-ttu-id="cd4ff-147">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="cd4ff-147">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="cd4ff-148">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="cd4ff-148">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)
