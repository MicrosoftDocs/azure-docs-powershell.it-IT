---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
ms.openlocfilehash: c53489e943b2e8afc10f655b59c6ed076974198a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191490"
---
# <span data-ttu-id="14004-101">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="14004-101">New-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="14004-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14004-102">SYNOPSIS</span></span>
<span data-ttu-id="14004-103">Crea o aggiorna un'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="14004-103">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="14004-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14004-104">SYNTAX</span></span>

### <span data-ttu-id="14004-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14004-105">Default (Default)</span></span>
```
New-AzManagedServicesAssignment [[-Scope] <String>] -RegistrationDefinitionName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14004-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="14004-106">ByResourceId</span></span>
```
New-AzManagedServicesAssignment [[-Scope] <String>] -RegistrationDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14004-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="14004-107">ByInputObject</span></span>
```
New-AzManagedServicesAssignment [[-Scope] <String>] -RegistrationDefinition <PSRegistrationDefinition> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14004-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14004-108">DESCRIPTION</span></span>
<span data-ttu-id="14004-109">Crea o aggiorna un'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="14004-109">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="14004-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14004-110">EXAMPLES</span></span>

### <span data-ttu-id="14004-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="14004-111">Example 1</span></span>
```powershell
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/d4d14a4c-9b54-4dc3-b755-6d0659e0224b

Name                                 RegistrationDefinitionId
----                                 ------------------------
3b3d5411-ec8c-4a52-8972-73f4952724b2 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/d4d14a4c-9b54-4dc3-b755-6d0659e0224b
```

<span data-ttu-id="14004-112">Crea una nuova assegnazione di registrazione in base all'ID di risorsa completo della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="14004-112">Creates a new registration assignment given the fully qualified resource id of the registration definition.</span></span>

### <span data-ttu-id="14004-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="14004-113">Example 2</span></span>
```powershell
New-AzManagedServicesAssignment -Scope /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/resourceGroups/mygroup1 -RegistrationDefinitionName 47f471b3-ff5f-463c-8a1f-286501b01ddc

Name                                 RegistrationDefinitionId
----                                 ------------------------
5aa0d921-64b8-40e8-af33-31993f0deaa8 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/47f471b3-ff5f-463c-8a1f-286501b01ddc
```

<span data-ttu-id="14004-114">Crea un'assegnazione di registrazione assegnata a un ambito e al nome della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="14004-114">Creates a the registration assignment given a scope and the registration definition name.</span></span>

### <span data-ttu-id="14004-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="14004-115">Example 3</span></span>
```powershell
PS C:\> $def = New-AzManagedServicesDefinition -RegistrationDefinitionName asd -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7"
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinition $def

Name                                 RegistrationDefinitionId
----                                 ------------------------
a25f63d9-605c-4878-99bd-0d315480d46b /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/4a50f8eb-96b3-44c4-a397-e1e57035fe65
```
<span data-ttu-id="14004-116">Crea un'assegnazione di registrazione assegnata a un oggetto di definizione della registrazione.</span><span class="sxs-lookup"><span data-stu-id="14004-116">Creates a the registration assignment given a registration definition object.</span></span>
## <span data-ttu-id="14004-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14004-117">PARAMETERS</span></span>

### <span data-ttu-id="14004-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14004-118">-AsJob</span></span>
<span data-ttu-id="14004-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="14004-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14004-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14004-120">-DefaultProfile</span></span>
<span data-ttu-id="14004-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14004-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14004-122">-RegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="14004-122">-RegistrationDefinition</span></span>
<span data-ttu-id="14004-123">Oggetto di input per la definizione della registrazione.</span><span class="sxs-lookup"><span data-stu-id="14004-123">The registration definition input object.</span></span>

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

### <span data-ttu-id="14004-124">-RegistrationDefinitionResourceId</span><span class="sxs-lookup"><span data-stu-id="14004-124">-RegistrationDefinitionResourceId</span></span>
<span data-ttu-id="14004-125">ID risorsa completo della definizione di registrazione, ad esempio/subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationDefinitions/b0c052e5-c437-4771-a476-8b1201158a57.</span><span class="sxs-lookup"><span data-stu-id="14004-125">The fully qualified resource id of the registration definition (for example, /subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationDefinitions/b0c052e5-c437-4771-a476-8b1201158a57).</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14004-126">-RegistrationDefinitionName</span><span class="sxs-lookup"><span data-stu-id="14004-126">-RegistrationDefinitionName</span></span>
<span data-ttu-id="14004-127">Nome della definizione di registrazione, ad esempio b0c052e5-c437-4771-A476-8b1201158a57.</span><span class="sxs-lookup"><span data-stu-id="14004-127">The registration definition name (for example, b0c052e5-c437-4771-a476-8b1201158a57.</span></span>

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

### <span data-ttu-id="14004-128">-Ambito</span><span class="sxs-lookup"><span data-stu-id="14004-128">-Scope</span></span>
<span data-ttu-id="14004-129">Ambito in cui deve essere creata l'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="14004-129">The scope where the registration assignment should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14004-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="14004-130">-Confirm</span></span>
<span data-ttu-id="14004-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14004-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14004-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14004-132">-WhatIf</span></span>
<span data-ttu-id="14004-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14004-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14004-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14004-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14004-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14004-135">CommonParameters</span></span>
<span data-ttu-id="14004-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14004-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14004-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14004-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14004-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14004-138">INPUTS</span></span>

### <span data-ttu-id="14004-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="14004-139">None</span></span>

## <span data-ttu-id="14004-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14004-140">OUTPUTS</span></span>

### <span data-ttu-id="14004-141">Microsoft. Azure. PowerShell. Cmdlets. ManagedServices. Models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="14004-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>

## <span data-ttu-id="14004-142">Note</span><span class="sxs-lookup"><span data-stu-id="14004-142">NOTES</span></span>

## <span data-ttu-id="14004-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14004-143">RELATED LINKS</span></span>
