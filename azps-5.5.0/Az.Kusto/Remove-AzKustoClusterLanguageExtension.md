---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 9cac9f92e61ac17ed825dd3e39991fc85c661d9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194310"
---
# <span data-ttu-id="61d78-101">Remove-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="61d78-101">Remove-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="61d78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61d78-102">SYNOPSIS</span></span>
<span data-ttu-id="61d78-103">Rimuovere un elenco di estensioni del linguaggio che possono essere eseguite all'interno di query KQL.</span><span class="sxs-lookup"><span data-stu-id="61d78-103">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="61d78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61d78-104">SYNTAX</span></span>

### <span data-ttu-id="61d78-105">RemoveExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61d78-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="61d78-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="61d78-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="61d78-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="61d78-107">DESCRIPTION</span></span>
<span data-ttu-id="61d78-108">Rimuovere un elenco di estensioni del linguaggio che possono essere eseguite all'interno di query KQL.</span><span class="sxs-lookup"><span data-stu-id="61d78-108">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="61d78-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61d78-109">EXAMPLES</span></span>

### <span data-ttu-id="61d78-110">Esempio 1: Rimuovere un elenco di estensioni delle lingue dal cluster</span><span class="sxs-lookup"><span data-stu-id="61d78-110">Example 1: Remove a list of language extensions from cluster</span></span>
```powershell
PS C:\> Remove-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"})
```

<span data-ttu-id="61d78-111">Il comando precedente rimuove un elenco di estensioni di lingua che possono essere eseguite all'interno di query KQL.</span><span class="sxs-lookup"><span data-stu-id="61d78-111">The above command removes a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="61d78-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61d78-112">PARAMETERS</span></span>

### <span data-ttu-id="61d78-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61d78-113">-AsJob</span></span>
<span data-ttu-id="61d78-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="61d78-114">Run the command as a job</span></span>

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

### <span data-ttu-id="61d78-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="61d78-115">-ClusterName</span></span>
<span data-ttu-id="61d78-116">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="61d78-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="61d78-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61d78-117">-DefaultProfile</span></span>
<span data-ttu-id="61d78-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61d78-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61d78-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61d78-119">-InputObject</span></span>
<span data-ttu-id="61d78-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="61d78-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="61d78-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="61d78-121">-NoWait</span></span>
<span data-ttu-id="61d78-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="61d78-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="61d78-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61d78-123">-PassThru</span></span>
<span data-ttu-id="61d78-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="61d78-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="61d78-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61d78-125">-ResourceGroupName</span></span>
<span data-ttu-id="61d78-126">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="61d78-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="61d78-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="61d78-127">-SubscriptionId</span></span>
<span data-ttu-id="61d78-128">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="61d78-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="61d78-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="61d78-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="61d78-130">-Value</span><span class="sxs-lookup"><span data-stu-id="61d78-130">-Value</span></span>
<span data-ttu-id="61d78-131">L'elenco delle estensioni di lingua.</span><span class="sxs-lookup"><span data-stu-id="61d78-131">The list of language extensions.</span></span>
<span data-ttu-id="61d78-132">Per creare, vedere la sezione NOTE relativa alle proprietà VALUE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="61d78-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="61d78-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61d78-133">-Confirm</span></span>
<span data-ttu-id="61d78-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61d78-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61d78-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61d78-135">-WhatIf</span></span>
<span data-ttu-id="61d78-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61d78-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61d78-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61d78-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61d78-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d78-138">CommonParameters</span></span>
<span data-ttu-id="61d78-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61d78-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d78-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61d78-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d78-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="61d78-141">INPUTS</span></span>

### <span data-ttu-id="61d78-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="61d78-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="61d78-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61d78-143">OUTPUTS</span></span>

### <span data-ttu-id="61d78-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="61d78-144">System.Boolean</span></span>

## <span data-ttu-id="61d78-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="61d78-145">NOTES</span></span>

<span data-ttu-id="61d78-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="61d78-146">ALIASES</span></span>

<span data-ttu-id="61d78-147">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="61d78-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="61d78-148">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="61d78-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="61d78-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="61d78-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="61d78-150">INPUTOBJECT <IKustoIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="61d78-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="61d78-151">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="61d78-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="61d78-152">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="61d78-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="61d78-153">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="61d78-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="61d78-154">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="61d78-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="61d78-155">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="61d78-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="61d78-156">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="61d78-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="61d78-157">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="61d78-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="61d78-158">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="61d78-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="61d78-159">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="61d78-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="61d78-160">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="61d78-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="61d78-161">VALUE <ILanguageExtension[]>: elenco delle estensioni delle lingue.</span><span class="sxs-lookup"><span data-stu-id="61d78-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="61d78-162">`[Name <LanguageExtensionName?>]`: nome dell'estensione della lingua.</span><span class="sxs-lookup"><span data-stu-id="61d78-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="61d78-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61d78-163">RELATED LINKS</span></span>

