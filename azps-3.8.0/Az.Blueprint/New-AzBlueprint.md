---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
ms.openlocfilehash: 11a2aeffc1ab3bb170b2e8543d9fd5d0300e3ce5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019129"
---
# <span data-ttu-id="5259a-101">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="5259a-101">New-AzBlueprint</span></span>

## <span data-ttu-id="5259a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5259a-102">SYNOPSIS</span></span>
<span data-ttu-id="5259a-103">Creare una nuova definizione Blueprint e salvarla nell'ambito dell'abbonamento o del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="5259a-103">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="5259a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5259a-104">SYNTAX</span></span>

### <span data-ttu-id="5259a-105">CreateBlueprintBySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5259a-105">CreateBlueprintBySubscription (Default)</span></span>
```
New-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5259a-106">CreateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5259a-106">CreateBlueprintByManagementGroup</span></span>
```
New-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5259a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5259a-107">DESCRIPTION</span></span>
<span data-ttu-id="5259a-108">Creare una nuova definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="5259a-108">Create a new blueprint definition.</span></span> 

## <span data-ttu-id="5259a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5259a-109">EXAMPLES</span></span>

### <span data-ttu-id="5259a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5259a-110">Example 1</span></span>
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

<span data-ttu-id="5259a-111">Creare una nuova definizione Blueprint all'interno della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="5259a-111">Create a new blueprint definition within the specified subscription.</span></span>

## <span data-ttu-id="5259a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5259a-112">PARAMETERS</span></span>

### <span data-ttu-id="5259a-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="5259a-113">-BlueprintFile</span></span>
<span data-ttu-id="5259a-114">Percorso di un file JSON Blueprint su disco.</span><span class="sxs-lookup"><span data-stu-id="5259a-114">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5259a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5259a-115">-DefaultProfile</span></span>
<span data-ttu-id="5259a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5259a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5259a-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="5259a-117">-ManagementGroupId</span></span>
<span data-ttu-id="5259a-118">ID gruppo di gestione in cui è o verrà salvata la definizione della cianografia.</span><span class="sxs-lookup"><span data-stu-id="5259a-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5259a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5259a-119">-Name</span></span>
<span data-ttu-id="5259a-120">Nome definizione modello.</span><span class="sxs-lookup"><span data-stu-id="5259a-120">Blueprint definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5259a-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5259a-121">-SubscriptionId</span></span>
<span data-ttu-id="5259a-122">ID sottoscrizione in cui la definizione del progetto è o verrà salvata.</span><span class="sxs-lookup"><span data-stu-id="5259a-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5259a-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5259a-123">-Confirm</span></span>
<span data-ttu-id="5259a-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5259a-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5259a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5259a-125">-WhatIf</span></span>
<span data-ttu-id="5259a-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5259a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5259a-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5259a-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5259a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5259a-128">CommonParameters</span></span>
<span data-ttu-id="5259a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5259a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5259a-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5259a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5259a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5259a-131">INPUTS</span></span>

### <span data-ttu-id="5259a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5259a-132">System.String</span></span>

## <span data-ttu-id="5259a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5259a-133">OUTPUTS</span></span>

### <span data-ttu-id="5259a-134">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="5259a-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="5259a-135">Note</span><span class="sxs-lookup"><span data-stu-id="5259a-135">NOTES</span></span>

## <span data-ttu-id="5259a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5259a-136">RELATED LINKS</span></span>
