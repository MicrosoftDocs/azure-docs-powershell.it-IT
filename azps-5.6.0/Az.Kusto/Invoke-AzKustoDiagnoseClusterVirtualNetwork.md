---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: d2530404774c3cb735dedb6eb233979fe602fe4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012046"
---
# <span data-ttu-id="d9b00-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d9b00-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="d9b00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9b00-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b00-103">Diagnostica lo stato della connettività di rete per le risorse esterne da cui dipende il servizio.</span><span class="sxs-lookup"><span data-stu-id="d9b00-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="d9b00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9b00-104">SYNTAX</span></span>

### <span data-ttu-id="d9b00-105">Diagnosi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9b00-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d9b00-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d9b00-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d9b00-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d9b00-107">DESCRIPTION</span></span>
<span data-ttu-id="d9b00-108">Diagnostica lo stato della connettività di rete per le risorse esterne da cui dipende il servizio.</span><span class="sxs-lookup"><span data-stu-id="d9b00-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="d9b00-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9b00-109">EXAMPLES</span></span>

### <span data-ttu-id="d9b00-110">Esempio 1: Visualizzare la diagnosi della connettività di rete per le risorse esterne</span><span class="sxs-lookup"><span data-stu-id="d9b00-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="d9b00-111">Il comando precedente diagnostica lo stato della connettività di rete per le risorse esterne da cui il cluster "testnewkustocluster" dipende</span><span class="sxs-lookup"><span data-stu-id="d9b00-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="d9b00-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9b00-112">PARAMETERS</span></span>

### <span data-ttu-id="d9b00-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9b00-113">-AsJob</span></span>
<span data-ttu-id="d9b00-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="d9b00-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d9b00-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d9b00-115">-ClusterName</span></span>
<span data-ttu-id="d9b00-116">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d9b00-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d9b00-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b00-117">-DefaultProfile</span></span>
<span data-ttu-id="d9b00-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b00-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9b00-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9b00-119">-InputObject</span></span>
<span data-ttu-id="d9b00-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d9b00-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d9b00-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d9b00-121">-NoWait</span></span>
<span data-ttu-id="d9b00-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="d9b00-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d9b00-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9b00-123">-ResourceGroupName</span></span>
<span data-ttu-id="d9b00-124">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d9b00-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d9b00-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9b00-125">-SubscriptionId</span></span>
<span data-ttu-id="d9b00-126">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b00-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d9b00-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d9b00-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d9b00-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9b00-128">-Confirm</span></span>
<span data-ttu-id="d9b00-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9b00-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9b00-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9b00-130">-WhatIf</span></span>
<span data-ttu-id="d9b00-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9b00-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9b00-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9b00-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9b00-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b00-133">CommonParameters</span></span>
<span data-ttu-id="d9b00-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9b00-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b00-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d9b00-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b00-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="d9b00-136">INPUTS</span></span>

### <span data-ttu-id="d9b00-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d9b00-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d9b00-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9b00-138">OUTPUTS</span></span>

### <span data-ttu-id="d9b00-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d9b00-139">System.String</span></span>

## <span data-ttu-id="d9b00-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="d9b00-140">NOTES</span></span>

<span data-ttu-id="d9b00-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d9b00-141">ALIASES</span></span>

<span data-ttu-id="d9b00-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="d9b00-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d9b00-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d9b00-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d9b00-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d9b00-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d9b00-145">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="d9b00-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d9b00-146">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="d9b00-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d9b00-147">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d9b00-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d9b00-148">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="d9b00-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d9b00-149">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d9b00-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d9b00-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="d9b00-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d9b00-151">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b00-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d9b00-152">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d9b00-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d9b00-153">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d9b00-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d9b00-154">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b00-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d9b00-155">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d9b00-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d9b00-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9b00-156">RELATED LINKS</span></span>

