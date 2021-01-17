---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
ms.openlocfilehash: a3a39db5f110f247ab58f2b4c6afcdb4536f4f50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368210"
---
# <span data-ttu-id="6d145-101">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="6d145-101">Remove-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="6d145-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d145-102">SYNOPSIS</span></span>
<span data-ttu-id="6d145-103">Elimina un'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="6d145-103">Deletes a registration assignment.</span></span>

## <span data-ttu-id="6d145-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d145-104">SYNTAX</span></span>

### <span data-ttu-id="6d145-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6d145-105">Default (Default)</span></span>
```
Remove-AzManagedServicesAssignment [-Scope <String>] -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d145-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6d145-106">ByInputObject</span></span>
```
Remove-AzManagedServicesAssignment -InputObject <PSRegistrationAssignment> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d145-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d145-107">DESCRIPTION</span></span>
<span data-ttu-id="6d145-108">Elimina un'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="6d145-108">Deletes a registration assignment.</span></span>

## <span data-ttu-id="6d145-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d145-109">EXAMPLES</span></span>

### <span data-ttu-id="6d145-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6d145-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80
PS C:\>
```

<span data-ttu-id="6d145-111">Elimina l'assegnazione di registrazione per nome nell'ambito predefinito.</span><span class="sxs-lookup"><span data-stu-id="6d145-111">Deletes the registration assignment by name at the default scope.</span></span>

### <span data-ttu-id="6d145-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6d145-112">Example 2</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 12b05f0f-3426-48da-9e67-738e1dbf775f
PS C:\> Remove-AzManagedServicesAssignment -InputObject $assignment
PS C:\>
```

<span data-ttu-id="6d145-113">Elimina l'assegnazione di registrazione usando l'oggetto di input fornito.</span><span class="sxs-lookup"><span data-stu-id="6d145-113">Deletes the registration assignment using the input object provided.</span></span>

### <span data-ttu-id="6d145-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6d145-114">Example 3</span></span>
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

<span data-ttu-id="6d145-115">Elimina l'assegnazione di registrazione per nome nell'ambito indicato.</span><span class="sxs-lookup"><span data-stu-id="6d145-115">Deletes the registration assignment by name at the given scope.</span></span>

## <span data-ttu-id="6d145-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d145-116">PARAMETERS</span></span>

### <span data-ttu-id="6d145-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d145-117">-DefaultProfile</span></span>
<span data-ttu-id="6d145-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d145-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d145-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d145-119">-InputObject</span></span>
<span data-ttu-id="6d145-120">Oggetto assegnazione registrazione.</span><span class="sxs-lookup"><span data-stu-id="6d145-120">The registration assignment object.</span></span>

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

### <span data-ttu-id="6d145-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d145-121">-Name</span></span>
<span data-ttu-id="6d145-122">Nome univoco dell'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="6d145-122">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="6d145-123">-Ambito</span><span class="sxs-lookup"><span data-stu-id="6d145-123">-Scope</span></span>
<span data-ttu-id="6d145-124">Ambito dell'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="6d145-124">The scope of the registration assignment.</span></span>

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

### <span data-ttu-id="6d145-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d145-125">-AsJob</span></span>
<span data-ttu-id="6d145-126">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6d145-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d145-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6d145-127">-Confirm</span></span>
<span data-ttu-id="6d145-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d145-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d145-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d145-129">-WhatIf</span></span>
<span data-ttu-id="6d145-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d145-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d145-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d145-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d145-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d145-132">CommonParameters</span></span>
<span data-ttu-id="6d145-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d145-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d145-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d145-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d145-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d145-135">INPUTS</span></span>

### <span data-ttu-id="6d145-136">Microsoft. Azure. PowerShell. Cmdlets. ManagedServices. Models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="6d145-136">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="6d145-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d145-137">OUTPUTS</span></span>

### <span data-ttu-id="6d145-138">System. void</span><span class="sxs-lookup"><span data-stu-id="6d145-138">System.Void</span></span>
## <span data-ttu-id="6d145-139">Note</span><span class="sxs-lookup"><span data-stu-id="6d145-139">NOTES</span></span>

## <span data-ttu-id="6d145-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d145-140">RELATED LINKS</span></span>
