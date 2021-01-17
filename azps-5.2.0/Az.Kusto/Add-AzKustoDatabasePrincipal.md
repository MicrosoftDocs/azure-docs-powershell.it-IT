---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
ms.openlocfilehash: d7af2877d4823f1da85f08e61035b386d57a9c2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361630"
---
# <span data-ttu-id="83548-101">Add-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="83548-101">Add-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="83548-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83548-102">SYNOPSIS</span></span>
<span data-ttu-id="83548-103">Aggiungere le autorizzazioni di entità di database.</span><span class="sxs-lookup"><span data-stu-id="83548-103">Add Database principals permissions.</span></span>

## <span data-ttu-id="83548-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83548-104">SYNTAX</span></span>

### <span data-ttu-id="83548-105">AddExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="83548-105">AddExpanded (Default)</span></span>
```
Add-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="83548-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="83548-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="83548-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83548-107">DESCRIPTION</span></span>
<span data-ttu-id="83548-108">Aggiungere le autorizzazioni di entità di database.</span><span class="sxs-lookup"><span data-stu-id="83548-108">Add Database principals permissions.</span></span>

## <span data-ttu-id="83548-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83548-109">EXAMPLES</span></span>

### <span data-ttu-id="83548-110">Esempio 1: aggiungere le autorizzazioni per le entità di database</span><span class="sxs-lookup"><span data-stu-id="83548-110">Example 1: Add Database principals permissions</span></span>
```powershell
PS C:\> Add-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="83548-111">Il comando precedente aggiunge le autorizzazioni per le entità di database</span><span class="sxs-lookup"><span data-stu-id="83548-111">The above command adds Database principals permissions</span></span>

## <span data-ttu-id="83548-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83548-112">PARAMETERS</span></span>

### <span data-ttu-id="83548-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="83548-113">-ClusterName</span></span>
<span data-ttu-id="83548-114">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="83548-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="83548-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="83548-115">-DatabaseName</span></span>
<span data-ttu-id="83548-116">Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="83548-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="83548-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83548-117">-DefaultProfile</span></span>
<span data-ttu-id="83548-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83548-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83548-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83548-119">-InputObject</span></span>
<span data-ttu-id="83548-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="83548-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="83548-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83548-121">-ResourceGroupName</span></span>
<span data-ttu-id="83548-122">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="83548-122">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="83548-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83548-123">-SubscriptionId</span></span>
<span data-ttu-id="83548-124">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="83548-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="83548-125">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="83548-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="83548-126">-Valore</span><span class="sxs-lookup"><span data-stu-id="83548-126">-Value</span></span>
<span data-ttu-id="83548-127">Elenco delle entità di database di Kusto.</span><span class="sxs-lookup"><span data-stu-id="83548-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="83548-128">Per creare una tabella hash, vedere la sezione Note per le proprietà del valore e crearne una.</span><span class="sxs-lookup"><span data-stu-id="83548-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83548-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="83548-129">-Confirm</span></span>
<span data-ttu-id="83548-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83548-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83548-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83548-131">-WhatIf</span></span>
<span data-ttu-id="83548-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83548-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83548-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83548-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83548-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83548-134">CommonParameters</span></span>
<span data-ttu-id="83548-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83548-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83548-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83548-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83548-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83548-137">INPUTS</span></span>

### <span data-ttu-id="83548-138">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="83548-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="83548-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83548-139">OUTPUTS</span></span>

### <span data-ttu-id="83548-140">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="83548-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="83548-141">Note</span><span class="sxs-lookup"><span data-stu-id="83548-141">NOTES</span></span>

<span data-ttu-id="83548-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="83548-142">ALIASES</span></span>

<span data-ttu-id="83548-143">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83548-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83548-144">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="83548-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83548-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="83548-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83548-146">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="83548-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="83548-147">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="83548-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="83548-148">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="83548-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="83548-149">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="83548-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="83548-150">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="83548-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="83548-151">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="83548-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="83548-152">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="83548-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="83548-153">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="83548-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="83548-154">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="83548-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="83548-155">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="83548-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="83548-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="83548-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="83548-157">VALUE <IDatabasePrincipal [] >: l'elenco delle entità di database di Kusto.</span><span class="sxs-lookup"><span data-stu-id="83548-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="83548-158">`Name <String>`: Nome dell'entità database.</span><span class="sxs-lookup"><span data-stu-id="83548-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="83548-159">`Role <DatabasePrincipalRole>`: Ruolo principale database.</span><span class="sxs-lookup"><span data-stu-id="83548-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="83548-160">`Type <DatabasePrincipalType>`: Tipo di entità database.</span><span class="sxs-lookup"><span data-stu-id="83548-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="83548-161">`[AppId <String>]`: ID applicazione-rilevante solo per il tipo di entità Application.</span><span class="sxs-lookup"><span data-stu-id="83548-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="83548-162">`[Email <String>]`: Messaggio di posta elettronica principale del database se esistente.</span><span class="sxs-lookup"><span data-stu-id="83548-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="83548-163">`[Fqn <String>]`: Nome completo dell'entità database.</span><span class="sxs-lookup"><span data-stu-id="83548-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="83548-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83548-164">RELATED LINKS</span></span>

