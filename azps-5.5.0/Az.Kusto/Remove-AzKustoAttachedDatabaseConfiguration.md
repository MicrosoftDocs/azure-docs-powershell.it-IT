---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 9d38b9c3297dc950cc12d46189bc940e27877d8a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187631"
---
# <span data-ttu-id="61a5b-101">Remove-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="61a5b-101">Remove-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="61a5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="61a5b-103">Elimina la configurazione di database allegata con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="61a5b-103">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="61a5b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61a5b-104">SYNTAX</span></span>

### <span data-ttu-id="61a5b-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61a5b-105">Delete (Default)</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="61a5b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="61a5b-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="61a5b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="61a5b-107">DESCRIPTION</span></span>
<span data-ttu-id="61a5b-108">Elimina la configurazione di database allegata con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="61a5b-108">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="61a5b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61a5b-109">EXAMPLES</span></span>

### <span data-ttu-id="61a5b-110">Esempio 1: Eliminare una attachedDatabaseConfiguration esistente in base al nome</span><span class="sxs-lookup"><span data-stu-id="61a5b-110">Example 1: Delete an existing AttachedDatabaseConfiguration by name</span></span>
```powershell
PS C:\> Remove-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration"
```

<span data-ttu-id="61a5b-111">Il comando precedente elimina il database di follower definito in AttachedDatabaseConfiguration "myfollowerconfiguration" dal cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="61a5b-111">The above command deletes the follower database defined in the AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="61a5b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61a5b-112">PARAMETERS</span></span>

### <span data-ttu-id="61a5b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61a5b-113">-AsJob</span></span>
<span data-ttu-id="61a5b-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="61a5b-114">Run the command as a job</span></span>

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

### <span data-ttu-id="61a5b-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="61a5b-115">-ClusterName</span></span>
<span data-ttu-id="61a5b-116">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="61a5b-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="61a5b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a5b-117">-DefaultProfile</span></span>
<span data-ttu-id="61a5b-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61a5b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61a5b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61a5b-119">-InputObject</span></span>
<span data-ttu-id="61a5b-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="61a5b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="61a5b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="61a5b-121">-Name</span></span>
<span data-ttu-id="61a5b-122">Nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="61a5b-122">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a5b-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="61a5b-123">-NoWait</span></span>
<span data-ttu-id="61a5b-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="61a5b-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="61a5b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61a5b-125">-PassThru</span></span>
<span data-ttu-id="61a5b-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="61a5b-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="61a5b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61a5b-127">-ResourceGroupName</span></span>
<span data-ttu-id="61a5b-128">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="61a5b-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="61a5b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="61a5b-129">-SubscriptionId</span></span>
<span data-ttu-id="61a5b-130">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="61a5b-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="61a5b-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="61a5b-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="61a5b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61a5b-132">-Confirm</span></span>
<span data-ttu-id="61a5b-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61a5b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61a5b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61a5b-134">-WhatIf</span></span>
<span data-ttu-id="61a5b-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61a5b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61a5b-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61a5b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61a5b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a5b-137">CommonParameters</span></span>
<span data-ttu-id="61a5b-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61a5b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a5b-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61a5b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a5b-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="61a5b-140">INPUTS</span></span>

### <span data-ttu-id="61a5b-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="61a5b-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="61a5b-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61a5b-142">OUTPUTS</span></span>

### <span data-ttu-id="61a5b-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="61a5b-143">System.Boolean</span></span>

## <span data-ttu-id="61a5b-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="61a5b-144">NOTES</span></span>

<span data-ttu-id="61a5b-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="61a5b-145">ALIASES</span></span>

<span data-ttu-id="61a5b-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="61a5b-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="61a5b-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="61a5b-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="61a5b-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="61a5b-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="61a5b-149">INPUTOBJECT <IKustoIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="61a5b-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="61a5b-150">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="61a5b-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="61a5b-151">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="61a5b-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="61a5b-152">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="61a5b-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="61a5b-153">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="61a5b-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="61a5b-154">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="61a5b-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="61a5b-155">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="61a5b-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="61a5b-156">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="61a5b-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="61a5b-157">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="61a5b-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="61a5b-158">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="61a5b-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="61a5b-159">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="61a5b-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="61a5b-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61a5b-160">RELATED LINKS</span></span>

