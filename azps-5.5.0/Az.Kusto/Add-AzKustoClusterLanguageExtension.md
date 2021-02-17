---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: e1b5a123d00e097e7e6315ac2231b145de645149
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185319"
---
# <span data-ttu-id="e227f-101">Add-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="e227f-101">Add-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="e227f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e227f-102">SYNOPSIS</span></span>
<span data-ttu-id="e227f-103">Aggiungere un elenco di estensioni del linguaggio che possono essere eseguite all'interno di query KQL.</span><span class="sxs-lookup"><span data-stu-id="e227f-103">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="e227f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e227f-104">SYNTAX</span></span>

### <span data-ttu-id="e227f-105">AddExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e227f-105">AddExpanded (Default)</span></span>
```
Add-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e227f-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e227f-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e227f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e227f-107">DESCRIPTION</span></span>
<span data-ttu-id="e227f-108">Aggiungere un elenco di estensioni del linguaggio che possono essere eseguite all'interno di query KQL.</span><span class="sxs-lookup"><span data-stu-id="e227f-108">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="e227f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e227f-109">EXAMPLES</span></span>

### <span data-ttu-id="e227f-110">Esempio 1: Aggiungere un elenco di estensioni della lingua</span><span class="sxs-lookup"><span data-stu-id="e227f-110">Example 1: Add a list of language extensions</span></span>
```powershell
PS C:\> Add-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"}, @{Name="PYTHON"})
```

<span data-ttu-id="e227f-111">Il comando precedente aggiunge un elenco di estensioni delle lingue che possono essere eseguite all'interno di query KQL</span><span class="sxs-lookup"><span data-stu-id="e227f-111">The above command adds a list of language extensions that can run within KQL queries</span></span>

## <span data-ttu-id="e227f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e227f-112">PARAMETERS</span></span>

### <span data-ttu-id="e227f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e227f-113">-AsJob</span></span>
<span data-ttu-id="e227f-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="e227f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e227f-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e227f-115">-ClusterName</span></span>
<span data-ttu-id="e227f-116">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e227f-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e227f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e227f-117">-DefaultProfile</span></span>
<span data-ttu-id="e227f-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e227f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e227f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e227f-119">-InputObject</span></span>
<span data-ttu-id="e227f-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e227f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e227f-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e227f-121">-NoWait</span></span>
<span data-ttu-id="e227f-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="e227f-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e227f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e227f-123">-PassThru</span></span>
<span data-ttu-id="e227f-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="e227f-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e227f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e227f-125">-ResourceGroupName</span></span>
<span data-ttu-id="e227f-126">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e227f-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e227f-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e227f-127">-SubscriptionId</span></span>
<span data-ttu-id="e227f-128">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e227f-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e227f-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e227f-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e227f-130">-Value</span><span class="sxs-lookup"><span data-stu-id="e227f-130">-Value</span></span>
<span data-ttu-id="e227f-131">L'elenco delle estensioni di lingua.</span><span class="sxs-lookup"><span data-stu-id="e227f-131">The list of language extensions.</span></span>
<span data-ttu-id="e227f-132">Per creare, vedere la sezione NOTE relativa alle proprietà VALUE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e227f-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="e227f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e227f-133">-Confirm</span></span>
<span data-ttu-id="e227f-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e227f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e227f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e227f-135">-WhatIf</span></span>
<span data-ttu-id="e227f-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e227f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e227f-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e227f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e227f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e227f-138">CommonParameters</span></span>
<span data-ttu-id="e227f-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e227f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e227f-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e227f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e227f-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="e227f-141">INPUTS</span></span>

### <span data-ttu-id="e227f-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="e227f-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e227f-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e227f-143">OUTPUTS</span></span>

### <span data-ttu-id="e227f-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e227f-144">System.Boolean</span></span>

## <span data-ttu-id="e227f-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="e227f-145">NOTES</span></span>

<span data-ttu-id="e227f-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e227f-146">ALIASES</span></span>

<span data-ttu-id="e227f-147">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="e227f-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e227f-148">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e227f-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e227f-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e227f-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e227f-150">INPUTOBJECT <IKustoIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="e227f-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e227f-151">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="e227f-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e227f-152">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e227f-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e227f-153">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="e227f-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e227f-154">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e227f-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e227f-155">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="e227f-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e227f-156">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e227f-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e227f-157">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="e227f-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e227f-158">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e227f-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e227f-159">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e227f-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e227f-160">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e227f-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="e227f-161">VALUE <ILanguageExtension[]>: elenco delle estensioni delle lingue.</span><span class="sxs-lookup"><span data-stu-id="e227f-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="e227f-162">`[Name <LanguageExtensionName?>]`: nome dell'estensione della lingua.</span><span class="sxs-lookup"><span data-stu-id="e227f-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="e227f-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e227f-163">RELATED LINKS</span></span>

