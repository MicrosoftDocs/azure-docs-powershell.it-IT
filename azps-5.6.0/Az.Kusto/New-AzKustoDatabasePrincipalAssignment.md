---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 9fd729a85babf1440516c52f0e7737f4c0d0d281
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970686"
---
# <span data-ttu-id="4c512-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="4c512-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="4c512-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c512-102">SYNOPSIS</span></span>
<span data-ttu-id="4c512-103">Crea un principalAssignment del database cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="4c512-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="4c512-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c512-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4c512-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4c512-105">DESCRIPTION</span></span>
<span data-ttu-id="4c512-106">Crea un'entità database cluster Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="4c512-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="4c512-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c512-107">EXAMPLES</span></span>

### <span data-ttu-id="4c512-108">Esempio 1: Creare un'entità database cluster Kusto principalAssignment</span><span class="sxs-lookup"><span data-stu-id="4c512-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="4c512-109">Il comando precedente crea un'entità database cluster Kusto principalAssignment</span><span class="sxs-lookup"><span data-stu-id="4c512-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="4c512-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c512-110">PARAMETERS</span></span>

### <span data-ttu-id="4c512-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c512-111">-AsJob</span></span>
<span data-ttu-id="4c512-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="4c512-112">Run the command as a job</span></span>

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

### <span data-ttu-id="4c512-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4c512-113">-ClusterName</span></span>
<span data-ttu-id="4c512-114">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="4c512-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="4c512-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4c512-115">-DatabaseName</span></span>
<span data-ttu-id="4c512-116">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="4c512-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="4c512-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c512-117">-DefaultProfile</span></span>
<span data-ttu-id="4c512-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c512-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c512-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4c512-119">-NoWait</span></span>
<span data-ttu-id="4c512-120">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="4c512-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4c512-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="4c512-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="4c512-122">Nome del principalAssignment di Kusto.</span><span class="sxs-lookup"><span data-stu-id="4c512-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="4c512-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="4c512-123">-PrincipalId</span></span>
<span data-ttu-id="4c512-124">ID entità assegnato all'entità database.</span><span class="sxs-lookup"><span data-stu-id="4c512-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="4c512-125">Può trattarsi di un messaggio di posta elettronica dell'utente, un ID applicazione o il nome di un gruppo di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="4c512-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="4c512-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="4c512-126">-PrincipalType</span></span>
<span data-ttu-id="4c512-127">Tipo di entità.</span><span class="sxs-lookup"><span data-stu-id="4c512-127">Principal type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.PrincipalType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c512-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c512-128">-ResourceGroupName</span></span>
<span data-ttu-id="4c512-129">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="4c512-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="4c512-130">-Role</span><span class="sxs-lookup"><span data-stu-id="4c512-130">-Role</span></span>
<span data-ttu-id="4c512-131">Ruolo principale del database.</span><span class="sxs-lookup"><span data-stu-id="4c512-131">Database principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DatabasePrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c512-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4c512-132">-SubscriptionId</span></span>
<span data-ttu-id="4c512-133">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4c512-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4c512-134">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="4c512-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c512-135">-TenantId</span><span class="sxs-lookup"><span data-stu-id="4c512-135">-TenantId</span></span>
<span data-ttu-id="4c512-136">ID tenant dell'entità</span><span class="sxs-lookup"><span data-stu-id="4c512-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="4c512-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c512-137">-Confirm</span></span>
<span data-ttu-id="4c512-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c512-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c512-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c512-139">-WhatIf</span></span>
<span data-ttu-id="4c512-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c512-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c512-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c512-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c512-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c512-142">CommonParameters</span></span>
<span data-ttu-id="4c512-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c512-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c512-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4c512-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c512-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="4c512-145">INPUTS</span></span>

## <span data-ttu-id="4c512-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c512-146">OUTPUTS</span></span>

### <span data-ttu-id="4c512-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="4c512-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="4c512-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="4c512-148">NOTES</span></span>

<span data-ttu-id="4c512-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4c512-149">ALIASES</span></span>

## <span data-ttu-id="4c512-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c512-150">RELATED LINKS</span></span>

