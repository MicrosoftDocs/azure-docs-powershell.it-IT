---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: eb5c139aea0520df77bf86af01bc3c02f8118263
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205930"
---
# <span data-ttu-id="7606f-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7606f-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="7606f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7606f-102">SYNOPSIS</span></span>
<span data-ttu-id="7606f-103">Rimuovere un servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="7606f-103">Remove an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="7606f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7606f-104">SYNTAX</span></span>

### <span data-ttu-id="7606f-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7606f-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7606f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7606f-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7606f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7606f-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7606f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7606f-108">DESCRIPTION</span></span>
<span data-ttu-id="7606f-109">Il cmdlet **Remove-AzSearchService** rimuove un servizio di Ricerca cognitiva di Azure con parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="7606f-109">The **Remove-AzSearchService** cmdlet removes an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="7606f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7606f-110">EXAMPLES</span></span>

### <span data-ttu-id="7606f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7606f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="7606f-112">L'esempio rimuove un servizio Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="7606f-112">The example removes an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="7606f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7606f-113">PARAMETERS</span></span>

### <span data-ttu-id="7606f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7606f-114">-DefaultProfile</span></span>
<span data-ttu-id="7606f-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7606f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7606f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7606f-116">-Force</span></span>
<span data-ttu-id="7606f-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="7606f-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7606f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7606f-118">-InputObject</span></span>
<span data-ttu-id="7606f-119">Oggetto di input del servizio ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="7606f-119">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7606f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7606f-120">-Name</span></span>
<span data-ttu-id="7606f-121">Nome del servizio Di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="7606f-121">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="7606f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7606f-122">-PassThru</span></span>
<span data-ttu-id="7606f-123">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7606f-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="7606f-124">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7606f-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7606f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7606f-125">-ResourceGroupName</span></span>
<span data-ttu-id="7606f-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7606f-126">Resource Group name.</span></span>

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

### <span data-ttu-id="7606f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7606f-127">-ResourceId</span></span>
<span data-ttu-id="7606f-128">ID risorsa del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="7606f-128">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="7606f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7606f-129">-Confirm</span></span>
<span data-ttu-id="7606f-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7606f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7606f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7606f-131">-WhatIf</span></span>
<span data-ttu-id="7606f-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7606f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7606f-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7606f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7606f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7606f-134">CommonParameters</span></span>
<span data-ttu-id="7606f-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7606f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7606f-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7606f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7606f-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="7606f-137">INPUTS</span></span>

### <span data-ttu-id="7606f-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="7606f-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="7606f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7606f-139">System.String</span></span>

## <span data-ttu-id="7606f-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7606f-140">OUTPUTS</span></span>

### <span data-ttu-id="7606f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7606f-141">System.Boolean</span></span>

## <span data-ttu-id="7606f-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="7606f-142">NOTES</span></span>

## <span data-ttu-id="7606f-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7606f-143">RELATED LINKS</span></span>

[<span data-ttu-id="7606f-144">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7606f-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="7606f-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7606f-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="7606f-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7606f-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)
