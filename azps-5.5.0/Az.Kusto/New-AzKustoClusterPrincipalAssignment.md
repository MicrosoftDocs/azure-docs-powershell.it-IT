---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: fafc31700477de968c453002e903b52aa73967d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209234"
---
# <span data-ttu-id="e5b8f-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="e5b8f-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="e5b8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b8f-103">Creare un principalAssignment cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e5b8f-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="e5b8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5b8f-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e5b8f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e5b8f-105">DESCRIPTION</span></span>
<span data-ttu-id="e5b8f-106">Creare un principalAssignment cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e5b8f-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="e5b8f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5b8f-107">EXAMPLES</span></span>

### <span data-ttu-id="e5b8f-108">Esempio 1: Creare un'assegnazione principalAssignment cluster kusto</span><span class="sxs-lookup"><span data-stu-id="e5b8f-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="e5b8f-109">Il comando precedente crea un'entità cluster Kusto principalAssignment</span><span class="sxs-lookup"><span data-stu-id="e5b8f-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="e5b8f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5b8f-110">PARAMETERS</span></span>

### <span data-ttu-id="e5b8f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5b8f-111">-AsJob</span></span>
<span data-ttu-id="e5b8f-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="e5b8f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e5b8f-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e5b8f-113">-ClusterName</span></span>
<span data-ttu-id="e5b8f-114">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e5b8f-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e5b8f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5b8f-115">-DefaultProfile</span></span>
<span data-ttu-id="e5b8f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5b8f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5b8f-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e5b8f-117">-NoWait</span></span>
<span data-ttu-id="e5b8f-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="e5b8f-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e5b8f-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="e5b8f-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="e5b8f-120">Nome del principalAssignment di Kusto.</span><span class="sxs-lookup"><span data-stu-id="e5b8f-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="e5b8f-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="e5b8f-121">-PrincipalId</span></span>
<span data-ttu-id="e5b8f-122">ID entità assegnato all'entità cluster.</span><span class="sxs-lookup"><span data-stu-id="e5b8f-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="e5b8f-123">Può trattarsi di un indirizzo di posta elettronica dell'utente, un ID applicazione o il nome di un gruppo di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e5b8f-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="e5b8f-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="e5b8f-124">-PrincipalType</span></span>
<span data-ttu-id="e5b8f-125">Tipo di entità.</span><span class="sxs-lookup"><span data-stu-id="e5b8f-125">Principal type.</span></span>

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

### <span data-ttu-id="e5b8f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5b8f-126">-ResourceGroupName</span></span>
<span data-ttu-id="e5b8f-127">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e5b8f-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e5b8f-128">-Role</span><span class="sxs-lookup"><span data-stu-id="e5b8f-128">-Role</span></span>
<span data-ttu-id="e5b8f-129">Ruolo principale del cluster.</span><span class="sxs-lookup"><span data-stu-id="e5b8f-129">Cluster principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.ClusterPrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5b8f-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5b8f-130">-SubscriptionId</span></span>
<span data-ttu-id="e5b8f-131">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e5b8f-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e5b8f-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e5b8f-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e5b8f-133">-TenantId</span><span class="sxs-lookup"><span data-stu-id="e5b8f-133">-TenantId</span></span>
<span data-ttu-id="e5b8f-134">ID tenant dell'entità</span><span class="sxs-lookup"><span data-stu-id="e5b8f-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="e5b8f-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5b8f-135">-Confirm</span></span>
<span data-ttu-id="e5b8f-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5b8f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5b8f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5b8f-137">-WhatIf</span></span>
<span data-ttu-id="e5b8f-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5b8f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5b8f-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5b8f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5b8f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5b8f-140">CommonParameters</span></span>
<span data-ttu-id="e5b8f-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5b8f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5b8f-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e5b8f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5b8f-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="e5b8f-143">INPUTS</span></span>

## <span data-ttu-id="e5b8f-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5b8f-144">OUTPUTS</span></span>

### <span data-ttu-id="e5b8f-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="e5b8f-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="e5b8f-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="e5b8f-146">NOTES</span></span>

<span data-ttu-id="e5b8f-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e5b8f-147">ALIASES</span></span>

## <span data-ttu-id="e5b8f-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5b8f-148">RELATED LINKS</span></span>

