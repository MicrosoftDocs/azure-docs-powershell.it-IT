---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: 682de416a4aba61e1f287661c88faee9e20d248c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202461"
---
# <span data-ttu-id="b887f-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b887f-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="b887f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b887f-102">SYNOPSIS</span></span>
<span data-ttu-id="b887f-103">Diagnostica lo stato di connettività di rete per le risorse esterne da cui dipende il servizio.</span><span class="sxs-lookup"><span data-stu-id="b887f-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="b887f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b887f-104">SYNTAX</span></span>

### <span data-ttu-id="b887f-105">Diagnostica (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b887f-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b887f-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b887f-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b887f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b887f-107">DESCRIPTION</span></span>
<span data-ttu-id="b887f-108">Diagnostica lo stato di connettività di rete per le risorse esterne da cui dipende il servizio.</span><span class="sxs-lookup"><span data-stu-id="b887f-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="b887f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b887f-109">EXAMPLES</span></span>

### <span data-ttu-id="b887f-110">Esempio 1: visualizzare la diagnosi della connettività di rete per le risorse esterne</span><span class="sxs-lookup"><span data-stu-id="b887f-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="b887f-111">Il comando precedente diagnostica lo stato della connettività di rete per le risorse esterne da cui dipende il cluster "testnewkustocluster"</span><span class="sxs-lookup"><span data-stu-id="b887f-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="b887f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b887f-112">PARAMETERS</span></span>

### <span data-ttu-id="b887f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b887f-113">-AsJob</span></span>
<span data-ttu-id="b887f-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="b887f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b887f-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="b887f-115">-ClusterName</span></span>
<span data-ttu-id="b887f-116">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b887f-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b887f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b887f-117">-DefaultProfile</span></span>
<span data-ttu-id="b887f-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b887f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b887f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b887f-119">-InputObject</span></span>
<span data-ttu-id="b887f-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b887f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b887f-121">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="b887f-121">-NoWait</span></span>
<span data-ttu-id="b887f-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="b887f-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b887f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b887f-123">-ResourceGroupName</span></span>
<span data-ttu-id="b887f-124">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b887f-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b887f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b887f-125">-SubscriptionId</span></span>
<span data-ttu-id="b887f-126">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b887f-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b887f-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b887f-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b887f-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b887f-128">-Confirm</span></span>
<span data-ttu-id="b887f-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b887f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b887f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b887f-130">-WhatIf</span></span>
<span data-ttu-id="b887f-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b887f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b887f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b887f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b887f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b887f-133">CommonParameters</span></span>
<span data-ttu-id="b887f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b887f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b887f-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b887f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b887f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b887f-136">INPUTS</span></span>

### <span data-ttu-id="b887f-137">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="b887f-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="b887f-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b887f-138">OUTPUTS</span></span>

### <span data-ttu-id="b887f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b887f-139">System.String</span></span>

## <span data-ttu-id="b887f-140">Note</span><span class="sxs-lookup"><span data-stu-id="b887f-140">NOTES</span></span>

<span data-ttu-id="b887f-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b887f-141">ALIASES</span></span>

<span data-ttu-id="b887f-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b887f-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b887f-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b887f-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b887f-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b887f-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b887f-145">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b887f-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b887f-146">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="b887f-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="b887f-147">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b887f-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="b887f-148">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="b887f-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="b887f-149">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b887f-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="b887f-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="b887f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b887f-151">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b887f-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="b887f-152">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="b887f-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="b887f-153">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="b887f-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="b887f-154">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b887f-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b887f-155">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b887f-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b887f-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b887f-156">RELATED LINKS</span></span>

