---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: cd29af9ac8569683e6447a51f4d4f6784139f735
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203778"
---
# <span data-ttu-id="c753a-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="c753a-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="c753a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c753a-102">SYNOPSIS</span></span>
<span data-ttu-id="c753a-103">Elimina un principalAssignment di Kusto.</span><span class="sxs-lookup"><span data-stu-id="c753a-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="c753a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c753a-104">SYNTAX</span></span>

### <span data-ttu-id="c753a-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c753a-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c753a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c753a-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c753a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c753a-107">DESCRIPTION</span></span>
<span data-ttu-id="c753a-108">Elimina un principalAssignment di Kusto.</span><span class="sxs-lookup"><span data-stu-id="c753a-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="c753a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c753a-109">EXAMPLES</span></span>

### <span data-ttu-id="c753a-110">Esempio 1: Eliminare un database PrincipalAssignment esistente di Kusto in base al nome</span><span class="sxs-lookup"><span data-stu-id="c753a-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="c753a-111">Il comando precedente elimina l'assegnazione principale denominata "kustoprincipal1" nel database Kusto "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="c753a-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="c753a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c753a-112">PARAMETERS</span></span>

### <span data-ttu-id="c753a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c753a-113">-AsJob</span></span>
<span data-ttu-id="c753a-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="c753a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="c753a-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c753a-115">-ClusterName</span></span>
<span data-ttu-id="c753a-116">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c753a-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c753a-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c753a-117">-DatabaseName</span></span>
<span data-ttu-id="c753a-118">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c753a-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="c753a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c753a-119">-DefaultProfile</span></span>
<span data-ttu-id="c753a-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c753a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c753a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c753a-121">-InputObject</span></span>
<span data-ttu-id="c753a-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c753a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c753a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c753a-123">-NoWait</span></span>
<span data-ttu-id="c753a-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="c753a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c753a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c753a-125">-PassThru</span></span>
<span data-ttu-id="c753a-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="c753a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c753a-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="c753a-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="c753a-128">Nome del principalAssignment di Kusto.</span><span class="sxs-lookup"><span data-stu-id="c753a-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="c753a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c753a-129">-ResourceGroupName</span></span>
<span data-ttu-id="c753a-130">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c753a-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c753a-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c753a-131">-SubscriptionId</span></span>
<span data-ttu-id="c753a-132">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c753a-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c753a-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c753a-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c753a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c753a-134">-Confirm</span></span>
<span data-ttu-id="c753a-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c753a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c753a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c753a-136">-WhatIf</span></span>
<span data-ttu-id="c753a-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c753a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c753a-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c753a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c753a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c753a-139">CommonParameters</span></span>
<span data-ttu-id="c753a-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c753a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c753a-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c753a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c753a-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="c753a-142">INPUTS</span></span>

### <span data-ttu-id="c753a-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="c753a-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c753a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c753a-144">OUTPUTS</span></span>

### <span data-ttu-id="c753a-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c753a-145">System.Boolean</span></span>

## <span data-ttu-id="c753a-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="c753a-146">NOTES</span></span>

<span data-ttu-id="c753a-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c753a-147">ALIASES</span></span>

<span data-ttu-id="c753a-148">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="c753a-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c753a-149">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c753a-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c753a-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c753a-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c753a-151">INPUTOBJECT <IKustoIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="c753a-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c753a-152">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="c753a-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c753a-153">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c753a-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c753a-154">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="c753a-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c753a-155">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c753a-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c753a-156">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="c753a-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c753a-157">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c753a-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c753a-158">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="c753a-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c753a-159">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c753a-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c753a-160">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c753a-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c753a-161">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c753a-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c753a-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c753a-162">RELATED LINKS</span></span>

