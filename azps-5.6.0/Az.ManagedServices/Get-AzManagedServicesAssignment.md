---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 5f0398981f6c3a59c9401df4ec89208a5f8196b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965789"
---
# <span data-ttu-id="5a960-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="5a960-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="5a960-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a960-102">SYNOPSIS</span></span>
<span data-ttu-id="5a960-103">Ottiene una specifica attività di registrazione o un elenco delle assegnazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="5a960-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="5a960-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a960-104">SYNTAX</span></span>

### <span data-ttu-id="5a960-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5a960-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a960-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5a960-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a960-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5a960-107">DESCRIPTION</span></span>
<span data-ttu-id="5a960-108">Ottiene una specifica attività di registrazione o un elenco delle assegnazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="5a960-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="5a960-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a960-109">EXAMPLES</span></span>

### <span data-ttu-id="5a960-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5a960-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="5a960-111">Recupera tutte le assegnazioni di registrazione nell'ambito predefinito.</span><span class="sxs-lookup"><span data-stu-id="5a960-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="5a960-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5a960-112">Example 2</span></span>
```
PS C:\> $assignments = Get-AzManagedServicesAssignment -ExpandRegistrationDefinition
PS C:\> $assignments[0].Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="5a960-113">Recupera tutte le assegnazioni di registrazione con i dettagli della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="5a960-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="5a960-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5a960-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="5a960-115">Ottiene un'assegnazione di registrazione per nome senza dettagli sulla definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="5a960-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="5a960-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="5a960-116">Example 4</span></span>
```
PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80 -ExpandRegistrationDefinition
PS C:\> $assignment.Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="5a960-117">Ottiene un'assegnazione di registrazione per nome con i dettagli della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="5a960-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="5a960-118">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="5a960-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="5a960-119">Recupera tutte le assegnazioni di registrazione in base all'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="5a960-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="5a960-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a960-120">PARAMETERS</span></span>

### <span data-ttu-id="5a960-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a960-121">-DefaultProfile</span></span>
<span data-ttu-id="5a960-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a960-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a960-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="5a960-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="5a960-124">Se includere i dettagli della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="5a960-124">Whether to include registration definition details.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a960-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5a960-125">-Name</span></span>
<span data-ttu-id="5a960-126">Nome univoco dell'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="5a960-126">The unique name of the Registration Assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a960-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="5a960-127">-Scope</span></span>
<span data-ttu-id="5a960-128">Ambito in cui è stata creata l'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="5a960-128">The scope where the registration assignment created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a960-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a960-129">CommonParameters</span></span>
<span data-ttu-id="5a960-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a960-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a960-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5a960-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a960-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="5a960-132">INPUTS</span></span>

### <span data-ttu-id="5a960-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5a960-133">None</span></span>
## <span data-ttu-id="5a960-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a960-134">OUTPUTS</span></span>

### <span data-ttu-id="5a960-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="5a960-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="5a960-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="5a960-136">NOTES</span></span>

## <span data-ttu-id="5a960-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a960-137">RELATED LINKS</span></span>
