---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: cbfd316b459c9cd2e1fc60e4416e50c426a3dc19
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488715"
---
# <span data-ttu-id="002b5-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="002b5-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="002b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="002b5-102">SYNOPSIS</span></span>
<span data-ttu-id="002b5-103">Aggiornare una definizione del modello.</span><span class="sxs-lookup"><span data-stu-id="002b5-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="002b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="002b5-104">SYNTAX</span></span>

### <span data-ttu-id="002b5-105">UpdateBlueprintBySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="002b5-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="002b5-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="002b5-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="002b5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="002b5-107">DESCRIPTION</span></span>
<span data-ttu-id="002b5-108">Aggiornare una definizione del modello e salvarla nell'ambito dell'abbonamento o del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="002b5-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="002b5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="002b5-109">EXAMPLES</span></span>

### <span data-ttu-id="002b5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="002b5-110">Example 1</span></span>
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

<span data-ttu-id="002b5-111">Aggiornare una definizione del modello con nuovi parametri.</span><span class="sxs-lookup"><span data-stu-id="002b5-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="002b5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="002b5-112">PARAMETERS</span></span>

### <span data-ttu-id="002b5-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="002b5-113">-BlueprintFile</span></span>
<span data-ttu-id="002b5-114">Percorso di un file JSON Blueprint su disco.</span><span class="sxs-lookup"><span data-stu-id="002b5-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="002b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="002b5-115">-DefaultProfile</span></span>
<span data-ttu-id="002b5-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="002b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="002b5-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="002b5-117">-ManagementGroupId</span></span>
<span data-ttu-id="002b5-118">ID gruppo di gestione in cui è o verrà salvata la definizione della cianografia.</span><span class="sxs-lookup"><span data-stu-id="002b5-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="002b5-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="002b5-119">-Name</span></span>
<span data-ttu-id="002b5-120">Nome definizione modello.</span><span class="sxs-lookup"><span data-stu-id="002b5-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="002b5-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="002b5-121">-SubscriptionId</span></span>
<span data-ttu-id="002b5-122">ID sottoscrizione in cui la definizione del progetto è o verrà salvata.</span><span class="sxs-lookup"><span data-stu-id="002b5-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="002b5-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="002b5-123">-Confirm</span></span>
<span data-ttu-id="002b5-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="002b5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="002b5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="002b5-125">-WhatIf</span></span>
<span data-ttu-id="002b5-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="002b5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="002b5-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="002b5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="002b5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="002b5-128">CommonParameters</span></span>
<span data-ttu-id="002b5-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="002b5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="002b5-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="002b5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="002b5-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="002b5-131">INPUTS</span></span>

### <span data-ttu-id="002b5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="002b5-132">System.String</span></span>

## <span data-ttu-id="002b5-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="002b5-133">OUTPUTS</span></span>

### <span data-ttu-id="002b5-134">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="002b5-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="002b5-135">Note</span><span class="sxs-lookup"><span data-stu-id="002b5-135">NOTES</span></span>

## <span data-ttu-id="002b5-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="002b5-136">RELATED LINKS</span></span>
