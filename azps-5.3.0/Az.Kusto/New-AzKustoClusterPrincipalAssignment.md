---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: fafc31700477de968c453002e903b52aa73967d8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476948"
---
# <span data-ttu-id="67d5d-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="67d5d-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="67d5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67d5d-102">SYNOPSIS</span></span>
<span data-ttu-id="67d5d-103">Creare un cluster di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="67d5d-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="67d5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67d5d-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="67d5d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67d5d-105">DESCRIPTION</span></span>
<span data-ttu-id="67d5d-106">Creare un cluster di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="67d5d-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="67d5d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67d5d-107">EXAMPLES</span></span>

### <span data-ttu-id="67d5d-108">Esempio 1: creare un cluster kusto principalAssignment</span><span class="sxs-lookup"><span data-stu-id="67d5d-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="67d5d-109">Il comando precedente crea un cluster kusto principalAssignment</span><span class="sxs-lookup"><span data-stu-id="67d5d-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="67d5d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67d5d-110">PARAMETERS</span></span>

### <span data-ttu-id="67d5d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67d5d-111">-AsJob</span></span>
<span data-ttu-id="67d5d-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="67d5d-112">Run the command as a job</span></span>

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

### <span data-ttu-id="67d5d-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="67d5d-113">-ClusterName</span></span>
<span data-ttu-id="67d5d-114">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="67d5d-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="67d5d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d5d-115">-DefaultProfile</span></span>
<span data-ttu-id="67d5d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67d5d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67d5d-117">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="67d5d-117">-NoWait</span></span>
<span data-ttu-id="67d5d-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="67d5d-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="67d5d-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="67d5d-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="67d5d-120">Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="67d5d-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="67d5d-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="67d5d-121">-PrincipalId</span></span>
<span data-ttu-id="67d5d-122">ID entità assegnato all'entità cluster.</span><span class="sxs-lookup"><span data-stu-id="67d5d-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="67d5d-123">Può essere un nome di posta elettronica, di ID applicazione o di gruppo di sicurezza per l'utente.</span><span class="sxs-lookup"><span data-stu-id="67d5d-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="67d5d-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="67d5d-124">-PrincipalType</span></span>
<span data-ttu-id="67d5d-125">Tipo di entità.</span><span class="sxs-lookup"><span data-stu-id="67d5d-125">Principal type.</span></span>

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

### <span data-ttu-id="67d5d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67d5d-126">-ResourceGroupName</span></span>
<span data-ttu-id="67d5d-127">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="67d5d-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="67d5d-128">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="67d5d-128">-Role</span></span>
<span data-ttu-id="67d5d-129">Ruolo principale del cluster.</span><span class="sxs-lookup"><span data-stu-id="67d5d-129">Cluster principal role.</span></span>

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

### <span data-ttu-id="67d5d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67d5d-130">-SubscriptionId</span></span>
<span data-ttu-id="67d5d-131">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="67d5d-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="67d5d-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="67d5d-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="67d5d-133">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="67d5d-133">-TenantId</span></span>
<span data-ttu-id="67d5d-134">ID tenant dell'entità</span><span class="sxs-lookup"><span data-stu-id="67d5d-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="67d5d-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="67d5d-135">-Confirm</span></span>
<span data-ttu-id="67d5d-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67d5d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67d5d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67d5d-137">-WhatIf</span></span>
<span data-ttu-id="67d5d-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67d5d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67d5d-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67d5d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67d5d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d5d-140">CommonParameters</span></span>
<span data-ttu-id="67d5d-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67d5d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d5d-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67d5d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d5d-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67d5d-143">INPUTS</span></span>

## <span data-ttu-id="67d5d-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67d5d-144">OUTPUTS</span></span>

### <span data-ttu-id="67d5d-145">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200918. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="67d5d-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="67d5d-146">Note</span><span class="sxs-lookup"><span data-stu-id="67d5d-146">NOTES</span></span>

<span data-ttu-id="67d5d-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="67d5d-147">ALIASES</span></span>

## <span data-ttu-id="67d5d-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67d5d-148">RELATED LINKS</span></span>

