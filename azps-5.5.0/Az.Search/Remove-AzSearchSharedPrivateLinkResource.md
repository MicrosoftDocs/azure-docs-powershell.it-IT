---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 922989583a071384de98343e12d48ce68cc32db8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205923"
---
# <span data-ttu-id="dfe46-101">Remove-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="dfe46-101">Remove-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="dfe46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfe46-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe46-103">Rimuovere la risorsa collegamento privato condiviso dal servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe46-103">Remove the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="dfe46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfe46-104">SYNTAX</span></span>

### <span data-ttu-id="dfe46-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dfe46-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dfe46-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfe46-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe46-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfe46-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe46-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfe46-108">InputObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -InputObject <PSSharedPrivateLinkResource> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfe46-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dfe46-109">DESCRIPTION</span></span>
<span data-ttu-id="dfe46-110">Il cmdlet **Remove-AzSearchSharedPrivateLinkResource** rimuove la risorsa collegamento privato condivisa dal servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe46-110">The **Remove-AzSearchSharedPrivateLinkResource** cmdlet removes the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="dfe46-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfe46-111">EXAMPLES</span></span>

### <span data-ttu-id="dfe46-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dfe46-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe

Confirm
Remove Shared Private Link Resource 'blob-pe'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="dfe46-113">Questo esempio elimina una risorsa di collegamento privato condivisa in base al nome del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe46-113">This example deletes a shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="dfe46-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfe46-114">PARAMETERS</span></span>

### <span data-ttu-id="dfe46-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfe46-115">-AsJob</span></span>
<span data-ttu-id="dfe46-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="dfe46-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dfe46-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe46-117">-DefaultProfile</span></span>
<span data-ttu-id="dfe46-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe46-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfe46-119">-Force</span><span class="sxs-lookup"><span data-stu-id="dfe46-119">-Force</span></span>
<span data-ttu-id="dfe46-120">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="dfe46-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dfe46-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfe46-121">-InputObject</span></span>
<span data-ttu-id="dfe46-122">Oggetto di input della risorsa collegamento privato condiviso</span><span class="sxs-lookup"><span data-stu-id="dfe46-122">Shared private link resource input object</span></span>

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

### <span data-ttu-id="dfe46-123">-Name</span><span class="sxs-lookup"><span data-stu-id="dfe46-123">-Name</span></span>
<span data-ttu-id="dfe46-124">Risorsa collegamento privato condiviso di Ricerca cognitiva di Azure</span><span class="sxs-lookup"><span data-stu-id="dfe46-124">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="dfe46-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dfe46-125">-ParentObject</span></span>
<span data-ttu-id="dfe46-126">Oggetto di input del servizio ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe46-126">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="dfe46-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dfe46-127">-PassThru</span></span>
<span data-ttu-id="dfe46-128">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="dfe46-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="dfe46-129">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="dfe46-129">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="dfe46-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe46-130">-ResourceGroupName</span></span>
<span data-ttu-id="dfe46-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dfe46-131">Resource Group name.</span></span>

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

### <span data-ttu-id="dfe46-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfe46-132">-ResourceId</span></span>
<span data-ttu-id="dfe46-133">ID risorsa collegamento privato condiviso</span><span class="sxs-lookup"><span data-stu-id="dfe46-133">Shared private link resource id</span></span>

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

### <span data-ttu-id="dfe46-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="dfe46-134">-ServiceName</span></span>
<span data-ttu-id="dfe46-135">Nome del servizio Di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe46-135">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="dfe46-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfe46-136">-Confirm</span></span>
<span data-ttu-id="dfe46-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfe46-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfe46-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfe46-138">-WhatIf</span></span>
<span data-ttu-id="dfe46-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfe46-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfe46-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfe46-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfe46-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe46-141">CommonParameters</span></span>
<span data-ttu-id="dfe46-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfe46-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe46-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dfe46-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe46-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="dfe46-144">INPUTS</span></span>

### <span data-ttu-id="dfe46-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="dfe46-145">None</span></span>

## <span data-ttu-id="dfe46-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfe46-146">OUTPUTS</span></span>

### <span data-ttu-id="dfe46-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dfe46-147">System.Boolean</span></span>

## <span data-ttu-id="dfe46-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="dfe46-148">NOTES</span></span>

## <span data-ttu-id="dfe46-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfe46-149">RELATED LINKS</span></span>

[<span data-ttu-id="dfe46-150">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="dfe46-150">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="dfe46-151">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="dfe46-151">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="dfe46-152">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="dfe46-152">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)