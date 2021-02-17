---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 5fd69c2ec5542ebcf8737f24cfbe068d775f1c04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178670"
---
# <span data-ttu-id="27273-101">Set-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="27273-101">Set-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="27273-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27273-102">SYNOPSIS</span></span>
<span data-ttu-id="27273-103">Aggiornare la risorsa di collegamento privato condiviso per il servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="27273-103">Update the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="27273-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27273-104">SYNTAX</span></span>

### <span data-ttu-id="27273-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27273-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -RequestMessage <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27273-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27273-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> -RequestMessage <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27273-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27273-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceId] <String> -RequestMessage <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27273-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27273-108">InputObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -RequestMessage <String> -InputObject <PSSharedPrivateLinkResource>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27273-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="27273-109">DESCRIPTION</span></span>
<span data-ttu-id="27273-110">Questo **set-AzSearchSharedPrivateLinkResource** aggiorna la risorsa collegamento privato condiviso per il servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="27273-110">This **Set-AzSearchSharedPrivateLinkResource** updates the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="27273-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27273-111">EXAMPLES</span></span>

### <span data-ttu-id="27273-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="27273-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe -RequestMessage "Please kindly approve"


Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : Please kindly approve
ResourceRegion        :
```

<span data-ttu-id="27273-113">Questo esempio aggiorna il messaggio di richiesta per la risorsa di collegamento privato condiviso in sospeso per il servizio Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="27273-113">This example updates the request message for the pending shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="27273-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27273-114">PARAMETERS</span></span>

### <span data-ttu-id="27273-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27273-115">-AsJob</span></span>
<span data-ttu-id="27273-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="27273-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27273-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27273-117">-DefaultProfile</span></span>
<span data-ttu-id="27273-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27273-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27273-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27273-119">-InputObject</span></span>
<span data-ttu-id="27273-120">Oggetto di input della risorsa collegamento privato condiviso</span><span class="sxs-lookup"><span data-stu-id="27273-120">Shared private link resource input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27273-121">-Name</span><span class="sxs-lookup"><span data-stu-id="27273-121">-Name</span></span>
<span data-ttu-id="27273-122">Risorsa collegamento privato condiviso di Ricerca cognitiva di Azure</span><span class="sxs-lookup"><span data-stu-id="27273-122">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="27273-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="27273-123">-ParentObject</span></span>
<span data-ttu-id="27273-124">Oggetto di input del servizio ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="27273-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="27273-125">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="27273-125">-RequestMessage</span></span>
<span data-ttu-id="27273-126">Messaggio di richiesta di risorsa collegamento privato condiviso</span><span class="sxs-lookup"><span data-stu-id="27273-126">Shared private link resource request message</span></span>

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

### <span data-ttu-id="27273-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27273-127">-ResourceGroupName</span></span>
<span data-ttu-id="27273-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="27273-128">Resource Group name.</span></span>

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

### <span data-ttu-id="27273-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27273-129">-ResourceId</span></span>
<span data-ttu-id="27273-130">ID risorsa collegamento privato condiviso</span><span class="sxs-lookup"><span data-stu-id="27273-130">Shared private link resource id</span></span>

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

### <span data-ttu-id="27273-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="27273-131">-ServiceName</span></span>
<span data-ttu-id="27273-132">Nome del servizio Di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="27273-132">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="27273-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27273-133">-Confirm</span></span>
<span data-ttu-id="27273-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27273-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27273-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27273-135">-WhatIf</span></span>
<span data-ttu-id="27273-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27273-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27273-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27273-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27273-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27273-138">CommonParameters</span></span>
<span data-ttu-id="27273-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27273-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27273-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="27273-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27273-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="27273-141">INPUTS</span></span>

### <span data-ttu-id="27273-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="27273-142">None</span></span>

## <span data-ttu-id="27273-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27273-143">OUTPUTS</span></span>

### <span data-ttu-id="27273-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="27273-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="27273-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="27273-145">NOTES</span></span>

## <span data-ttu-id="27273-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27273-146">RELATED LINKS</span></span>

[<span data-ttu-id="27273-147">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="27273-147">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="27273-148">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="27273-148">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="27273-149">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="27273-149">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)