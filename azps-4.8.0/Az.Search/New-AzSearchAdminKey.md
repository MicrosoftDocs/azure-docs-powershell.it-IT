---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
ms.openlocfilehash: ae925d39dab3b56e70cb7c42b320e57eb7f7811a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188259"
---
# <span data-ttu-id="94949-101">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="94949-101">New-AzSearchAdminKey</span></span>

## <span data-ttu-id="94949-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94949-102">SYNOPSIS</span></span>
<span data-ttu-id="94949-103">Rigenera una chiave di amministratore del servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="94949-103">Regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="94949-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94949-104">SYNTAX</span></span>

### <span data-ttu-id="94949-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="94949-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94949-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94949-106">ParentObjectParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94949-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94949-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94949-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94949-108">DESCRIPTION</span></span>
<span data-ttu-id="94949-109">Il cmdlet **New-AzSearchAdminKey** rigenera una chiave di amministratore del servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="94949-109">The **New-AzSearchAdminKey** cmdlet regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="94949-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94949-110">EXAMPLES</span></span>

### <span data-ttu-id="94949-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="94949-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="94949-112">L'esempio rigenera la chiave primaria del servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="94949-112">The example regenerates Primary key of the Azure Search Service.</span></span>

## <span data-ttu-id="94949-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94949-113">PARAMETERS</span></span>

### <span data-ttu-id="94949-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94949-114">-DefaultProfile</span></span>
<span data-ttu-id="94949-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94949-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94949-116">-Force</span><span class="sxs-lookup"><span data-stu-id="94949-116">-Force</span></span>
<span data-ttu-id="94949-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="94949-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="94949-118">-Tipi di tipo</span><span class="sxs-lookup"><span data-stu-id="94949-118">-KeyKind</span></span>
<span data-ttu-id="94949-119">Tipo di chiave di amministrazione del servizio di ricerca (primario/secondario).</span><span class="sxs-lookup"><span data-stu-id="94949-119">Search Service admin key kind (Primary/Secondary).</span></span>

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

### <span data-ttu-id="94949-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="94949-120">-ParentObject</span></span>
<span data-ttu-id="94949-121">Oggetto di input del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="94949-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="94949-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="94949-122">-ParentResourceId</span></span>
<span data-ttu-id="94949-123">ID risorsa del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="94949-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="94949-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94949-124">-ResourceGroupName</span></span>
<span data-ttu-id="94949-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="94949-125">Resource Group name.</span></span>

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

### <span data-ttu-id="94949-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="94949-126">-ServiceName</span></span>
<span data-ttu-id="94949-127">Nome del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="94949-127">Search Service name.</span></span>

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

### <span data-ttu-id="94949-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="94949-128">-Confirm</span></span>
<span data-ttu-id="94949-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94949-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94949-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94949-130">-WhatIf</span></span>
<span data-ttu-id="94949-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94949-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94949-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94949-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94949-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94949-133">CommonParameters</span></span>
<span data-ttu-id="94949-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94949-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94949-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94949-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94949-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94949-136">INPUTS</span></span>

### <span data-ttu-id="94949-137">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="94949-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="94949-138">System. String</span><span class="sxs-lookup"><span data-stu-id="94949-138">System.String</span></span>

## <span data-ttu-id="94949-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94949-139">OUTPUTS</span></span>

### <span data-ttu-id="94949-140">Microsoft. Azure. Commands. Management. search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="94949-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="94949-141">Note</span><span class="sxs-lookup"><span data-stu-id="94949-141">NOTES</span></span>

## <span data-ttu-id="94949-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94949-142">RELATED LINKS</span></span>

[<span data-ttu-id="94949-143">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="94949-143">Get-AzSearchAdminKeyPair</span></span>](./Get-AzSearchAdminKeyPair.md)