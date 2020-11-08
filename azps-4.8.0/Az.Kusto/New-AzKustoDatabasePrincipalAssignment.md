---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 8bfcb3a96ee8db53a6a869a01441739ee9c503bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189647"
---
# <span data-ttu-id="f62e9-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="f62e9-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="f62e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f62e9-102">SYNOPSIS</span></span>
<span data-ttu-id="f62e9-103">Crea un database di Kusto cluster principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f62e9-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="f62e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f62e9-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f62e9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f62e9-105">DESCRIPTION</span></span>
<span data-ttu-id="f62e9-106">Crea un database di Kusto cluster principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f62e9-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="f62e9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f62e9-107">EXAMPLES</span></span>

### <span data-ttu-id="f62e9-108">Esempio 1: creare un database di cluster kusto principalAssignment</span><span class="sxs-lookup"><span data-stu-id="f62e9-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="f62e9-109">Il comando precedente crea un database di cluster kusto principalAssignment</span><span class="sxs-lookup"><span data-stu-id="f62e9-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="f62e9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f62e9-110">PARAMETERS</span></span>

### <span data-ttu-id="f62e9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f62e9-111">-AsJob</span></span>
<span data-ttu-id="f62e9-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="f62e9-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f62e9-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="f62e9-113">-ClusterName</span></span>
<span data-ttu-id="f62e9-114">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="f62e9-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f62e9-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f62e9-115">-DatabaseName</span></span>
<span data-ttu-id="f62e9-116">Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="f62e9-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="f62e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f62e9-117">-DefaultProfile</span></span>
<span data-ttu-id="f62e9-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f62e9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f62e9-119">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="f62e9-119">-NoWait</span></span>
<span data-ttu-id="f62e9-120">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="f62e9-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f62e9-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="f62e9-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="f62e9-122">Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="f62e9-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="f62e9-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="f62e9-123">-PrincipalId</span></span>
<span data-ttu-id="f62e9-124">ID entità assegnato all'entità di database.</span><span class="sxs-lookup"><span data-stu-id="f62e9-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="f62e9-125">Può essere un nome di posta elettronica, di ID applicazione o di gruppo di sicurezza per l'utente.</span><span class="sxs-lookup"><span data-stu-id="f62e9-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="f62e9-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="f62e9-126">-PrincipalType</span></span>
<span data-ttu-id="f62e9-127">Tipo di entità.</span><span class="sxs-lookup"><span data-stu-id="f62e9-127">Principal type.</span></span>

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

### <span data-ttu-id="f62e9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f62e9-128">-ResourceGroupName</span></span>
<span data-ttu-id="f62e9-129">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="f62e9-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f62e9-130">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="f62e9-130">-Role</span></span>
<span data-ttu-id="f62e9-131">Ruolo principale del database.</span><span class="sxs-lookup"><span data-stu-id="f62e9-131">Database principal role.</span></span>

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

### <span data-ttu-id="f62e9-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f62e9-132">-SubscriptionId</span></span>
<span data-ttu-id="f62e9-133">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f62e9-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f62e9-134">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f62e9-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f62e9-135">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="f62e9-135">-TenantId</span></span>
<span data-ttu-id="f62e9-136">ID tenant dell'entità</span><span class="sxs-lookup"><span data-stu-id="f62e9-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="f62e9-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f62e9-137">-Confirm</span></span>
<span data-ttu-id="f62e9-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f62e9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f62e9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f62e9-139">-WhatIf</span></span>
<span data-ttu-id="f62e9-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f62e9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f62e9-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f62e9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f62e9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f62e9-142">CommonParameters</span></span>
<span data-ttu-id="f62e9-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f62e9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f62e9-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f62e9-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f62e9-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f62e9-145">INPUTS</span></span>

## <span data-ttu-id="f62e9-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f62e9-146">OUTPUTS</span></span>

### <span data-ttu-id="f62e9-147">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="f62e9-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="f62e9-148">Note</span><span class="sxs-lookup"><span data-stu-id="f62e9-148">NOTES</span></span>

<span data-ttu-id="f62e9-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f62e9-149">ALIASES</span></span>

## <span data-ttu-id="f62e9-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f62e9-150">RELATED LINKS</span></span>
