---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: bd643f5a655819179646d30bcee1b96f1509df17
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202446"
---
# <span data-ttu-id="efb25-101">Remove-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="efb25-101">Remove-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="efb25-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="efb25-102">SYNOPSIS</span></span>
<span data-ttu-id="efb25-103">Rimuovere un elenco di estensioni di lingua che possono essere eseguite in query KQL.</span><span class="sxs-lookup"><span data-stu-id="efb25-103">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="efb25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="efb25-104">SYNTAX</span></span>

### <span data-ttu-id="efb25-105">RemoveExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="efb25-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="efb25-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="efb25-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="efb25-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efb25-107">DESCRIPTION</span></span>
<span data-ttu-id="efb25-108">Rimuovere un elenco di estensioni di lingua che possono essere eseguite in query KQL.</span><span class="sxs-lookup"><span data-stu-id="efb25-108">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="efb25-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="efb25-109">EXAMPLES</span></span>

### <span data-ttu-id="efb25-110">Esempio 1: rimuovere un elenco di estensioni di lingua dal cluster</span><span class="sxs-lookup"><span data-stu-id="efb25-110">Example 1: Remove a list of language extensions from cluster</span></span>
```powershell
PS C:\> Remove-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"})
```

<span data-ttu-id="efb25-111">Il comando precedente consente di rimuovere un elenco di estensioni di lingua che possono essere eseguite in query KQL.</span><span class="sxs-lookup"><span data-stu-id="efb25-111">The above command removes a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="efb25-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="efb25-112">PARAMETERS</span></span>

### <span data-ttu-id="efb25-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efb25-113">-AsJob</span></span>
<span data-ttu-id="efb25-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="efb25-114">Run the command as a job</span></span>

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

### <span data-ttu-id="efb25-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="efb25-115">-ClusterName</span></span>
<span data-ttu-id="efb25-116">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="efb25-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="efb25-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efb25-117">-DefaultProfile</span></span>
<span data-ttu-id="efb25-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="efb25-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efb25-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efb25-119">-InputObject</span></span>
<span data-ttu-id="efb25-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="efb25-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="efb25-121">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="efb25-121">-NoWait</span></span>
<span data-ttu-id="efb25-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="efb25-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="efb25-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efb25-123">-PassThru</span></span>
<span data-ttu-id="efb25-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="efb25-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="efb25-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efb25-125">-ResourceGroupName</span></span>
<span data-ttu-id="efb25-126">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="efb25-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="efb25-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="efb25-127">-SubscriptionId</span></span>
<span data-ttu-id="efb25-128">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="efb25-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="efb25-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="efb25-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="efb25-130">-Valore</span><span class="sxs-lookup"><span data-stu-id="efb25-130">-Value</span></span>
<span data-ttu-id="efb25-131">Elenco delle estensioni della lingua.</span><span class="sxs-lookup"><span data-stu-id="efb25-131">The list of language extensions.</span></span>
<span data-ttu-id="efb25-132">Per creare una tabella hash, vedere la sezione Note per le proprietà del valore e crearne una.</span><span class="sxs-lookup"><span data-stu-id="efb25-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="efb25-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="efb25-133">-Confirm</span></span>
<span data-ttu-id="efb25-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efb25-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efb25-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efb25-135">-WhatIf</span></span>
<span data-ttu-id="efb25-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efb25-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efb25-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efb25-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efb25-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb25-138">CommonParameters</span></span>
<span data-ttu-id="efb25-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efb25-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb25-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="efb25-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb25-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="efb25-141">INPUTS</span></span>

### <span data-ttu-id="efb25-142">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="efb25-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="efb25-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="efb25-143">OUTPUTS</span></span>

### <span data-ttu-id="efb25-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="efb25-144">System.Boolean</span></span>

## <span data-ttu-id="efb25-145">Note</span><span class="sxs-lookup"><span data-stu-id="efb25-145">NOTES</span></span>

<span data-ttu-id="efb25-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="efb25-146">ALIASES</span></span>

<span data-ttu-id="efb25-147">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="efb25-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="efb25-148">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="efb25-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="efb25-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="efb25-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="efb25-150">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="efb25-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="efb25-151">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="efb25-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="efb25-152">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="efb25-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="efb25-153">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="efb25-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="efb25-154">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="efb25-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="efb25-155">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="efb25-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="efb25-156">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="efb25-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="efb25-157">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="efb25-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="efb25-158">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="efb25-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="efb25-159">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="efb25-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="efb25-160">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="efb25-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="efb25-161">VALUE <ILanguageExtension [] >: l'elenco delle estensioni della lingua.</span><span class="sxs-lookup"><span data-stu-id="efb25-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="efb25-162">`[Name <LanguageExtensionName?>]`: Nome dell'estensione della lingua.</span><span class="sxs-lookup"><span data-stu-id="efb25-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="efb25-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="efb25-163">RELATED LINKS</span></span>

