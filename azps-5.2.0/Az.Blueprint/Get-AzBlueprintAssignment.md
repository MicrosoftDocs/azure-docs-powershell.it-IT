---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 06398b9c5e880577606e0367722fc22c242d58f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327779"
---
# <span data-ttu-id="6cc64-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="6cc64-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="6cc64-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6cc64-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc64-103">Ottenere una o più assegnazioni Blueprint.</span><span class="sxs-lookup"><span data-stu-id="6cc64-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="6cc64-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cc64-104">SYNTAX</span></span>

### <span data-ttu-id="6cc64-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6cc64-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cc64-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="6cc64-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cc64-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="6cc64-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cc64-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="6cc64-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cc64-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cc64-109">DESCRIPTION</span></span>
<span data-ttu-id="6cc64-110">Ottenere una o più assegnazioni Blueprint.</span><span class="sxs-lookup"><span data-stu-id="6cc64-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="6cc64-111">Le assegnazioni di cianografiche esistono nell'ambito dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6cc64-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="6cc64-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cc64-112">EXAMPLES</span></span>

### <span data-ttu-id="6cc64-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6cc64-113">Example 1</span></span>
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

<span data-ttu-id="6cc64-114">Ottenere le assegnazioni Blueprint all'interno della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="6cc64-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="6cc64-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6cc64-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="6cc64-116">Ottenere l'assegnazione del progetto con il nome specificato all'interno della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="6cc64-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="6cc64-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6cc64-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="6cc64-118">Ottenere le assegnazioni del progetto all'interno del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="6cc64-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="6cc64-119">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="6cc64-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="6cc64-120">Ottenere l'assegnazione del progetto con il nome specificato nel gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="6cc64-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="6cc64-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6cc64-121">PARAMETERS</span></span>

### <span data-ttu-id="6cc64-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc64-122">-DefaultProfile</span></span>
<span data-ttu-id="6cc64-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6cc64-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cc64-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="6cc64-124">-ManagementGroupId</span></span>
<span data-ttu-id="6cc64-125">ID del gruppo di gestione in cui viene salvata l'assegnazione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="6cc64-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="6cc64-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="6cc64-126">-Name</span></span>
<span data-ttu-id="6cc64-127">Nome assegnazione modello.</span><span class="sxs-lookup"><span data-stu-id="6cc64-127">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="6cc64-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cc64-128">-SubscriptionId</span></span>
<span data-ttu-id="6cc64-129">ID abbonamento a cui è distribuita l'assegnazione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="6cc64-129">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="6cc64-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc64-130">CommonParameters</span></span>
<span data-ttu-id="6cc64-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cc64-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc64-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cc64-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc64-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6cc64-133">INPUTS</span></span>

### <span data-ttu-id="6cc64-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6cc64-134">System.String</span></span>

## <span data-ttu-id="6cc64-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cc64-135">OUTPUTS</span></span>

### <span data-ttu-id="6cc64-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="6cc64-136">System.Object</span></span>
## <span data-ttu-id="6cc64-137">Note</span><span class="sxs-lookup"><span data-stu-id="6cc64-137">NOTES</span></span>

## <span data-ttu-id="6cc64-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cc64-138">RELATED LINKS</span></span>
