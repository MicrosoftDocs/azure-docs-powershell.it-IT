---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/stop-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
ms.openlocfilehash: 4f03c3fd8e36e8122a8ada001efa97475922dc91
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007853"
---
# <span data-ttu-id="9a229-101">Stop-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="9a229-101">Stop-AzKustoCluster</span></span>

## <span data-ttu-id="9a229-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a229-102">SYNOPSIS</span></span>
<span data-ttu-id="9a229-103">Ferma un cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9a229-103">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="9a229-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a229-104">SYNTAX</span></span>

### <span data-ttu-id="9a229-105">Interrompi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9a229-105">Stop (Default)</span></span>
```
Stop-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9a229-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9a229-106">StopViaIdentity</span></span>
```
Stop-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9a229-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9a229-107">DESCRIPTION</span></span>
<span data-ttu-id="9a229-108">Ferma un cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9a229-108">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="9a229-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a229-109">EXAMPLES</span></span>

### <span data-ttu-id="9a229-110">Esempio 1: Interrompere un cluster di Kusto</span><span class="sxs-lookup"><span data-stu-id="9a229-110">Example 1: Stop a Kusto cluster</span></span>
```powershell
PS C:\> Stop-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="9a229-111">Il comando precedente interrompe un cluster Kusto</span><span class="sxs-lookup"><span data-stu-id="9a229-111">The above command stops a Kusto cluster</span></span>

## <span data-ttu-id="9a229-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a229-112">PARAMETERS</span></span>

### <span data-ttu-id="9a229-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a229-113">-AsJob</span></span>
<span data-ttu-id="9a229-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="9a229-114">Run the command as a job</span></span>

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

### <span data-ttu-id="9a229-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a229-115">-DefaultProfile</span></span>
<span data-ttu-id="9a229-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a229-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a229-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a229-117">-InputObject</span></span>
<span data-ttu-id="9a229-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9a229-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a229-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9a229-119">-Name</span></span>
<span data-ttu-id="9a229-120">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9a229-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a229-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9a229-121">-NoWait</span></span>
<span data-ttu-id="9a229-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="9a229-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9a229-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a229-123">-PassThru</span></span>
<span data-ttu-id="9a229-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="9a229-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9a229-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a229-125">-ResourceGroupName</span></span>
<span data-ttu-id="9a229-126">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9a229-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a229-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9a229-127">-SubscriptionId</span></span>
<span data-ttu-id="9a229-128">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9a229-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9a229-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="9a229-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a229-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a229-130">-Confirm</span></span>
<span data-ttu-id="9a229-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a229-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a229-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a229-132">-WhatIf</span></span>
<span data-ttu-id="9a229-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a229-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a229-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a229-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a229-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a229-135">CommonParameters</span></span>
<span data-ttu-id="9a229-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a229-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a229-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9a229-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a229-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="9a229-138">INPUTS</span></span>

### <span data-ttu-id="9a229-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="9a229-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="9a229-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a229-140">OUTPUTS</span></span>

### <span data-ttu-id="9a229-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9a229-141">System.Boolean</span></span>

## <span data-ttu-id="9a229-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="9a229-142">NOTES</span></span>

<span data-ttu-id="9a229-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9a229-143">ALIASES</span></span>

<span data-ttu-id="9a229-144">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="9a229-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9a229-145">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="9a229-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9a229-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9a229-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9a229-147">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="9a229-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9a229-148">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="9a229-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="9a229-149">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9a229-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="9a229-150">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="9a229-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="9a229-151">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9a229-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="9a229-152">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="9a229-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9a229-153">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9a229-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="9a229-154">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="9a229-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="9a229-155">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9a229-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="9a229-156">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9a229-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9a229-157">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="9a229-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9a229-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a229-158">RELATED LINKS</span></span>

