---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 34f8b99ef4c8958415780fecb98c291d2845209d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018947"
---
# <span data-ttu-id="3a83d-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="3a83d-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="3a83d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a83d-102">SYNOPSIS</span></span>
<span data-ttu-id="3a83d-103">Rimuovere un'assegnazione Blueprint da un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3a83d-103">Remove a blueprint assignment from a subscription.</span></span>

## <span data-ttu-id="3a83d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a83d-104">SYNTAX</span></span>

### <span data-ttu-id="3a83d-105">DeleteBlueprintAssignmentByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3a83d-105">DeleteBlueprintAssignmentByName (Default)</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a83d-106">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="3a83d-106">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-InputObject] <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a83d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a83d-107">DESCRIPTION</span></span>
<span data-ttu-id="3a83d-108">Rimuovere un modello assegnato a un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3a83d-108">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="3a83d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a83d-109">EXAMPLES</span></span>

### <span data-ttu-id="3a83d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3a83d-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="3a83d-111">Rimuovere l'assegnazione Blueprint specificata per nome dall'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="3a83d-111">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="3a83d-112">Il cmdlet richiederà la conferma prima di eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="3a83d-112">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="3a83d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a83d-113">PARAMETERS</span></span>

### <span data-ttu-id="3a83d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a83d-114">-DefaultProfile</span></span>
<span data-ttu-id="3a83d-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a83d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a83d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a83d-116">-InputObject</span></span>
<span data-ttu-id="3a83d-117">Oggetto assegnazione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="3a83d-117">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a83d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a83d-118">-Name</span></span>
<span data-ttu-id="3a83d-119">Nome assegnazione modello.</span><span class="sxs-lookup"><span data-stu-id="3a83d-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a83d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a83d-120">-PassThru</span></span>
<span data-ttu-id="3a83d-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3a83d-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3a83d-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a83d-122">-SubscriptionId</span></span>
<span data-ttu-id="3a83d-123">ID abbonamento a cui è distribuita l'assegnazione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="3a83d-123">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a83d-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3a83d-124">-Confirm</span></span>
<span data-ttu-id="3a83d-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a83d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a83d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a83d-126">-WhatIf</span></span>
<span data-ttu-id="3a83d-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a83d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a83d-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a83d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a83d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a83d-129">CommonParameters</span></span>
<span data-ttu-id="3a83d-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a83d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a83d-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a83d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a83d-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a83d-132">INPUTS</span></span>

### <span data-ttu-id="3a83d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3a83d-133">System.String</span></span>

### <span data-ttu-id="3a83d-134">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="3a83d-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="3a83d-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a83d-135">OUTPUTS</span></span>

### <span data-ttu-id="3a83d-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="3a83d-136">System.Object</span></span>
## <span data-ttu-id="3a83d-137">Note</span><span class="sxs-lookup"><span data-stu-id="3a83d-137">NOTES</span></span>

## <span data-ttu-id="3a83d-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a83d-138">RELATED LINKS</span></span>
