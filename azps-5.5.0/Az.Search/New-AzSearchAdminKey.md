---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
ms.openlocfilehash: 28eabb6ccc583a1f3f141c9f02239eca84b04e81
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192703"
---
# <span data-ttu-id="37b3d-101">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="37b3d-101">New-AzSearchAdminKey</span></span>

## <span data-ttu-id="37b3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="37b3d-103">Rigenera una chiave di amministratore del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="37b3d-103">Regenerates an admin key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="37b3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37b3d-104">SYNTAX</span></span>

### <span data-ttu-id="37b3d-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="37b3d-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37b3d-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37b3d-106">ParentObjectParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37b3d-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37b3d-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37b3d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="37b3d-108">DESCRIPTION</span></span>
<span data-ttu-id="37b3d-109">Il cmdlet **New-AzSearchAdminKey** rigenera una chiave di amministratore del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="37b3d-109">The **New-AzSearchAdminKey** cmdlet regenerates an admin key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="37b3d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37b3d-110">EXAMPLES</span></span>

### <span data-ttu-id="37b3d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="37b3d-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="37b3d-112">L'esempio rigenera la chiave primaria del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="37b3d-112">The example regenerates Primary key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="37b3d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37b3d-113">PARAMETERS</span></span>

### <span data-ttu-id="37b3d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b3d-114">-DefaultProfile</span></span>
<span data-ttu-id="37b3d-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37b3d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37b3d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="37b3d-116">-Force</span></span>
<span data-ttu-id="37b3d-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="37b3d-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="37b3d-118">-Key Ritieni</span><span class="sxs-lookup"><span data-stu-id="37b3d-118">-KeyKind</span></span>
<span data-ttu-id="37b3d-119">Tipo di chiave di chiave del servizio ricerca cognitiva di Azure (primaria/secondaria).</span><span class="sxs-lookup"><span data-stu-id="37b3d-119">Azure Cognitive Search Service admin key kind (Primary/Secondary).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKeyKind
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b3d-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="37b3d-120">-ParentObject</span></span>
<span data-ttu-id="37b3d-121">Oggetto di input del servizio ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="37b3d-121">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="37b3d-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="37b3d-122">-ParentResourceId</span></span>
<span data-ttu-id="37b3d-123">ID risorsa del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="37b3d-123">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="37b3d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37b3d-124">-ResourceGroupName</span></span>
<span data-ttu-id="37b3d-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="37b3d-125">Resource Group name.</span></span>

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

### <span data-ttu-id="37b3d-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="37b3d-126">-ServiceName</span></span>
<span data-ttu-id="37b3d-127">Nome del servizio Di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="37b3d-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="37b3d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37b3d-128">-Confirm</span></span>
<span data-ttu-id="37b3d-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37b3d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37b3d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37b3d-130">-WhatIf</span></span>
<span data-ttu-id="37b3d-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37b3d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37b3d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37b3d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37b3d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b3d-133">CommonParameters</span></span>
<span data-ttu-id="37b3d-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37b3d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b3d-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="37b3d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b3d-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="37b3d-136">INPUTS</span></span>

### <span data-ttu-id="37b3d-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="37b3d-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="37b3d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="37b3d-138">System.String</span></span>

## <span data-ttu-id="37b3d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37b3d-139">OUTPUTS</span></span>

### <span data-ttu-id="37b3d-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="37b3d-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="37b3d-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="37b3d-141">NOTES</span></span>

## <span data-ttu-id="37b3d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37b3d-142">RELATED LINKS</span></span>

[<span data-ttu-id="37b3d-143">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="37b3d-143">Get-AzSearchAdminKeyPair</span></span>](./Get-AzSearchAdminKeyPair.md)
