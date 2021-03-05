---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 98b5f30bfe3a829d276c435c9beef71cf8a2f7de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986633"
---
# <span data-ttu-id="2e716-101">Remove-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2e716-101">Remove-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="2e716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e716-102">SYNOPSIS</span></span>
<span data-ttu-id="2e716-103">Rimuovere la connessione all'endpoint privato dal servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e716-103">Remove the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="2e716-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e716-104">SYNTAX</span></span>

### <span data-ttu-id="2e716-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2e716-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e716-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e716-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e716-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e716-107">InputObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -InputObject <PSPrivateEndpointConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e716-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e716-108">ResourceIdParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e716-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2e716-109">DESCRIPTION</span></span>
<span data-ttu-id="2e716-110">**Remove-AzSearchPrivateEndpointConnection** rimuove la connessione all'endpoint privato dal servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e716-110">The **Remove-AzSearchPrivateEndpointConnection** removes the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="2e716-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e716-111">EXAMPLES</span></span>

### <span data-ttu-id="2e716-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2e716-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="2e716-113">Questo esempio rimuove una connessione all'endpoint privato dal servizio di ricerca in base al nome.</span><span class="sxs-lookup"><span data-stu-id="2e716-113">This example removes a private endpoint connection from the search service by name.</span></span>

## <span data-ttu-id="2e716-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e716-114">PARAMETERS</span></span>

### <span data-ttu-id="2e716-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e716-115">-DefaultProfile</span></span>
<span data-ttu-id="2e716-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e716-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e716-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2e716-117">-Force</span></span>
<span data-ttu-id="2e716-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="2e716-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2e716-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e716-119">-InputObject</span></span>
<span data-ttu-id="2e716-120">Oggetto di input della connessione all'endpoint privato</span><span class="sxs-lookup"><span data-stu-id="2e716-120">Private endpoint connection input object</span></span>

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

### <span data-ttu-id="2e716-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2e716-121">-Name</span></span>
<span data-ttu-id="2e716-122">Nome della connessione all'endpoint privato del servizio Cognitivo di Azure</span><span class="sxs-lookup"><span data-stu-id="2e716-122">Azure Cognitive Search Service private endpoint connection name</span></span>

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

### <span data-ttu-id="2e716-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2e716-123">-ParentObject</span></span>
<span data-ttu-id="2e716-124">Oggetto di input del servizio di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e716-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="2e716-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e716-125">-PassThru</span></span>
<span data-ttu-id="2e716-126">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2e716-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2e716-127">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2e716-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="2e716-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e716-128">-ResourceGroupName</span></span>
<span data-ttu-id="2e716-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2e716-129">Resource Group name.</span></span>

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

### <span data-ttu-id="2e716-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e716-130">-ResourceId</span></span>
<span data-ttu-id="2e716-131">ID risorsa del servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="2e716-131">Private link service resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e716-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2e716-132">-ServiceName</span></span>
<span data-ttu-id="2e716-133">Nome del servizio di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e716-133">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="2e716-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e716-134">-Confirm</span></span>
<span data-ttu-id="2e716-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e716-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e716-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e716-136">-WhatIf</span></span>
<span data-ttu-id="2e716-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e716-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e716-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e716-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e716-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e716-139">CommonParameters</span></span>
<span data-ttu-id="2e716-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e716-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e716-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2e716-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e716-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="2e716-142">INPUTS</span></span>

### <span data-ttu-id="2e716-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2e716-143">None</span></span>

## <span data-ttu-id="2e716-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e716-144">OUTPUTS</span></span>

### <span data-ttu-id="2e716-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e716-145">System.Boolean</span></span>

## <span data-ttu-id="2e716-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="2e716-146">NOTES</span></span>

## <span data-ttu-id="2e716-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e716-147">RELATED LINKS</span></span>

[<span data-ttu-id="2e716-148">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="2e716-148">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="2e716-149">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="2e716-149">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)