---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
ms.openlocfilehash: 47a76f15700a4697dc7256d73c30ef96eb21523c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673891"
---
# <span data-ttu-id="5b0e7-101">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="5b0e7-101">Remove-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="5b0e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b0e7-102">SYNOPSIS</span></span>
<span data-ttu-id="5b0e7-103">Elimina un'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="5b0e7-103">Deletes a registration assignment.</span></span>

## <span data-ttu-id="5b0e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b0e7-104">SYNTAX</span></span>

### <span data-ttu-id="5b0e7-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b0e7-105">Default (Default)</span></span>
```
Remove-AzManagedServicesAssignment [[-Scope] <String>] -Id <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0e7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b0e7-106">ByResourceId</span></span>
```
Remove-AzManagedServicesAssignment -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0e7-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5b0e7-107">ByInputObject</span></span>
```
Remove-AzManagedServicesAssignment -InputObject <PSRegistrationAssignment> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b0e7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b0e7-108">DESCRIPTION</span></span>
<span data-ttu-id="5b0e7-109">Elimina un'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="5b0e7-109">Deletes a registration assignment.</span></span>

## <span data-ttu-id="5b0e7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b0e7-110">EXAMPLES</span></span>

### <span data-ttu-id="5b0e7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5b0e7-111">Example 1</span></span>
```powershell
PS C:\Remove-AzManagedServicesAssignment -Id b037e73c-815e-4472-868f-59e51b49b949

Name                                 RegistrationDefinitionId
----                                 ------------------------
b037e73c-815e-4472-868f-59e51b49b949 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/be2f72e6-93e0-4d3f-ac50-9a756ed4ffa7
```

<span data-ttu-id="5b0e7-112">Elimina l'assegnazione di registrazione sotto l'ambito predefinito.</span><span class="sxs-lookup"><span data-stu-id="5b0e7-112">Deletes the registration assignment under the default scope.</span></span>

### <span data-ttu-id="5b0e7-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5b0e7-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzManagedServicesAssignment -ResourceId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationAssignments/88ba878b-9a3c-40c3-80da-015cbe488a2f

Name                                 RegistrationDefinitionId
----                                 ------------------------
88ba878b-9a3c-40c3-80da-015cbe488a2f /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/40be0299-6573-4391-be2f-b41dd4aaf4f9
```

<span data-ttu-id="5b0e7-114">Elimina l'assegnazione di registrazione in base all'ID risorsa completo.</span><span class="sxs-lookup"><span data-stu-id="5b0e7-114">Deletes the registration assignment given the fully qualified resource id.</span></span>

### <span data-ttu-id="5b0e7-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5b0e7-115">Example 3</span></span>
```powershell
PS C:\> $assignment = New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/33974646-9bce-461d-89eb-331f20fca33c
PS C:\> Remove-AzManagedServicesAssignment -InputObject $assignment
```

<span data-ttu-id="5b0e7-116">Elimina l'assegnazione di registrazione usando l'oggetto di input fornito.</span><span class="sxs-lookup"><span data-stu-id="5b0e7-116">Deletes the registration assignment using the input object provided.</span></span>

## <span data-ttu-id="5b0e7-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b0e7-117">PARAMETERS</span></span>

### <span data-ttu-id="5b0e7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b0e7-118">-AsJob</span></span>
<span data-ttu-id="5b0e7-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5b0e7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b0e7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b0e7-120">-DefaultProfile</span></span>
<span data-ttu-id="5b0e7-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b0e7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b0e7-122">-ID</span><span class="sxs-lookup"><span data-stu-id="5b0e7-122">-Id</span></span>
<span data-ttu-id="5b0e7-123">GUID assegnazione registrazione (ad esempio, b0c052e5-c437-4771-A476-8b1201158a57)</span><span class="sxs-lookup"><span data-stu-id="5b0e7-123">The registration assignment GUID (for example, b0c052e5-c437-4771-a476-8b1201158a57)</span></span>
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

### <span data-ttu-id="5b0e7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b0e7-124">-InputObject</span></span>
<span data-ttu-id="5b0e7-125">Oggetto assegnazione registrazione.</span><span class="sxs-lookup"><span data-stu-id="5b0e7-125">The registration assignment object.</span></span>

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

### <span data-ttu-id="5b0e7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b0e7-126">-ResourceId</span></span>
<span data-ttu-id="5b0e7-127">ID di risorsa completo dell'assegnazione di registrazione, ad esempio/subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57.</span><span class="sxs-lookup"><span data-stu-id="5b0e7-127">The fully qualified resource id of the registration assignment (for example, /subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57).</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e7-128">-Ambito</span><span class="sxs-lookup"><span data-stu-id="5b0e7-128">-Scope</span></span>
<span data-ttu-id="5b0e7-129">Ambito in cui deve essere creata l'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="5b0e7-129">The scope where the registration assignment should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e7-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5b0e7-130">-Confirm</span></span>
<span data-ttu-id="5b0e7-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b0e7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b0e7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b0e7-132">-WhatIf</span></span>
<span data-ttu-id="5b0e7-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b0e7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b0e7-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b0e7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b0e7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b0e7-135">CommonParameters</span></span>
<span data-ttu-id="5b0e7-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b0e7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b0e7-137">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b0e7-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b0e7-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b0e7-138">INPUTS</span></span>

### <span data-ttu-id="5b0e7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5b0e7-139">System.String</span></span>

### <span data-ttu-id="5b0e7-140">Microsoft. Azure. PowerShell. Cmdlets. ManagedServices. Models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="5b0e7-140">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>

## <span data-ttu-id="5b0e7-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b0e7-141">OUTPUTS</span></span>

### <span data-ttu-id="5b0e7-142">Microsoft. Azure. PowerShell. Cmdlets. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="5b0e7-142">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="5b0e7-143">Note</span><span class="sxs-lookup"><span data-stu-id="5b0e7-143">NOTES</span></span>

## <span data-ttu-id="5b0e7-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b0e7-144">RELATED LINKS</span></span>
