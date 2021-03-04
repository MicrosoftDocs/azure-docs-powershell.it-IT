---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: ab6ef84d05e77711a767f35f915d53c2fe5cdb46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975774"
---
# <span data-ttu-id="8d1b8-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="8d1b8-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="8d1b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d1b8-102">SYNOPSIS</span></span>
<span data-ttu-id="8d1b8-103">Elimina il database con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-103">Deletes the database with the given name.</span></span>

## <span data-ttu-id="8d1b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d1b8-104">SYNTAX</span></span>

### <span data-ttu-id="8d1b8-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8d1b8-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8d1b8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8d1b8-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8d1b8-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8d1b8-107">DESCRIPTION</span></span>
<span data-ttu-id="8d1b8-108">Elimina il database con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-108">Deletes the database with the given name.</span></span>

## <span data-ttu-id="8d1b8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d1b8-109">EXAMPLES</span></span>

### <span data-ttu-id="8d1b8-110">Esempio 1: Eliminare un database Kusto esistente in base al nome</span><span class="sxs-lookup"><span data-stu-id="8d1b8-110">Example 1: Delete an existing Kusto database by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
```

<span data-ttu-id="8d1b8-111">Il comando precedente elimina il database Kusto denominato "mykustodatabase" nel cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="8d1b8-111">The above command deletes the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="8d1b8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d1b8-112">PARAMETERS</span></span>

### <span data-ttu-id="8d1b8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d1b8-113">-AsJob</span></span>
<span data-ttu-id="8d1b8-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="8d1b8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="8d1b8-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8d1b8-115">-ClusterName</span></span>
<span data-ttu-id="8d1b8-116">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="8d1b8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d1b8-117">-DefaultProfile</span></span>
<span data-ttu-id="8d1b8-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d1b8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d1b8-119">-InputObject</span></span>
<span data-ttu-id="8d1b8-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8d1b8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8d1b8-121">-Name</span></span>
<span data-ttu-id="8d1b8-122">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-122">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d1b8-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8d1b8-123">-NoWait</span></span>
<span data-ttu-id="8d1b8-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="8d1b8-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8d1b8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d1b8-125">-PassThru</span></span>
<span data-ttu-id="8d1b8-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="8d1b8-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8d1b8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d1b8-127">-ResourceGroupName</span></span>
<span data-ttu-id="8d1b8-128">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="8d1b8-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d1b8-129">-SubscriptionId</span></span>
<span data-ttu-id="8d1b8-130">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8d1b8-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8d1b8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d1b8-132">-Confirm</span></span>
<span data-ttu-id="8d1b8-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d1b8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d1b8-134">-WhatIf</span></span>
<span data-ttu-id="8d1b8-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d1b8-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d1b8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d1b8-137">CommonParameters</span></span>
<span data-ttu-id="8d1b8-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d1b8-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d1b8-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="8d1b8-140">INPUTS</span></span>

### <span data-ttu-id="8d1b8-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="8d1b8-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="8d1b8-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d1b8-142">OUTPUTS</span></span>

### <span data-ttu-id="8d1b8-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8d1b8-143">System.Boolean</span></span>

## <span data-ttu-id="8d1b8-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="8d1b8-144">NOTES</span></span>

<span data-ttu-id="8d1b8-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8d1b8-145">ALIASES</span></span>

<span data-ttu-id="8d1b8-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="8d1b8-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8d1b8-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d1b8-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8d1b8-149">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="8d1b8-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8d1b8-150">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="8d1b8-151">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="8d1b8-152">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="8d1b8-153">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="8d1b8-154">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="8d1b8-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8d1b8-155">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="8d1b8-156">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="8d1b8-157">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="8d1b8-158">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8d1b8-159">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="8d1b8-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8d1b8-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d1b8-160">RELATED LINKS</span></span>

