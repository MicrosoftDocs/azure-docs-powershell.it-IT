---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: 682de416a4aba61e1f287661c88faee9e20d248c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209266"
---
# <span data-ttu-id="fadc6-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fadc6-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="fadc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fadc6-102">SYNOPSIS</span></span>
<span data-ttu-id="fadc6-103">Diagnostica lo stato della connettività di rete per le risorse esterne da cui dipende il servizio.</span><span class="sxs-lookup"><span data-stu-id="fadc6-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="fadc6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fadc6-104">SYNTAX</span></span>

### <span data-ttu-id="fadc6-105">Diagnosi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fadc6-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fadc6-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fadc6-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fadc6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fadc6-107">DESCRIPTION</span></span>
<span data-ttu-id="fadc6-108">Diagnostica lo stato della connettività di rete per le risorse esterne da cui dipende il servizio.</span><span class="sxs-lookup"><span data-stu-id="fadc6-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="fadc6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fadc6-109">EXAMPLES</span></span>

### <span data-ttu-id="fadc6-110">Esempio 1: Visualizzare la diagnosi della connettività di rete per le risorse esterne</span><span class="sxs-lookup"><span data-stu-id="fadc6-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="fadc6-111">Il comando precedente diagnostica lo stato della connettività di rete per le risorse esterne da cui il cluster "testnewkustocluster" dipende</span><span class="sxs-lookup"><span data-stu-id="fadc6-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="fadc6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fadc6-112">PARAMETERS</span></span>

### <span data-ttu-id="fadc6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fadc6-113">-AsJob</span></span>
<span data-ttu-id="fadc6-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="fadc6-114">Run the command as a job</span></span>

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

### <span data-ttu-id="fadc6-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fadc6-115">-ClusterName</span></span>
<span data-ttu-id="fadc6-116">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fadc6-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fadc6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fadc6-117">-DefaultProfile</span></span>
<span data-ttu-id="fadc6-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fadc6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fadc6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fadc6-119">-InputObject</span></span>
<span data-ttu-id="fadc6-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="fadc6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DiagnoseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fadc6-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fadc6-121">-NoWait</span></span>
<span data-ttu-id="fadc6-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="fadc6-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fadc6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fadc6-123">-ResourceGroupName</span></span>
<span data-ttu-id="fadc6-124">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fadc6-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fadc6-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fadc6-125">-SubscriptionId</span></span>
<span data-ttu-id="fadc6-126">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fadc6-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fadc6-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="fadc6-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fadc6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fadc6-128">-Confirm</span></span>
<span data-ttu-id="fadc6-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fadc6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fadc6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fadc6-130">-WhatIf</span></span>
<span data-ttu-id="fadc6-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fadc6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fadc6-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fadc6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fadc6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fadc6-133">CommonParameters</span></span>
<span data-ttu-id="fadc6-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fadc6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fadc6-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fadc6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fadc6-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="fadc6-136">INPUTS</span></span>

### <span data-ttu-id="fadc6-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="fadc6-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="fadc6-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fadc6-138">OUTPUTS</span></span>

### <span data-ttu-id="fadc6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="fadc6-139">System.String</span></span>

## <span data-ttu-id="fadc6-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="fadc6-140">NOTES</span></span>

<span data-ttu-id="fadc6-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fadc6-141">ALIASES</span></span>

<span data-ttu-id="fadc6-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="fadc6-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fadc6-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="fadc6-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fadc6-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fadc6-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fadc6-145">INPUTOBJECT <IKustoIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="fadc6-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fadc6-146">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="fadc6-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="fadc6-147">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fadc6-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="fadc6-148">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="fadc6-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="fadc6-149">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fadc6-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="fadc6-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="fadc6-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fadc6-151">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fadc6-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="fadc6-152">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="fadc6-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="fadc6-153">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fadc6-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="fadc6-154">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fadc6-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fadc6-155">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="fadc6-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="fadc6-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fadc6-156">RELATED LINKS</span></span>

