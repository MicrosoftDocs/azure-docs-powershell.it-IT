---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 11789a16186d0f7c8358371ace2a454d78d932df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189821"
---
# <span data-ttu-id="d503a-101">Add-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="d503a-101">Add-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="d503a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d503a-102">SYNOPSIS</span></span>
<span data-ttu-id="d503a-103">Aggiungere un elenco di estensioni di lingua che possono essere eseguite in query KQL.</span><span class="sxs-lookup"><span data-stu-id="d503a-103">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="d503a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d503a-104">SYNTAX</span></span>

### <span data-ttu-id="d503a-105">AddExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d503a-105">AddExpanded (Default)</span></span>
```
Add-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d503a-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d503a-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d503a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d503a-107">DESCRIPTION</span></span>
<span data-ttu-id="d503a-108">Aggiungere un elenco di estensioni di lingua che possono essere eseguite in query KQL.</span><span class="sxs-lookup"><span data-stu-id="d503a-108">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="d503a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d503a-109">EXAMPLES</span></span>

### <span data-ttu-id="d503a-110">Esempio 1: aggiungere un elenco di estensioni della lingua</span><span class="sxs-lookup"><span data-stu-id="d503a-110">Example 1: Add a list of language extensions</span></span>
```powershell
PS C:\> Add-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"}, @{Name="PYTHON"})
```

<span data-ttu-id="d503a-111">Il comando precedente aggiunge un elenco di estensioni di lingua che possono essere eseguite in query KQL</span><span class="sxs-lookup"><span data-stu-id="d503a-111">The above command adds a list of language extensions that can run within KQL queries</span></span>

## <span data-ttu-id="d503a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d503a-112">PARAMETERS</span></span>

### <span data-ttu-id="d503a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d503a-113">-AsJob</span></span>
<span data-ttu-id="d503a-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="d503a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d503a-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="d503a-115">-ClusterName</span></span>
<span data-ttu-id="d503a-116">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="d503a-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d503a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d503a-117">-DefaultProfile</span></span>
<span data-ttu-id="d503a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d503a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d503a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d503a-119">-InputObject</span></span>
<span data-ttu-id="d503a-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d503a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d503a-121">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="d503a-121">-NoWait</span></span>
<span data-ttu-id="d503a-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="d503a-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d503a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d503a-123">-PassThru</span></span>
<span data-ttu-id="d503a-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="d503a-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d503a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d503a-125">-ResourceGroupName</span></span>
<span data-ttu-id="d503a-126">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="d503a-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d503a-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d503a-127">-SubscriptionId</span></span>
<span data-ttu-id="d503a-128">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d503a-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d503a-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d503a-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d503a-130">-Valore</span><span class="sxs-lookup"><span data-stu-id="d503a-130">-Value</span></span>
<span data-ttu-id="d503a-131">Elenco delle estensioni della lingua.</span><span class="sxs-lookup"><span data-stu-id="d503a-131">The list of language extensions.</span></span>
<span data-ttu-id="d503a-132">Per creare una tabella hash, vedere la sezione Note per le proprietà del valore e crearne una.</span><span class="sxs-lookup"><span data-stu-id="d503a-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d503a-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d503a-133">-Confirm</span></span>
<span data-ttu-id="d503a-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d503a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d503a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d503a-135">-WhatIf</span></span>
<span data-ttu-id="d503a-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d503a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d503a-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d503a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d503a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d503a-138">CommonParameters</span></span>
<span data-ttu-id="d503a-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d503a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d503a-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d503a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d503a-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d503a-141">INPUTS</span></span>

### <span data-ttu-id="d503a-142">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d503a-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d503a-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d503a-143">OUTPUTS</span></span>

### <span data-ttu-id="d503a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d503a-144">System.Boolean</span></span>

## <span data-ttu-id="d503a-145">Note</span><span class="sxs-lookup"><span data-stu-id="d503a-145">NOTES</span></span>

<span data-ttu-id="d503a-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d503a-146">ALIASES</span></span>

<span data-ttu-id="d503a-147">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d503a-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d503a-148">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d503a-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d503a-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d503a-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d503a-150">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="d503a-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d503a-151">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="d503a-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d503a-152">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="d503a-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d503a-153">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="d503a-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d503a-154">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="d503a-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d503a-155">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="d503a-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d503a-156">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d503a-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d503a-157">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="d503a-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d503a-158">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="d503a-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d503a-159">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d503a-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d503a-160">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d503a-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="d503a-161">VALUE <ILanguageExtension [] >: l'elenco delle estensioni della lingua.</span><span class="sxs-lookup"><span data-stu-id="d503a-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="d503a-162">`[Name <LanguageExtensionName?>]`: Nome dell'estensione della lingua.</span><span class="sxs-lookup"><span data-stu-id="d503a-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="d503a-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d503a-163">RELATED LINKS</span></span>

