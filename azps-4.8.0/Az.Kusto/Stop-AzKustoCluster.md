---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/stop-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
ms.openlocfilehash: 1dd67a5a3557ba38267f570c77b5117466e4260b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031669"
---
# <span data-ttu-id="3ea12-101">Stop-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="3ea12-101">Stop-AzKustoCluster</span></span>

## <span data-ttu-id="3ea12-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ea12-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea12-103">Arresta un cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="3ea12-103">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="3ea12-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ea12-104">SYNTAX</span></span>

### <span data-ttu-id="3ea12-105">Interrompi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3ea12-105">Stop (Default)</span></span>
```
Stop-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3ea12-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3ea12-106">StopViaIdentity</span></span>
```
Stop-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3ea12-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ea12-107">DESCRIPTION</span></span>
<span data-ttu-id="3ea12-108">Arresta un cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="3ea12-108">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="3ea12-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ea12-109">EXAMPLES</span></span>

### <span data-ttu-id="3ea12-110">Esempio 1: arrestare un cluster kusto</span><span class="sxs-lookup"><span data-stu-id="3ea12-110">Example 1: Stop a Kusto cluster</span></span>
```powershell
PS C:\> Stop-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="3ea12-111">Il comando precedente arresta un cluster kusto</span><span class="sxs-lookup"><span data-stu-id="3ea12-111">The above command stops a Kusto cluster</span></span>

## <span data-ttu-id="3ea12-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ea12-112">PARAMETERS</span></span>

### <span data-ttu-id="3ea12-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ea12-113">-AsJob</span></span>
<span data-ttu-id="3ea12-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="3ea12-114">Run the command as a job</span></span>

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

### <span data-ttu-id="3ea12-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea12-115">-DefaultProfile</span></span>
<span data-ttu-id="3ea12-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ea12-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ea12-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ea12-117">-InputObject</span></span>
<span data-ttu-id="3ea12-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3ea12-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3ea12-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ea12-119">-Name</span></span>
<span data-ttu-id="3ea12-120">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="3ea12-120">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="3ea12-121">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="3ea12-121">-NoWait</span></span>
<span data-ttu-id="3ea12-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="3ea12-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3ea12-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ea12-123">-PassThru</span></span>
<span data-ttu-id="3ea12-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="3ea12-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3ea12-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ea12-125">-ResourceGroupName</span></span>
<span data-ttu-id="3ea12-126">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="3ea12-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="3ea12-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ea12-127">-SubscriptionId</span></span>
<span data-ttu-id="3ea12-128">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3ea12-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3ea12-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3ea12-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3ea12-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3ea12-130">-Confirm</span></span>
<span data-ttu-id="3ea12-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ea12-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ea12-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ea12-132">-WhatIf</span></span>
<span data-ttu-id="3ea12-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ea12-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ea12-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ea12-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ea12-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea12-135">CommonParameters</span></span>
<span data-ttu-id="3ea12-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ea12-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea12-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ea12-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea12-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ea12-138">INPUTS</span></span>

### <span data-ttu-id="3ea12-139">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="3ea12-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="3ea12-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ea12-140">OUTPUTS</span></span>

### <span data-ttu-id="3ea12-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ea12-141">System.Boolean</span></span>

## <span data-ttu-id="3ea12-142">Note</span><span class="sxs-lookup"><span data-stu-id="3ea12-142">NOTES</span></span>

<span data-ttu-id="3ea12-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3ea12-143">ALIASES</span></span>

<span data-ttu-id="3ea12-144">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ea12-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3ea12-145">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="3ea12-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3ea12-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3ea12-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3ea12-147">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="3ea12-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3ea12-148">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="3ea12-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="3ea12-149">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="3ea12-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="3ea12-150">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="3ea12-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="3ea12-151">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="3ea12-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="3ea12-152">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="3ea12-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3ea12-153">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3ea12-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="3ea12-154">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="3ea12-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="3ea12-155">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="3ea12-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="3ea12-156">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3ea12-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3ea12-157">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3ea12-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3ea12-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ea12-158">RELATED LINKS</span></span>

