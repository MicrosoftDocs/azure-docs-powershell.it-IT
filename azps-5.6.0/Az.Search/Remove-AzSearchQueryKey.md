---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: 79e7ff902d75387180e519bbaf8a5cdc3e2431a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016014"
---
# <span data-ttu-id="aea3c-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="aea3c-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="aea3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aea3c-102">SYNOPSIS</span></span>
<span data-ttu-id="aea3c-103">Rimuovere la chiave di query dal servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="aea3c-103">Remove the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="aea3c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aea3c-104">SYNTAX</span></span>

### <span data-ttu-id="aea3c-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aea3c-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aea3c-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aea3c-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aea3c-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aea3c-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aea3c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aea3c-108">DESCRIPTION</span></span>
<span data-ttu-id="aea3c-109">Il cmdlet **Remove-AzSearchQueryKey** rimuove la chiave di query dal servizio Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="aea3c-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="aea3c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aea3c-110">EXAMPLES</span></span>

### <span data-ttu-id="aea3c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aea3c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name         Key                             
----         ---                             
             D260F448EA192EBC19D59F7E5670E8BB
NewQueryKey1 B4C13E3F6FA76100D3488673CFDCD438

PS C:\> Remove-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyValue B4C13E3F6FA76100D3488673CFDCD438

Confirm
Are you sure you want to remove query key 'B4C13E3F6FA76100D3488673CFDCD438'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="aea3c-112">L'esempio rimuove la chiave di query dal servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="aea3c-112">The example removes the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="aea3c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aea3c-113">PARAMETERS</span></span>

### <span data-ttu-id="aea3c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea3c-114">-DefaultProfile</span></span>
<span data-ttu-id="aea3c-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aea3c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aea3c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="aea3c-116">-Force</span></span>
<span data-ttu-id="aea3c-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="aea3c-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="aea3c-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="aea3c-118">-KeyValue</span></span>
<span data-ttu-id="aea3c-119">Valore di chiave della chiave della query del servizio cognitivo di Azure.</span><span class="sxs-lookup"><span data-stu-id="aea3c-119">Azure Cognitive Search Service query key value.</span></span>

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

### <span data-ttu-id="aea3c-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="aea3c-120">-ParentObject</span></span>
<span data-ttu-id="aea3c-121">Oggetto di input del servizio di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="aea3c-121">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="aea3c-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="aea3c-122">-ParentResourceId</span></span>
<span data-ttu-id="aea3c-123">ID risorsa del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="aea3c-123">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aea3c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aea3c-124">-PassThru</span></span>
<span data-ttu-id="aea3c-125">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="aea3c-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="aea3c-126">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="aea3c-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="aea3c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aea3c-127">-ResourceGroupName</span></span>
<span data-ttu-id="aea3c-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aea3c-128">Resource Group name.</span></span>

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

### <span data-ttu-id="aea3c-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="aea3c-129">-ServiceName</span></span>
<span data-ttu-id="aea3c-130">Nome del servizio di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="aea3c-130">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="aea3c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aea3c-131">-Confirm</span></span>
<span data-ttu-id="aea3c-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aea3c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aea3c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aea3c-133">-WhatIf</span></span>
<span data-ttu-id="aea3c-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aea3c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aea3c-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aea3c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aea3c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea3c-136">CommonParameters</span></span>
<span data-ttu-id="aea3c-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aea3c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea3c-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aea3c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea3c-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="aea3c-139">INPUTS</span></span>

### <span data-ttu-id="aea3c-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="aea3c-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="aea3c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="aea3c-141">System.String</span></span>

## <span data-ttu-id="aea3c-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aea3c-142">OUTPUTS</span></span>

### <span data-ttu-id="aea3c-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aea3c-143">System.Boolean</span></span>

## <span data-ttu-id="aea3c-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="aea3c-144">NOTES</span></span>

## <span data-ttu-id="aea3c-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aea3c-145">RELATED LINKS</span></span>

[<span data-ttu-id="aea3c-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="aea3c-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="aea3c-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="aea3c-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
