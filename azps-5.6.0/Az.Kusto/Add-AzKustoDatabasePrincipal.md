---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/add-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
ms.openlocfilehash: c01d481b5ee9351de0b099a144a709c89a3990ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964574"
---
# <span data-ttu-id="5b774-101">Add-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="5b774-101">Add-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="5b774-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b774-102">SYNOPSIS</span></span>
<span data-ttu-id="5b774-103">Aggiungere le autorizzazioni entità di database.</span><span class="sxs-lookup"><span data-stu-id="5b774-103">Add Database principals permissions.</span></span>

## <span data-ttu-id="5b774-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b774-104">SYNTAX</span></span>

### <span data-ttu-id="5b774-105">AddExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b774-105">AddExpanded (Default)</span></span>
```
Add-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5b774-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5b774-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5b774-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5b774-107">DESCRIPTION</span></span>
<span data-ttu-id="5b774-108">Aggiungere le autorizzazioni entità di database.</span><span class="sxs-lookup"><span data-stu-id="5b774-108">Add Database principals permissions.</span></span>

## <span data-ttu-id="5b774-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b774-109">EXAMPLES</span></span>

### <span data-ttu-id="5b774-110">Esempio 1: Aggiungere le autorizzazioni entità di database</span><span class="sxs-lookup"><span data-stu-id="5b774-110">Example 1: Add Database principals permissions</span></span>
```powershell
PS C:\> Add-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="5b774-111">Il comando precedente aggiunge le autorizzazioni Entità database</span><span class="sxs-lookup"><span data-stu-id="5b774-111">The above command adds Database principals permissions</span></span>

## <span data-ttu-id="5b774-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b774-112">PARAMETERS</span></span>

### <span data-ttu-id="5b774-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5b774-113">-ClusterName</span></span>
<span data-ttu-id="5b774-114">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="5b774-114">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b774-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5b774-115">-DatabaseName</span></span>
<span data-ttu-id="5b774-116">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="5b774-116">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b774-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b774-117">-DefaultProfile</span></span>
<span data-ttu-id="5b774-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b774-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b774-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b774-119">-InputObject</span></span>
<span data-ttu-id="5b774-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5b774-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: AddViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b774-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b774-121">-ResourceGroupName</span></span>
<span data-ttu-id="5b774-122">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="5b774-122">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b774-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b774-123">-SubscriptionId</span></span>
<span data-ttu-id="5b774-124">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5b774-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5b774-125">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5b774-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b774-126">-Value</span><span class="sxs-lookup"><span data-stu-id="5b774-126">-Value</span></span>
<span data-ttu-id="5b774-127">Elenco delle entità database Kusto.</span><span class="sxs-lookup"><span data-stu-id="5b774-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="5b774-128">Per creare, vedere la sezione NOTE relativa alle proprietà VALUE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5b774-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="5b774-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b774-129">-Confirm</span></span>
<span data-ttu-id="5b774-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b774-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b774-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b774-131">-WhatIf</span></span>
<span data-ttu-id="5b774-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b774-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b774-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b774-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b774-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b774-134">CommonParameters</span></span>
<span data-ttu-id="5b774-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b774-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b774-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5b774-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b774-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="5b774-137">INPUTS</span></span>

### <span data-ttu-id="5b774-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="5b774-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="5b774-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b774-139">OUTPUTS</span></span>

### <span data-ttu-id="5b774-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="5b774-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="5b774-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="5b774-141">NOTES</span></span>

<span data-ttu-id="5b774-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5b774-142">ALIASES</span></span>

<span data-ttu-id="5b774-143">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="5b774-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5b774-144">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="5b774-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5b774-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5b774-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5b774-146">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="5b774-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5b774-147">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="5b774-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="5b774-148">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="5b774-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="5b774-149">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="5b774-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="5b774-150">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="5b774-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="5b774-151">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="5b774-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5b774-152">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5b774-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="5b774-153">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="5b774-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="5b774-154">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="5b774-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="5b774-155">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5b774-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5b774-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5b774-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="5b774-157">VALUE <IDatabasePrincipal[]>: elenco delle entità database Kusto.</span><span class="sxs-lookup"><span data-stu-id="5b774-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="5b774-158">`Name <String>`: nome dell'entità database.</span><span class="sxs-lookup"><span data-stu-id="5b774-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="5b774-159">`Role <DatabasePrincipalRole>`: ruolo principale del database.</span><span class="sxs-lookup"><span data-stu-id="5b774-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="5b774-160">`Type <DatabasePrincipalType>`: tipo di entità database.</span><span class="sxs-lookup"><span data-stu-id="5b774-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="5b774-161">`[AppId <String>]`: ID applicazione- pertinente solo per il tipo di entità applicazione.</span><span class="sxs-lookup"><span data-stu-id="5b774-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="5b774-162">`[Email <String>]`: messaggio di posta elettronica dell'entità database, se esistente.</span><span class="sxs-lookup"><span data-stu-id="5b774-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="5b774-163">`[Fqn <String>]`: nome completo dell'entità database.</span><span class="sxs-lookup"><span data-stu-id="5b774-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="5b774-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b774-164">RELATED LINKS</span></span>

