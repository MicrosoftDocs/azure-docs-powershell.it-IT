---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 12e43eeb22151df8569e068933036fe29749ed1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194270"
---
# <span data-ttu-id="b13c7-101">Remove-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="b13c7-101">Remove-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="b13c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b13c7-102">SYNOPSIS</span></span>
<span data-ttu-id="b13c7-103">Rimuovere le autorizzazioni delle entità di database.</span><span class="sxs-lookup"><span data-stu-id="b13c7-103">Remove Database principals permissions.</span></span>

## <span data-ttu-id="b13c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b13c7-104">SYNTAX</span></span>

### <span data-ttu-id="b13c7-105">RemoveExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b13c7-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b13c7-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b13c7-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b13c7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b13c7-107">DESCRIPTION</span></span>
<span data-ttu-id="b13c7-108">Rimuovere le autorizzazioni delle entità di database.</span><span class="sxs-lookup"><span data-stu-id="b13c7-108">Remove Database principals permissions.</span></span>

## <span data-ttu-id="b13c7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b13c7-109">EXAMPLES</span></span>

### <span data-ttu-id="b13c7-110">Esempio 1: Rimuovere le autorizzazioni delle entità di database</span><span class="sxs-lookup"><span data-stu-id="b13c7-110">Example 1: Remove Database principals permissions</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="b13c7-111">Il comando precedente rimuove le autorizzazioni entità database</span><span class="sxs-lookup"><span data-stu-id="b13c7-111">The above command removes Database principals permissions</span></span>

## <span data-ttu-id="b13c7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b13c7-112">PARAMETERS</span></span>

### <span data-ttu-id="b13c7-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b13c7-113">-ClusterName</span></span>
<span data-ttu-id="b13c7-114">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="b13c7-114">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13c7-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b13c7-115">-DatabaseName</span></span>
<span data-ttu-id="b13c7-116">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="b13c7-116">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b13c7-117">-DefaultProfile</span></span>
<span data-ttu-id="b13c7-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b13c7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b13c7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b13c7-119">-InputObject</span></span>
<span data-ttu-id="b13c7-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b13c7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: RemoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b13c7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b13c7-121">-ResourceGroupName</span></span>
<span data-ttu-id="b13c7-122">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="b13c7-122">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13c7-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b13c7-123">-SubscriptionId</span></span>
<span data-ttu-id="b13c7-124">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b13c7-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b13c7-125">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b13c7-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13c7-126">-Value</span><span class="sxs-lookup"><span data-stu-id="b13c7-126">-Value</span></span>
<span data-ttu-id="b13c7-127">Elenco delle entità database Kusto.</span><span class="sxs-lookup"><span data-stu-id="b13c7-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="b13c7-128">Per creare, vedere la sezione NOTE relativa alle proprietà VALUE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b13c7-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13c7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b13c7-129">-Confirm</span></span>
<span data-ttu-id="b13c7-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b13c7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b13c7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b13c7-131">-WhatIf</span></span>
<span data-ttu-id="b13c7-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b13c7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b13c7-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b13c7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b13c7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b13c7-134">CommonParameters</span></span>
<span data-ttu-id="b13c7-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b13c7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b13c7-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b13c7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b13c7-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="b13c7-137">INPUTS</span></span>

### <span data-ttu-id="b13c7-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="b13c7-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="b13c7-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b13c7-139">OUTPUTS</span></span>

### <span data-ttu-id="b13c7-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="b13c7-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="b13c7-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="b13c7-141">NOTES</span></span>

<span data-ttu-id="b13c7-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b13c7-142">ALIASES</span></span>

<span data-ttu-id="b13c7-143">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b13c7-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b13c7-144">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b13c7-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b13c7-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b13c7-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b13c7-146">INPUTOBJECT <IKustoIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="b13c7-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b13c7-147">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="b13c7-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="b13c7-148">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="b13c7-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="b13c7-149">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="b13c7-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="b13c7-150">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="b13c7-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="b13c7-151">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b13c7-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b13c7-152">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b13c7-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="b13c7-153">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="b13c7-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="b13c7-154">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="b13c7-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="b13c7-155">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b13c7-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b13c7-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b13c7-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="b13c7-157">VALUE <IDatabasePrincipal[]>: elenco delle entità database Kusto.</span><span class="sxs-lookup"><span data-stu-id="b13c7-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="b13c7-158">`Name <String>`: nome dell'entità database.</span><span class="sxs-lookup"><span data-stu-id="b13c7-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="b13c7-159">`Role <DatabasePrincipalRole>`: ruolo principale del database.</span><span class="sxs-lookup"><span data-stu-id="b13c7-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="b13c7-160">`Type <DatabasePrincipalType>`: tipo di entità database.</span><span class="sxs-lookup"><span data-stu-id="b13c7-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="b13c7-161">`[AppId <String>]`: ID applicazione- pertinente solo per il tipo di entità applicazione.</span><span class="sxs-lookup"><span data-stu-id="b13c7-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="b13c7-162">`[Email <String>]`: messaggio di posta elettronica dell'entità database, se esistente.</span><span class="sxs-lookup"><span data-stu-id="b13c7-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="b13c7-163">`[Fqn <String>]`: nome completo dell'entità database.</span><span class="sxs-lookup"><span data-stu-id="b13c7-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="b13c7-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b13c7-164">RELATED LINKS</span></span>

