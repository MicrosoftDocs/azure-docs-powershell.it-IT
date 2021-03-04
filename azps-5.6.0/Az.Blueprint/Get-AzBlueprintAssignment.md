---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 375eca319a1db467e97addac50faa3f91fe0ecc5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954862"
---
# <span data-ttu-id="48db5-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="48db5-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="48db5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48db5-102">SYNOPSIS</span></span>
<span data-ttu-id="48db5-103">Ottieni una o più attività di progetto.</span><span class="sxs-lookup"><span data-stu-id="48db5-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="48db5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48db5-104">SYNTAX</span></span>

### <span data-ttu-id="48db5-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48db5-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48db5-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="48db5-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48db5-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="48db5-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48db5-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="48db5-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48db5-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="48db5-109">DESCRIPTION</span></span>
<span data-ttu-id="48db5-110">Ottieni una o più attività di progetto.</span><span class="sxs-lookup"><span data-stu-id="48db5-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="48db5-111">Le assegnazioni del progetto sono presenti nell'ambito della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="48db5-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="48db5-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48db5-112">EXAMPLES</span></span>

### <span data-ttu-id="48db5-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="48db5-113">Example 1</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name              : Assignment-PS-BlueprintDefinition
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : AllResourcesReadOnly
ProvisioningState : Succeeded
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="48db5-114">Ottenere le assegnazioni della progetto all'interno della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="48db5-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="48db5-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="48db5-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="48db5-116">Ottenere l'assegnazione della progetto con il nome specificato all'interno della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="48db5-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="48db5-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="48db5-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="48db5-118">Ottenere le assegnazioni della progetto all'interno del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="48db5-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="48db5-119">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="48db5-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="48db5-120">Ottenere l'assegnazione della progetto con il nome specificato all'interno del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="48db5-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="48db5-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48db5-121">PARAMETERS</span></span>

### <span data-ttu-id="48db5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48db5-122">-DefaultProfile</span></span>
<span data-ttu-id="48db5-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48db5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48db5-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="48db5-124">-ManagementGroupId</span></span>
<span data-ttu-id="48db5-125">ID del gruppo di gestione in cui viene salvata l'assegnazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="48db5-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48db5-126">-Name</span><span class="sxs-lookup"><span data-stu-id="48db5-126">-Name</span></span>
<span data-ttu-id="48db5-127">Nome dell'attività del progetto.</span><span class="sxs-lookup"><span data-stu-id="48db5-127">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48db5-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48db5-128">-SubscriptionId</span></span>
<span data-ttu-id="48db5-129">ID sottoscrizione a cui viene distribuita l'assegnazione della progetto.</span><span class="sxs-lookup"><span data-stu-id="48db5-129">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48db5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48db5-130">CommonParameters</span></span>
<span data-ttu-id="48db5-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48db5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48db5-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="48db5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48db5-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="48db5-133">INPUTS</span></span>

### <span data-ttu-id="48db5-134">System.String</span><span class="sxs-lookup"><span data-stu-id="48db5-134">System.String</span></span>

## <span data-ttu-id="48db5-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48db5-135">OUTPUTS</span></span>

### <span data-ttu-id="48db5-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="48db5-136">System.Object</span></span>
## <span data-ttu-id="48db5-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="48db5-137">NOTES</span></span>

## <span data-ttu-id="48db5-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48db5-138">RELATED LINKS</span></span>
