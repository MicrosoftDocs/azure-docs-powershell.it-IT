---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 8aae61e163baf95cbed62ea239c7d1a6190aed1f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187486"
---
# <span data-ttu-id="6d9c5-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="6d9c5-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="6d9c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d9c5-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9c5-103">Ottiene una specifica attività di registrazione o un elenco delle assegnazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="6d9c5-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="6d9c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d9c5-104">SYNTAX</span></span>

### <span data-ttu-id="6d9c5-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6d9c5-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d9c5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6d9c5-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d9c5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6d9c5-107">DESCRIPTION</span></span>
<span data-ttu-id="6d9c5-108">Ottiene una specifica attività di registrazione o un elenco delle assegnazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="6d9c5-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="6d9c5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d9c5-109">EXAMPLES</span></span>

### <span data-ttu-id="6d9c5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6d9c5-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="6d9c5-111">Recupera tutte le assegnazioni di registrazione nell'ambito predefinito.</span><span class="sxs-lookup"><span data-stu-id="6d9c5-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="6d9c5-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6d9c5-112">Example 2</span></span>
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

<span data-ttu-id="6d9c5-113">Recupera tutte le assegnazioni di registrazione con i dettagli della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="6d9c5-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="6d9c5-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6d9c5-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="6d9c5-115">Ottiene un'assegnazione di registrazione per nome senza dettagli sulla definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="6d9c5-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="6d9c5-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="6d9c5-116">Example 4</span></span>
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

<span data-ttu-id="6d9c5-117">Ottiene un'assegnazione di registrazione per nome con i dettagli della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="6d9c5-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="6d9c5-118">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="6d9c5-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="6d9c5-119">Recupera tutte le assegnazioni di registrazione in base all'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="6d9c5-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="6d9c5-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d9c5-120">PARAMETERS</span></span>

### <span data-ttu-id="6d9c5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9c5-121">-DefaultProfile</span></span>
<span data-ttu-id="6d9c5-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9c5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d9c5-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="6d9c5-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="6d9c5-124">Se includere i dettagli della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="6d9c5-124">Whether to include registration definition details.</span></span>

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

### <span data-ttu-id="6d9c5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6d9c5-125">-Name</span></span>
<span data-ttu-id="6d9c5-126">Nome univoco dell'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="6d9c5-126">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="6d9c5-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="6d9c5-127">-Scope</span></span>
<span data-ttu-id="6d9c5-128">Ambito in cui è stata creata l'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="6d9c5-128">The scope where the registration assignment created.</span></span>

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

### <span data-ttu-id="6d9c5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9c5-129">CommonParameters</span></span>
<span data-ttu-id="6d9c5-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d9c5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d9c5-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6d9c5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9c5-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="6d9c5-132">INPUTS</span></span>

### <span data-ttu-id="6d9c5-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6d9c5-133">None</span></span>
## <span data-ttu-id="6d9c5-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d9c5-134">OUTPUTS</span></span>

### <span data-ttu-id="6d9c5-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="6d9c5-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="6d9c5-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="6d9c5-136">NOTES</span></span>

## <span data-ttu-id="6d9c5-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d9c5-137">RELATED LINKS</span></span>
