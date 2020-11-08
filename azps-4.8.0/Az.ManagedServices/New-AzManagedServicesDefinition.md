---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: 6c9c4b562acbf80dba9b1b414345d5eb8e3ecc60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191488"
---
# <span data-ttu-id="3dcf2-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="3dcf2-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="3dcf2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3dcf2-102">SYNOPSIS</span></span>
<span data-ttu-id="3dcf2-103">Crea o aggiorna una definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="3dcf2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dcf2-104">SYNTAX</span></span>

### <span data-ttu-id="3dcf2-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3dcf2-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dcf2-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="3dcf2-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] -PlanName <String>
 -PlanPublisher <String> -PlanProduct <String> -PlanVersion <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dcf2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dcf2-107">DESCRIPTION</span></span>
<span data-ttu-id="3dcf2-108">Crea o aggiorna una definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-108">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="3dcf2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dcf2-109">EXAMPLES</span></span>

### <span data-ttu-id="3dcf2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3dcf2-110">Example 1</span></span>
```powershell
PS C:\> PS C:\> New-AzManagedServicesDefinition -Name name -ManagedByTenantId bab3375b-6197-4a15-a44b-16c41faa91d7 -PrincipalId d6f6c88a-5b7a-455e-ba40-ce146d4d3671 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -Description mydef

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fdad02a1-a715-4352-844f-2923233590da bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="3dcf2-111">Crea o aggiorna una definizione di registrazione in base ai parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-111">Creates or updates a registration definition given the required parameters.</span></span>

### <span data-ttu-id="3dcf2-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3dcf2-112">Example 2</span></span>
```powershell
PS C> New-AzManagedServicesDefinition -Name asd -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7" -PlanName plan -PlanPublisher publisher -PlanProduct product -PlanVersion 0.1

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
8cde7c19-1750-468e-973e-b711549edc35 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="3dcf2-113">Crea o aggiorna una definizione di registrazione con i dettagli del piano.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-113">Creates or updates a registration definition with the plan details.</span></span>

## <span data-ttu-id="3dcf2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3dcf2-114">PARAMETERS</span></span>

### <span data-ttu-id="3dcf2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3dcf2-115">-AsJob</span></span>
<span data-ttu-id="3dcf2-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3dcf2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3dcf2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dcf2-117">-DefaultProfile</span></span>
<span data-ttu-id="3dcf2-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dcf2-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dcf2-119">-Description</span></span>
<span data-ttu-id="3dcf2-120">Descrizione della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-120">The description of the Registration Definition.</span></span>

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

### <span data-ttu-id="3dcf2-121">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="3dcf2-121">-ManagedByTenantId</span></span>
<span data-ttu-id="3dcf2-122">Identificatore del tenant di ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-122">The ManagedBy Tenant Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf2-123">-PlanName</span><span class="sxs-lookup"><span data-stu-id="3dcf2-123">-PlanName</span></span>
<span data-ttu-id="3dcf2-124">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-124">The name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf2-125">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="3dcf2-125">-PlanProduct</span></span>
<span data-ttu-id="3dcf2-126">Nome del prodotto.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-126">The name of the Product.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf2-127">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="3dcf2-127">-PlanPublisher</span></span>
<span data-ttu-id="3dcf2-128">Nome del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-128">The name of the Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf2-129">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="3dcf2-129">-PlanVersion</span></span>
<span data-ttu-id="3dcf2-130">Numero di versione del piano.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-130">The version number of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf2-131">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="3dcf2-131">-PrincipalId</span></span>
<span data-ttu-id="3dcf2-132">Identificatore principale di ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-132">The ManagedBy Principal Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf2-133">-RegistrationDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3dcf2-133">-RegistrationDefinitionName</span></span>
<span data-ttu-id="3dcf2-134">Nome della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-134">The name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf2-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="3dcf2-135">-RoleDefinitionId</span></span>
<span data-ttu-id="3dcf2-136">Identificatore del ruolo del provider del servizio gestito.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-136">The Managed Service Provider's Role Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dcf2-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3dcf2-137">-Confirm</span></span>
<span data-ttu-id="3dcf2-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dcf2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dcf2-139">-WhatIf</span></span>
<span data-ttu-id="3dcf2-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dcf2-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dcf2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dcf2-142">CommonParameters</span></span>
<span data-ttu-id="3dcf2-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dcf2-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dcf2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dcf2-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3dcf2-145">INPUTS</span></span>

### <span data-ttu-id="3dcf2-146">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3dcf2-146">None</span></span>

## <span data-ttu-id="3dcf2-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dcf2-147">OUTPUTS</span></span>

### <span data-ttu-id="3dcf2-148">Microsoft. Azure. PowerShell. Cmdlets. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="3dcf2-148">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="3dcf2-149">Note</span><span class="sxs-lookup"><span data-stu-id="3dcf2-149">NOTES</span></span>

## <span data-ttu-id="3dcf2-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dcf2-150">RELATED LINKS</span></span>