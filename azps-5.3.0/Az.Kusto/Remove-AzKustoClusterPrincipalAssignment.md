---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 92d6855753bdf56941d6f6ca85ec021228894a2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476939"
---
# <span data-ttu-id="7f522-101">Remove-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="7f522-101">Remove-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="7f522-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f522-102">SYNOPSIS</span></span>
<span data-ttu-id="7f522-103">Elimina un principalAssignment del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="7f522-103">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="7f522-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f522-104">SYNTAX</span></span>

### <span data-ttu-id="7f522-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7f522-105">Delete (Default)</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7f522-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7f522-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7f522-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f522-107">DESCRIPTION</span></span>
<span data-ttu-id="7f522-108">Elimina un principalAssignment del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="7f522-108">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="7f522-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f522-109">EXAMPLES</span></span>

### <span data-ttu-id="7f522-110">Esempio 1: eliminare un cluster di Kusto esistente PrincipalAssignment per nome</span><span class="sxs-lookup"><span data-stu-id="7f522-110">Example 1: Delete an existing Kusto cluster PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="7f522-111">Il comando precedente elimina il PrincipalAssignment denominato "kustoprincipal1" nel cluster kusto "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="7f522-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto cluster  "testnewkustocluster".</span></span>

## <span data-ttu-id="7f522-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f522-112">PARAMETERS</span></span>

### <span data-ttu-id="7f522-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f522-113">-AsJob</span></span>
<span data-ttu-id="7f522-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="7f522-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7f522-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="7f522-115">-ClusterName</span></span>
<span data-ttu-id="7f522-116">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="7f522-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f522-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f522-117">-DefaultProfile</span></span>
<span data-ttu-id="7f522-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f522-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f522-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f522-119">-InputObject</span></span>
<span data-ttu-id="7f522-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7f522-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f522-121">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="7f522-121">-NoWait</span></span>
<span data-ttu-id="7f522-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="7f522-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7f522-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f522-123">-PassThru</span></span>
<span data-ttu-id="7f522-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="7f522-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7f522-125">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="7f522-125">-PrincipalAssignmentName</span></span>
<span data-ttu-id="7f522-126">Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="7f522-126">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f522-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f522-127">-ResourceGroupName</span></span>
<span data-ttu-id="7f522-128">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="7f522-128">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f522-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7f522-129">-SubscriptionId</span></span>
<span data-ttu-id="7f522-130">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7f522-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7f522-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="7f522-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f522-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7f522-132">-Confirm</span></span>
<span data-ttu-id="7f522-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f522-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f522-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f522-134">-WhatIf</span></span>
<span data-ttu-id="7f522-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f522-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f522-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f522-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f522-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f522-137">CommonParameters</span></span>
<span data-ttu-id="7f522-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f522-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f522-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f522-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f522-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f522-140">INPUTS</span></span>

### <span data-ttu-id="7f522-141">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="7f522-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="7f522-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f522-142">OUTPUTS</span></span>

### <span data-ttu-id="7f522-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f522-143">System.Boolean</span></span>

## <span data-ttu-id="7f522-144">Note</span><span class="sxs-lookup"><span data-stu-id="7f522-144">NOTES</span></span>

<span data-ttu-id="7f522-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7f522-145">ALIASES</span></span>

<span data-ttu-id="7f522-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f522-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7f522-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="7f522-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7f522-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7f522-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7f522-149">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="7f522-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7f522-150">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="7f522-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="7f522-151">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="7f522-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="7f522-152">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="7f522-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="7f522-153">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="7f522-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="7f522-154">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="7f522-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7f522-155">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7f522-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="7f522-156">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="7f522-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="7f522-157">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="7f522-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="7f522-158">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7f522-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7f522-159">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="7f522-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7f522-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f522-160">RELATED LINKS</span></span>

