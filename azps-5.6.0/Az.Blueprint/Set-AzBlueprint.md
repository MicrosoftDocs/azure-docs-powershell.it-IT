---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: 5511be0e20c99a6a120e2f7591287b9ee17b0943
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965101"
---
# <span data-ttu-id="61ca2-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="61ca2-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="61ca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="61ca2-103">Aggiornare la definizione di progetto.</span><span class="sxs-lookup"><span data-stu-id="61ca2-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="61ca2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61ca2-104">SYNTAX</span></span>

### <span data-ttu-id="61ca2-105">UpdateBlueprintBySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61ca2-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61ca2-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="61ca2-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61ca2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="61ca2-107">DESCRIPTION</span></span>
<span data-ttu-id="61ca2-108">Aggiornare una definizione di progetto e salvarla all'interno della sottoscrizione o del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="61ca2-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="61ca2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61ca2-109">EXAMPLES</span></span>

### <span data-ttu-id="61ca2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61ca2-110">Example 1</span></span>
```powershell
PS C:\> Set-AzBlueprint -Name MyBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

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

<span data-ttu-id="61ca2-111">Aggiornare la definizione di una progetto con nuovi parametri.</span><span class="sxs-lookup"><span data-stu-id="61ca2-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="61ca2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61ca2-112">PARAMETERS</span></span>

### <span data-ttu-id="61ca2-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="61ca2-113">-BlueprintFile</span></span>
<span data-ttu-id="61ca2-114">Percorso di un file JSON del progetto sul disco.</span><span class="sxs-lookup"><span data-stu-id="61ca2-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="61ca2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ca2-115">-DefaultProfile</span></span>
<span data-ttu-id="61ca2-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61ca2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61ca2-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="61ca2-117">-ManagementGroupId</span></span>
<span data-ttu-id="61ca2-118">ID gruppo di gestione in cui la definizione del progetto è o verrà salvata.</span><span class="sxs-lookup"><span data-stu-id="61ca2-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61ca2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="61ca2-119">-Name</span></span>
<span data-ttu-id="61ca2-120">Nome della definizione del progetto.</span><span class="sxs-lookup"><span data-stu-id="61ca2-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="61ca2-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="61ca2-121">-SubscriptionId</span></span>
<span data-ttu-id="61ca2-122">ID sottoscrizione in cui verrà o sarà salvata la definizione del progetto.</span><span class="sxs-lookup"><span data-stu-id="61ca2-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61ca2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61ca2-123">-Confirm</span></span>
<span data-ttu-id="61ca2-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61ca2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61ca2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61ca2-125">-WhatIf</span></span>
<span data-ttu-id="61ca2-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61ca2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61ca2-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61ca2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61ca2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ca2-128">CommonParameters</span></span>
<span data-ttu-id="61ca2-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61ca2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ca2-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61ca2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ca2-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="61ca2-131">INPUTS</span></span>

### <span data-ttu-id="61ca2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="61ca2-132">System.String</span></span>

## <span data-ttu-id="61ca2-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61ca2-133">OUTPUTS</span></span>

### <span data-ttu-id="61ca2-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="61ca2-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="61ca2-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="61ca2-135">NOTES</span></span>

## <span data-ttu-id="61ca2-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61ca2-136">RELATED LINKS</span></span>
