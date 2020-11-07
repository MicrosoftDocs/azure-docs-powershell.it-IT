---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 0e3d08384383f858ed65c30637e7321663344959
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864262"
---
# <span data-ttu-id="ce583-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="ce583-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="ce583-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce583-102">SYNOPSIS</span></span>
<span data-ttu-id="ce583-103">Ottenere una o più assegnazioni Blueprint.</span><span class="sxs-lookup"><span data-stu-id="ce583-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="ce583-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce583-104">SYNTAX</span></span>

### <span data-ttu-id="ce583-105">BlueprintAssignmentsBySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ce583-105">BlueprintAssignmentsBySubscription (Default)</span></span>
```
Get-AzBlueprintAssignment [[-SubscriptionId] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce583-106">BlueprintAssignmentByName</span><span class="sxs-lookup"><span data-stu-id="ce583-106">BlueprintAssignmentByName</span></span>
```
Get-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce583-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce583-107">DESCRIPTION</span></span>
<span data-ttu-id="ce583-108">Ottenere una o più assegnazioni Blueprint.</span><span class="sxs-lookup"><span data-stu-id="ce583-108">Get one or more blueprint assignments.</span></span> <span data-ttu-id="ce583-109">Le assegnazioni di cianografiche esistono nell'ambito dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ce583-109">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="ce583-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce583-110">EXAMPLES</span></span>

### <span data-ttu-id="ce583-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ce583-111">Example 1</span></span>
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

<span data-ttu-id="ce583-112">Ottenere le assegnazioni Blueprint all'interno della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="ce583-112">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="ce583-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ce583-113">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="ce583-114">Ottenere l'assegnazione del progetto con il nome specificato all'interno della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="ce583-114">Get the blueprint assignment with the given name within the specified subscription.</span></span>

## <span data-ttu-id="ce583-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce583-115">PARAMETERS</span></span>

### <span data-ttu-id="ce583-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce583-116">-DefaultProfile</span></span>
<span data-ttu-id="ce583-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce583-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce583-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce583-118">-Name</span></span>
<span data-ttu-id="ce583-119">Nome assegnazione modello.</span><span class="sxs-lookup"><span data-stu-id="ce583-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce583-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce583-120">-SubscriptionId</span></span>
<span data-ttu-id="ce583-121">ID abbonamento a cui è distribuita l'assegnazione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="ce583-121">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce583-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce583-122">CommonParameters</span></span>
<span data-ttu-id="ce583-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce583-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce583-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce583-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce583-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce583-125">INPUTS</span></span>

### <span data-ttu-id="ce583-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ce583-126">System.String</span></span>

## <span data-ttu-id="ce583-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce583-127">OUTPUTS</span></span>

### <span data-ttu-id="ce583-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="ce583-128">System.Object</span></span>
## <span data-ttu-id="ce583-129">Note</span><span class="sxs-lookup"><span data-stu-id="ce583-129">NOTES</span></span>

## <span data-ttu-id="ce583-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce583-130">RELATED LINKS</span></span>
