---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: ed5c5bf502e1d19b0ba095e5db68f1f116a71137
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955661"
---
# <span data-ttu-id="fd618-101">Remove-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="fd618-101">Remove-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="fd618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd618-102">SYNOPSIS</span></span>
<span data-ttu-id="fd618-103">Rimuovere la risorsa collegamento privato condiviso dal servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="fd618-103">Remove the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="fd618-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd618-104">SYNTAX</span></span>

### <span data-ttu-id="fd618-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fd618-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd618-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd618-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd618-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd618-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd618-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd618-108">InputObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -InputObject <PSSharedPrivateLinkResource> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd618-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fd618-109">DESCRIPTION</span></span>
<span data-ttu-id="fd618-110">Il cmdlet **Remove-AzSearchSharedPrivateLinkResource** rimuove la risorsa collegamento privato condivisa dal servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="fd618-110">The **Remove-AzSearchSharedPrivateLinkResource** cmdlet removes the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="fd618-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd618-111">EXAMPLES</span></span>

### <span data-ttu-id="fd618-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fd618-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe

Confirm
Remove Shared Private Link Resource 'blob-pe'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="fd618-113">Questo esempio elimina una risorsa di collegamento privato condivisa in base al nome del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="fd618-113">This example deletes a shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="fd618-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd618-114">PARAMETERS</span></span>

### <span data-ttu-id="fd618-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd618-115">-AsJob</span></span>
<span data-ttu-id="fd618-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fd618-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd618-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd618-117">-DefaultProfile</span></span>
<span data-ttu-id="fd618-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd618-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd618-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fd618-119">-Force</span></span>
<span data-ttu-id="fd618-120">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="fd618-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fd618-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd618-121">-InputObject</span></span>
<span data-ttu-id="fd618-122">Oggetto di input della risorsa collegamento privato condiviso</span><span class="sxs-lookup"><span data-stu-id="fd618-122">Shared private link resource input object</span></span>

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

### <span data-ttu-id="fd618-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fd618-123">-Name</span></span>
<span data-ttu-id="fd618-124">Risorsa collegamento privato condiviso di Ricerca cognitiva di Azure</span><span class="sxs-lookup"><span data-stu-id="fd618-124">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="fd618-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fd618-125">-ParentObject</span></span>
<span data-ttu-id="fd618-126">Oggetto di input del servizio di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="fd618-126">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="fd618-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd618-127">-PassThru</span></span>
<span data-ttu-id="fd618-128">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="fd618-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fd618-129">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="fd618-129">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="fd618-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd618-130">-ResourceGroupName</span></span>
<span data-ttu-id="fd618-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fd618-131">Resource Group name.</span></span>

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

### <span data-ttu-id="fd618-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd618-132">-ResourceId</span></span>
<span data-ttu-id="fd618-133">ID risorsa collegamento privato condiviso</span><span class="sxs-lookup"><span data-stu-id="fd618-133">Shared private link resource id</span></span>

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

### <span data-ttu-id="fd618-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fd618-134">-ServiceName</span></span>
<span data-ttu-id="fd618-135">Nome del servizio di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="fd618-135">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="fd618-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd618-136">-Confirm</span></span>
<span data-ttu-id="fd618-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd618-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd618-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd618-138">-WhatIf</span></span>
<span data-ttu-id="fd618-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd618-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd618-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd618-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd618-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd618-141">CommonParameters</span></span>
<span data-ttu-id="fd618-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd618-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd618-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fd618-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd618-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="fd618-144">INPUTS</span></span>

### <span data-ttu-id="fd618-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fd618-145">None</span></span>

## <span data-ttu-id="fd618-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd618-146">OUTPUTS</span></span>

### <span data-ttu-id="fd618-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd618-147">System.Boolean</span></span>

## <span data-ttu-id="fd618-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="fd618-148">NOTES</span></span>

## <span data-ttu-id="fd618-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd618-149">RELATED LINKS</span></span>

[<span data-ttu-id="fd618-150">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="fd618-150">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="fd618-151">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="fd618-151">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="fd618-152">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="fd618-152">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)