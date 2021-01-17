---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 8aae61e163baf95cbed62ea239c7d1a6190aed1f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343555"
---
# <span data-ttu-id="b811b-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="b811b-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="b811b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b811b-102">SYNOPSIS</span></span>
<span data-ttu-id="b811b-103">Ottiene una specifica assegnazione di registrazione o un elenco delle assegnazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="b811b-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="b811b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b811b-104">SYNTAX</span></span>

### <span data-ttu-id="b811b-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b811b-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b811b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b811b-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b811b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b811b-107">DESCRIPTION</span></span>
<span data-ttu-id="b811b-108">Ottiene una specifica assegnazione di registrazione o un elenco delle assegnazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="b811b-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="b811b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b811b-109">EXAMPLES</span></span>

### <span data-ttu-id="b811b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b811b-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="b811b-111">Ottiene tutte le assegnazioni di registrazione nell'ambito predefinito.</span><span class="sxs-lookup"><span data-stu-id="b811b-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="b811b-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b811b-112">Example 2</span></span>
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

<span data-ttu-id="b811b-113">Ottiene tutte le assegnazioni di registrazione con i dettagli della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="b811b-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="b811b-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b811b-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="b811b-115">Ottiene un'assegnazione di registrazione per nome senza dettagli sulla definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="b811b-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="b811b-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="b811b-116">Example 4</span></span>
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

<span data-ttu-id="b811b-117">Ottiene un'assegnazione di registrazione per nome con i dettagli della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="b811b-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="b811b-118">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="b811b-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="b811b-119">Ottiene tutte le assegnazioni di registrazione in base a un ambito specifico.</span><span class="sxs-lookup"><span data-stu-id="b811b-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="b811b-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b811b-120">PARAMETERS</span></span>

### <span data-ttu-id="b811b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b811b-121">-DefaultProfile</span></span>
<span data-ttu-id="b811b-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b811b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b811b-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="b811b-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="b811b-124">Se includere i dettagli della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="b811b-124">Whether to include registration definition details.</span></span>

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

### <span data-ttu-id="b811b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b811b-125">-Name</span></span>
<span data-ttu-id="b811b-126">Nome univoco dell'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="b811b-126">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="b811b-127">-Ambito</span><span class="sxs-lookup"><span data-stu-id="b811b-127">-Scope</span></span>
<span data-ttu-id="b811b-128">Ambito in cui è stata creata l'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="b811b-128">The scope where the registration assignment created.</span></span>

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

### <span data-ttu-id="b811b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b811b-129">CommonParameters</span></span>
<span data-ttu-id="b811b-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b811b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b811b-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b811b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b811b-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b811b-132">INPUTS</span></span>

### <span data-ttu-id="b811b-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b811b-133">None</span></span>
## <span data-ttu-id="b811b-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b811b-134">OUTPUTS</span></span>

### <span data-ttu-id="b811b-135">Microsoft. Azure. PowerShell. Cmdlets. ManagedServices. Models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="b811b-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="b811b-136">Note</span><span class="sxs-lookup"><span data-stu-id="b811b-136">NOTES</span></span>

## <span data-ttu-id="b811b-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b811b-137">RELATED LINKS</span></span>
