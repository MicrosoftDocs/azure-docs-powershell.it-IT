---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: e7a74fcc6d5e1a80282cfb365070df1b339aea45
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189356"
---
# <span data-ttu-id="68281-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="68281-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="68281-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68281-102">SYNOPSIS</span></span>
<span data-ttu-id="68281-103">Rimuovere la chiave di query dal servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="68281-103">Remove the query key from the Azure Search service.</span></span>

## <span data-ttu-id="68281-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68281-104">SYNTAX</span></span>

### <span data-ttu-id="68281-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="68281-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68281-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68281-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68281-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68281-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68281-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68281-108">DESCRIPTION</span></span>
<span data-ttu-id="68281-109">Il cmdlet **Remove-AzSearchQueryKey** rimuove la chiave di query dal servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="68281-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="68281-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68281-110">EXAMPLES</span></span>

### <span data-ttu-id="68281-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="68281-111">Example 1</span></span>
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

<span data-ttu-id="68281-112">Nell'esempio viene rimossa la chiave di query dal servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="68281-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="68281-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68281-113">PARAMETERS</span></span>

### <span data-ttu-id="68281-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68281-114">-DefaultProfile</span></span>
<span data-ttu-id="68281-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68281-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68281-116">-Force</span><span class="sxs-lookup"><span data-stu-id="68281-116">-Force</span></span>
<span data-ttu-id="68281-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="68281-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="68281-118">-Valore della stessa</span><span class="sxs-lookup"><span data-stu-id="68281-118">-KeyValue</span></span>
<span data-ttu-id="68281-119">Valore della chiave query del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="68281-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="68281-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="68281-120">-ParentObject</span></span>
<span data-ttu-id="68281-121">Oggetto di input del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="68281-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="68281-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="68281-122">-ParentResourceId</span></span>
<span data-ttu-id="68281-123">ID risorsa del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="68281-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="68281-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68281-124">-PassThru</span></span>
<span data-ttu-id="68281-125">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="68281-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="68281-126">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="68281-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="68281-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68281-127">-ResourceGroupName</span></span>
<span data-ttu-id="68281-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="68281-128">Resource Group name.</span></span>

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

### <span data-ttu-id="68281-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="68281-129">-ServiceName</span></span>
<span data-ttu-id="68281-130">Nome del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="68281-130">Search Service name.</span></span>

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

### <span data-ttu-id="68281-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="68281-131">-Confirm</span></span>
<span data-ttu-id="68281-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68281-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68281-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68281-133">-WhatIf</span></span>
<span data-ttu-id="68281-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68281-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68281-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68281-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68281-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68281-136">CommonParameters</span></span>
<span data-ttu-id="68281-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68281-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68281-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68281-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68281-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68281-139">INPUTS</span></span>

### <span data-ttu-id="68281-140">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="68281-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="68281-141">System. String</span><span class="sxs-lookup"><span data-stu-id="68281-141">System.String</span></span>

## <span data-ttu-id="68281-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68281-142">OUTPUTS</span></span>

### <span data-ttu-id="68281-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68281-143">System.Boolean</span></span>

## <span data-ttu-id="68281-144">Note</span><span class="sxs-lookup"><span data-stu-id="68281-144">NOTES</span></span>

## <span data-ttu-id="68281-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68281-145">RELATED LINKS</span></span>

[<span data-ttu-id="68281-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="68281-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="68281-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="68281-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
