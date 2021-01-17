---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: e1b5a123d00e097e7e6315ac2231b145de645149
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476157"
---
# <span data-ttu-id="56e1c-101">Add-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="56e1c-101">Add-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="56e1c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="56e1c-103">Aggiungere un elenco di estensioni di lingua che possono essere eseguite in query KQL.</span><span class="sxs-lookup"><span data-stu-id="56e1c-103">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="56e1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56e1c-104">SYNTAX</span></span>

### <span data-ttu-id="56e1c-105">AddExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56e1c-105">AddExpanded (Default)</span></span>
```
Add-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="56e1c-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="56e1c-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="56e1c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56e1c-107">DESCRIPTION</span></span>
<span data-ttu-id="56e1c-108">Aggiungere un elenco di estensioni di lingua che possono essere eseguite in query KQL.</span><span class="sxs-lookup"><span data-stu-id="56e1c-108">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="56e1c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56e1c-109">EXAMPLES</span></span>

### <span data-ttu-id="56e1c-110">Esempio 1: aggiungere un elenco di estensioni della lingua</span><span class="sxs-lookup"><span data-stu-id="56e1c-110">Example 1: Add a list of language extensions</span></span>
```powershell
PS C:\> Add-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"}, @{Name="PYTHON"})
```

<span data-ttu-id="56e1c-111">Il comando precedente aggiunge un elenco di estensioni di lingua che possono essere eseguite in query KQL</span><span class="sxs-lookup"><span data-stu-id="56e1c-111">The above command adds a list of language extensions that can run within KQL queries</span></span>

## <span data-ttu-id="56e1c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56e1c-112">PARAMETERS</span></span>

### <span data-ttu-id="56e1c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56e1c-113">-AsJob</span></span>
<span data-ttu-id="56e1c-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="56e1c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="56e1c-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="56e1c-115">-ClusterName</span></span>
<span data-ttu-id="56e1c-116">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="56e1c-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="56e1c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e1c-117">-DefaultProfile</span></span>
<span data-ttu-id="56e1c-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56e1c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56e1c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56e1c-119">-InputObject</span></span>
<span data-ttu-id="56e1c-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="56e1c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="56e1c-121">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="56e1c-121">-NoWait</span></span>
<span data-ttu-id="56e1c-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="56e1c-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="56e1c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56e1c-123">-PassThru</span></span>
<span data-ttu-id="56e1c-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="56e1c-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="56e1c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56e1c-125">-ResourceGroupName</span></span>
<span data-ttu-id="56e1c-126">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="56e1c-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="56e1c-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56e1c-127">-SubscriptionId</span></span>
<span data-ttu-id="56e1c-128">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="56e1c-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="56e1c-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="56e1c-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="56e1c-130">-Valore</span><span class="sxs-lookup"><span data-stu-id="56e1c-130">-Value</span></span>
<span data-ttu-id="56e1c-131">Elenco delle estensioni della lingua.</span><span class="sxs-lookup"><span data-stu-id="56e1c-131">The list of language extensions.</span></span>
<span data-ttu-id="56e1c-132">Per creare una tabella hash, vedere la sezione Note per le proprietà del valore e crearne una.</span><span class="sxs-lookup"><span data-stu-id="56e1c-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e1c-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56e1c-133">-Confirm</span></span>
<span data-ttu-id="56e1c-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56e1c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56e1c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56e1c-135">-WhatIf</span></span>
<span data-ttu-id="56e1c-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56e1c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56e1c-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56e1c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56e1c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e1c-138">CommonParameters</span></span>
<span data-ttu-id="56e1c-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56e1c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e1c-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56e1c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e1c-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56e1c-141">INPUTS</span></span>

### <span data-ttu-id="56e1c-142">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="56e1c-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="56e1c-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56e1c-143">OUTPUTS</span></span>

### <span data-ttu-id="56e1c-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="56e1c-144">System.Boolean</span></span>

## <span data-ttu-id="56e1c-145">Note</span><span class="sxs-lookup"><span data-stu-id="56e1c-145">NOTES</span></span>

<span data-ttu-id="56e1c-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="56e1c-146">ALIASES</span></span>

<span data-ttu-id="56e1c-147">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56e1c-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56e1c-148">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="56e1c-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56e1c-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="56e1c-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56e1c-150">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="56e1c-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="56e1c-151">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="56e1c-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="56e1c-152">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="56e1c-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="56e1c-153">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="56e1c-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="56e1c-154">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="56e1c-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="56e1c-155">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="56e1c-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="56e1c-156">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="56e1c-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="56e1c-157">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="56e1c-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="56e1c-158">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="56e1c-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="56e1c-159">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="56e1c-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="56e1c-160">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="56e1c-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="56e1c-161">VALUE <ILanguageExtension [] >: l'elenco delle estensioni della lingua.</span><span class="sxs-lookup"><span data-stu-id="56e1c-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="56e1c-162">`[Name <LanguageExtensionName?>]`: Nome dell'estensione della lingua.</span><span class="sxs-lookup"><span data-stu-id="56e1c-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="56e1c-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56e1c-163">RELATED LINKS</span></span>

