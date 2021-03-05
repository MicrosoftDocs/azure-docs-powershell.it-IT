---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/powershell/module/az.managedservices/remove-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
ms.openlocfilehash: f63b27c19b2ba1366b1418360a731829041f5247
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983086"
---
# <span data-ttu-id="2357b-101">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="2357b-101">Remove-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="2357b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2357b-102">SYNOPSIS</span></span>
<span data-ttu-id="2357b-103">Elimina un'attività di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2357b-103">Deletes a registration assignment.</span></span>

## <span data-ttu-id="2357b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2357b-104">SYNTAX</span></span>

### <span data-ttu-id="2357b-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2357b-105">Default (Default)</span></span>
```
Remove-AzManagedServicesAssignment [-Scope <String>] -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2357b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2357b-106">ByInputObject</span></span>
```
Remove-AzManagedServicesAssignment -InputObject <PSRegistrationAssignment> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2357b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2357b-107">DESCRIPTION</span></span>
<span data-ttu-id="2357b-108">Elimina un'attività di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2357b-108">Deletes a registration assignment.</span></span>

## <span data-ttu-id="2357b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2357b-109">EXAMPLES</span></span>

### <span data-ttu-id="2357b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2357b-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80
PS C:\>
```

<span data-ttu-id="2357b-111">Elimina l'assegnazione di registrazione per nome nell'ambito predefinito.</span><span class="sxs-lookup"><span data-stu-id="2357b-111">Deletes the registration assignment by name at the default scope.</span></span>

### <span data-ttu-id="2357b-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2357b-112">Example 2</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 12b05f0f-3426-48da-9e67-738e1dbf775f
PS C:\> Remove-AzManagedServicesAssignment -InputObject $assignment
PS C:\>
```

<span data-ttu-id="2357b-113">Elimina l'assegnazione di registrazione usando l'oggetto di input fornito.</span><span class="sxs-lookup"><span data-stu-id="2357b-113">Deletes the registration assignment using the input object provided.</span></span>

### <span data-ttu-id="2357b-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="2357b-114">Example 3</span></span>
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


PS C:\> Remove-AzManagedServicesAssignment -Name b279ec53-b42f-4952-bd62-cd49982e9572 -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8
PS C:\>
```

<span data-ttu-id="2357b-115">Elimina l'assegnazione di registrazione per nome nell'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="2357b-115">Deletes the registration assignment by name at the given scope.</span></span>

## <span data-ttu-id="2357b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2357b-116">PARAMETERS</span></span>

### <span data-ttu-id="2357b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2357b-117">-DefaultProfile</span></span>
<span data-ttu-id="2357b-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2357b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2357b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2357b-119">-InputObject</span></span>
<span data-ttu-id="2357b-120">Oggetto assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2357b-120">The registration assignment object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2357b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2357b-121">-Name</span></span>
<span data-ttu-id="2357b-122">Nome univoco dell'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2357b-122">The unique name of the Registration Assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2357b-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="2357b-123">-Scope</span></span>
<span data-ttu-id="2357b-124">Ambito dell'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2357b-124">The scope of the registration assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2357b-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2357b-125">-AsJob</span></span>
<span data-ttu-id="2357b-126">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2357b-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2357b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2357b-127">-Confirm</span></span>
<span data-ttu-id="2357b-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2357b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2357b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2357b-129">-WhatIf</span></span>
<span data-ttu-id="2357b-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2357b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2357b-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2357b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2357b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2357b-132">CommonParameters</span></span>
<span data-ttu-id="2357b-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2357b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2357b-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2357b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2357b-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="2357b-135">INPUTS</span></span>

### <span data-ttu-id="2357b-136">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="2357b-136">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="2357b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2357b-137">OUTPUTS</span></span>

### <span data-ttu-id="2357b-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="2357b-138">System.Void</span></span>
## <span data-ttu-id="2357b-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="2357b-139">NOTES</span></span>

## <span data-ttu-id="2357b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2357b-140">RELATED LINKS</span></span>
