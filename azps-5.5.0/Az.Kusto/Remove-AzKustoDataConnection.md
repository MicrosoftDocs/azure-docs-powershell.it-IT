---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: c04cbc2a92e6fa80c718cb32d95cc4059e4e3a6d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194287"
---
# <span data-ttu-id="bcdaf-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="bcdaf-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="bcdaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcdaf-102">SYNOPSIS</span></span>
<span data-ttu-id="bcdaf-103">Elimina la connessione dati con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="bcdaf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcdaf-104">SYNTAX</span></span>

### <span data-ttu-id="bcdaf-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bcdaf-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bcdaf-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bcdaf-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bcdaf-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bcdaf-107">DESCRIPTION</span></span>
<span data-ttu-id="bcdaf-108">Elimina la connessione dati con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="bcdaf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcdaf-109">EXAMPLES</span></span>

### <span data-ttu-id="bcdaf-110">Esempio 1: Eliminare una connessione dati esistente in base al nome</span><span class="sxs-lookup"><span data-stu-id="bcdaf-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="bcdaf-111">Il comando precedente elimina la connessione dati denominata "mykustodataconnection" nel database "mykustodatabase" del cluster esistente "testnewkustocluster" nel gruppo di risorse "testrg"</span><span class="sxs-lookup"><span data-stu-id="bcdaf-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="bcdaf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcdaf-112">PARAMETERS</span></span>

### <span data-ttu-id="bcdaf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcdaf-113">-AsJob</span></span>
<span data-ttu-id="bcdaf-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="bcdaf-114">Run the command as a job</span></span>

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

### <span data-ttu-id="bcdaf-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bcdaf-115">-ClusterName</span></span>
<span data-ttu-id="bcdaf-116">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="bcdaf-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bcdaf-117">-DatabaseName</span></span>
<span data-ttu-id="bcdaf-118">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="bcdaf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcdaf-119">-DefaultProfile</span></span>
<span data-ttu-id="bcdaf-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcdaf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcdaf-121">-InputObject</span></span>
<span data-ttu-id="bcdaf-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bcdaf-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bcdaf-123">-Name</span></span>
<span data-ttu-id="bcdaf-124">Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-124">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdaf-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bcdaf-125">-NoWait</span></span>
<span data-ttu-id="bcdaf-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="bcdaf-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bcdaf-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcdaf-127">-PassThru</span></span>
<span data-ttu-id="bcdaf-128">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="bcdaf-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bcdaf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcdaf-129">-ResourceGroupName</span></span>
<span data-ttu-id="bcdaf-130">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="bcdaf-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bcdaf-131">-SubscriptionId</span></span>
<span data-ttu-id="bcdaf-132">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bcdaf-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bcdaf-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcdaf-134">-Confirm</span></span>
<span data-ttu-id="bcdaf-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcdaf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcdaf-136">-WhatIf</span></span>
<span data-ttu-id="bcdaf-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcdaf-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcdaf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcdaf-139">CommonParameters</span></span>
<span data-ttu-id="bcdaf-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcdaf-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcdaf-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="bcdaf-142">INPUTS</span></span>

### <span data-ttu-id="bcdaf-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="bcdaf-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="bcdaf-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcdaf-144">OUTPUTS</span></span>

### <span data-ttu-id="bcdaf-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bcdaf-145">System.Boolean</span></span>

## <span data-ttu-id="bcdaf-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="bcdaf-146">NOTES</span></span>

<span data-ttu-id="bcdaf-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bcdaf-147">ALIASES</span></span>

<span data-ttu-id="bcdaf-148">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="bcdaf-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bcdaf-149">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bcdaf-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bcdaf-151">INPUTOBJECT <IKustoIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="bcdaf-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bcdaf-152">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="bcdaf-153">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="bcdaf-154">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="bcdaf-155">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="bcdaf-156">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="bcdaf-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bcdaf-157">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="bcdaf-158">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="bcdaf-159">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="bcdaf-160">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bcdaf-161">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="bcdaf-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bcdaf-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcdaf-162">RELATED LINKS</span></span>

