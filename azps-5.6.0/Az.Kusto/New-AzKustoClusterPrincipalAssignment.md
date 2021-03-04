---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 738f0d4b4033dd7cccdc0fbabe94d2dfde9779c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959549"
---
# <span data-ttu-id="394d4-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="394d4-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="394d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="394d4-102">SYNOPSIS</span></span>
<span data-ttu-id="394d4-103">Creare un principalAssignment cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="394d4-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="394d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="394d4-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="394d4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="394d4-105">DESCRIPTION</span></span>
<span data-ttu-id="394d4-106">Creare un principalAssignment cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="394d4-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="394d4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="394d4-107">EXAMPLES</span></span>

### <span data-ttu-id="394d4-108">Esempio 1: Creare un principalAssignment cluster kusto</span><span class="sxs-lookup"><span data-stu-id="394d4-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="394d4-109">Il comando precedente crea un principalAssignment cluster Kusto</span><span class="sxs-lookup"><span data-stu-id="394d4-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="394d4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="394d4-110">PARAMETERS</span></span>

### <span data-ttu-id="394d4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="394d4-111">-AsJob</span></span>
<span data-ttu-id="394d4-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="394d4-112">Run the command as a job</span></span>

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

### <span data-ttu-id="394d4-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="394d4-113">-ClusterName</span></span>
<span data-ttu-id="394d4-114">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="394d4-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="394d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="394d4-115">-DefaultProfile</span></span>
<span data-ttu-id="394d4-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="394d4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="394d4-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="394d4-117">-NoWait</span></span>
<span data-ttu-id="394d4-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="394d4-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="394d4-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="394d4-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="394d4-120">Nome del principalAssignment di Kusto.</span><span class="sxs-lookup"><span data-stu-id="394d4-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="394d4-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="394d4-121">-PrincipalId</span></span>
<span data-ttu-id="394d4-122">ID entità assegnato all'entità cluster.</span><span class="sxs-lookup"><span data-stu-id="394d4-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="394d4-123">Può trattarsi di un messaggio di posta elettronica dell'utente, un ID applicazione o il nome di un gruppo di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="394d4-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="394d4-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="394d4-124">-PrincipalType</span></span>
<span data-ttu-id="394d4-125">Tipo di entità.</span><span class="sxs-lookup"><span data-stu-id="394d4-125">Principal type.</span></span>

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

### <span data-ttu-id="394d4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="394d4-126">-ResourceGroupName</span></span>
<span data-ttu-id="394d4-127">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="394d4-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="394d4-128">-Role</span><span class="sxs-lookup"><span data-stu-id="394d4-128">-Role</span></span>
<span data-ttu-id="394d4-129">Ruolo principale del cluster.</span><span class="sxs-lookup"><span data-stu-id="394d4-129">Cluster principal role.</span></span>

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

### <span data-ttu-id="394d4-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="394d4-130">-SubscriptionId</span></span>
<span data-ttu-id="394d4-131">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="394d4-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="394d4-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="394d4-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="394d4-133">-TenantId</span><span class="sxs-lookup"><span data-stu-id="394d4-133">-TenantId</span></span>
<span data-ttu-id="394d4-134">ID tenant dell'entità</span><span class="sxs-lookup"><span data-stu-id="394d4-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="394d4-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="394d4-135">-Confirm</span></span>
<span data-ttu-id="394d4-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="394d4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="394d4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="394d4-137">-WhatIf</span></span>
<span data-ttu-id="394d4-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="394d4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="394d4-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="394d4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="394d4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="394d4-140">CommonParameters</span></span>
<span data-ttu-id="394d4-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="394d4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="394d4-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="394d4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="394d4-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="394d4-143">INPUTS</span></span>

## <span data-ttu-id="394d4-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="394d4-144">OUTPUTS</span></span>

### <span data-ttu-id="394d4-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="394d4-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="394d4-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="394d4-146">NOTES</span></span>

<span data-ttu-id="394d4-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="394d4-147">ALIASES</span></span>

## <span data-ttu-id="394d4-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="394d4-148">RELATED LINKS</span></span>

