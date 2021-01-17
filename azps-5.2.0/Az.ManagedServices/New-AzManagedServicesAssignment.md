---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
ms.openlocfilehash: 8023dde9253ccb4a1f7ff223c4dfdddf773a4728
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368241"
---
# <span data-ttu-id="2993b-101">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="2993b-101">New-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="2993b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2993b-102">SYNOPSIS</span></span>
<span data-ttu-id="2993b-103">Crea o aggiorna un'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2993b-103">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="2993b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2993b-104">SYNTAX</span></span>

### <span data-ttu-id="2993b-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2993b-105">Default (Default)</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>] -RegistrationDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2993b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2993b-106">ByInputObject</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>]
 -RegistrationDefinition <PSRegistrationDefinition> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2993b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2993b-107">DESCRIPTION</span></span>
<span data-ttu-id="2993b-108">Crea o aggiorna un'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2993b-108">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="2993b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2993b-109">EXAMPLES</span></span>

### <span data-ttu-id="2993b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2993b-110">Example 1</span></span>
```
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded

PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\>
```

<span data-ttu-id="2993b-111">Crea un'assegnazione di registrazione nell'ambito predefinito usando l'identificatore della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2993b-111">Creates a registration assignment at the default scope using the registration definition identifier.</span></span>

### <span data-ttu-id="2993b-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2993b-112">Example 2</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinition $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b279ec53-b42f-4952-bd62-cd49982e9572 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/b279ec53-b42f-4952-bd62-cd49982e9572 Succeeded


PS C:\>
```

<span data-ttu-id="2993b-113">Crea un'assegnazione di registrazione con un oggetto definizione di registrazione come input.</span><span class="sxs-lookup"><span data-stu-id="2993b-113">Creates a registration assignment with a registration definition object as input.</span></span>

### <span data-ttu-id="2993b-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="2993b-114">Example 3</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded

PS C:\>
```

<span data-ttu-id="2993b-115">Aggiorna un'assegnazione di registrazione con un nome e un identificatore di definizione della registrazione.</span><span class="sxs-lookup"><span data-stu-id="2993b-115">Updates a registration assignment with a registration definition identifier and name.</span></span>


## <span data-ttu-id="2993b-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2993b-116">PARAMETERS</span></span>

### <span data-ttu-id="2993b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2993b-117">-DefaultProfile</span></span>
<span data-ttu-id="2993b-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2993b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2993b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2993b-119">-Name</span></span>
<span data-ttu-id="2993b-120">Nome univoco dell'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2993b-120">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="2993b-121">-RegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="2993b-121">-RegistrationDefinition</span></span>
<span data-ttu-id="2993b-122">Oggetto di input per la definizione della registrazione.</span><span class="sxs-lookup"><span data-stu-id="2993b-122">The registration definition input object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2993b-123">-RegistrationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="2993b-123">-RegistrationDefinitionId</span></span>
<span data-ttu-id="2993b-124">ID risorsa completo della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2993b-124">The fully qualified resource id of the registration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2993b-125">-Ambito</span><span class="sxs-lookup"><span data-stu-id="2993b-125">-Scope</span></span>
<span data-ttu-id="2993b-126">Ambito in cui deve essere creata l'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2993b-126">The scope where the registration assignment should be created.</span></span>

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

### <span data-ttu-id="2993b-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2993b-127">-AsJob</span></span>
<span data-ttu-id="2993b-128">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2993b-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2993b-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2993b-129">-Confirm</span></span>
<span data-ttu-id="2993b-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2993b-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2993b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2993b-131">-WhatIf</span></span>
<span data-ttu-id="2993b-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2993b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2993b-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2993b-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2993b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2993b-134">CommonParameters</span></span>
<span data-ttu-id="2993b-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2993b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2993b-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2993b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2993b-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2993b-137">INPUTS</span></span>

### <span data-ttu-id="2993b-138">Microsoft. Azure. PowerShell. Cmdlets. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="2993b-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
### <span data-ttu-id="2993b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2993b-139">System.String</span></span>
## <span data-ttu-id="2993b-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2993b-140">OUTPUTS</span></span>

### <span data-ttu-id="2993b-141">Microsoft. Azure. PowerShell. Cmdlets. ManagedServices. Models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="2993b-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="2993b-142">Note</span><span class="sxs-lookup"><span data-stu-id="2993b-142">NOTES</span></span>

## <span data-ttu-id="2993b-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2993b-143">RELATED LINKS</span></span>
