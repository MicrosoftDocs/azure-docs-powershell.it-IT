---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
ms.openlocfilehash: 790a74ef5a296dbc90e9c1db16678b8c1bacf071
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200911"
---
# <span data-ttu-id="755e8-101">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="755e8-101">New-AzBlueprint</span></span>

## <span data-ttu-id="755e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="755e8-102">SYNOPSIS</span></span>
<span data-ttu-id="755e8-103">Creare una nuova definizione di progetto e salvarla all'interno della sottoscrizione o gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="755e8-103">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="755e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="755e8-104">SYNTAX</span></span>

### <span data-ttu-id="755e8-105">CreateBlueprintBySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="755e8-105">CreateBlueprintBySubscription (Default)</span></span>
```
New-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="755e8-106">CreateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="755e8-106">CreateBlueprintByManagementGroup</span></span>
```
New-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="755e8-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="755e8-107">DESCRIPTION</span></span>
<span data-ttu-id="755e8-108">Creare una nuova definizione di progetto.</span><span class="sxs-lookup"><span data-stu-id="755e8-108">Create a new blueprint definition.</span></span> 

## <span data-ttu-id="755e8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="755e8-109">EXAMPLES</span></span>

### <span data-ttu-id="755e8-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="755e8-110">Example 1</span></span>
```powershell
PS C:\> New-AzBlueprint -Name MyNewBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

Name              : SimpleBlueprint
Id                : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint
ManagementGroupId : myManagementGroupId
Versions          : 
Description       : test
TimeCreated       : 2019-05-12
TargetScope       : Subscription
Parameters        : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue}
ResourceGroups    : {AppNetworkRG}
```

<span data-ttu-id="755e8-111">Creare una nuova definizione di progetto all'interno della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="755e8-111">Create a new blueprint definition within the specified subscription.</span></span>

## <span data-ttu-id="755e8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="755e8-112">PARAMETERS</span></span>

### <span data-ttu-id="755e8-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="755e8-113">-BlueprintFile</span></span>
<span data-ttu-id="755e8-114">Percorso di un file JSON del progetto sul disco.</span><span class="sxs-lookup"><span data-stu-id="755e8-114">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="755e8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="755e8-115">-DefaultProfile</span></span>
<span data-ttu-id="755e8-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="755e8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="755e8-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="755e8-117">-ManagementGroupId</span></span>
<span data-ttu-id="755e8-118">ID gruppo di gestione in cui la definizione del progetto è o verrà salvata.</span><span class="sxs-lookup"><span data-stu-id="755e8-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="755e8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="755e8-119">-Name</span></span>
<span data-ttu-id="755e8-120">Nome della definizione del progetto.</span><span class="sxs-lookup"><span data-stu-id="755e8-120">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="755e8-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="755e8-121">-SubscriptionId</span></span>
<span data-ttu-id="755e8-122">ID abbonamento in cui verrà o sarà salvata la definizione del progetto.</span><span class="sxs-lookup"><span data-stu-id="755e8-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="755e8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="755e8-123">-Confirm</span></span>
<span data-ttu-id="755e8-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="755e8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="755e8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="755e8-125">-WhatIf</span></span>
<span data-ttu-id="755e8-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="755e8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="755e8-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="755e8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="755e8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755e8-128">CommonParameters</span></span>
<span data-ttu-id="755e8-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="755e8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755e8-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="755e8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755e8-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="755e8-131">INPUTS</span></span>

### <span data-ttu-id="755e8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="755e8-132">System.String</span></span>

## <span data-ttu-id="755e8-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="755e8-133">OUTPUTS</span></span>

### <span data-ttu-id="755e8-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="755e8-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="755e8-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="755e8-135">NOTES</span></span>

## <span data-ttu-id="755e8-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="755e8-136">RELATED LINKS</span></span>
