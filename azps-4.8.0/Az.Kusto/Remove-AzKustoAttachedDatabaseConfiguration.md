---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 9d38b9c3297dc950cc12d46189bc940e27877d8a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031681"
---
# <span data-ttu-id="0b4d2-101">Remove-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b4d2-101">Remove-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="0b4d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b4d2-102">SYNOPSIS</span></span>
<span data-ttu-id="0b4d2-103">Elimina la configurazione del database allegato con il nome indicato.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-103">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="0b4d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b4d2-104">SYNTAX</span></span>

### <span data-ttu-id="0b4d2-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0b4d2-105">Delete (Default)</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0b4d2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0b4d2-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0b4d2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b4d2-107">DESCRIPTION</span></span>
<span data-ttu-id="0b4d2-108">Elimina la configurazione del database allegato con il nome indicato.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-108">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="0b4d2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b4d2-109">EXAMPLES</span></span>

### <span data-ttu-id="0b4d2-110">Esempio 1: eliminare un AttachedDatabaseConfiguration esistente per nome</span><span class="sxs-lookup"><span data-stu-id="0b4d2-110">Example 1: Delete an existing AttachedDatabaseConfiguration by name</span></span>
```powershell
PS C:\> Remove-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration"
```

<span data-ttu-id="0b4d2-111">Il comando precedente elimina il database di follower definito nel AttachedDatabaseConfiguration "myfollowerconfiguration" dal cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="0b4d2-111">The above command deletes the follower database defined in the AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="0b4d2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b4d2-112">PARAMETERS</span></span>

### <span data-ttu-id="0b4d2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b4d2-113">-AsJob</span></span>
<span data-ttu-id="0b4d2-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="0b4d2-114">Run the command as a job</span></span>

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

### <span data-ttu-id="0b4d2-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="0b4d2-115">-ClusterName</span></span>
<span data-ttu-id="0b4d2-116">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b4d2-117">-DefaultProfile</span></span>
<span data-ttu-id="0b4d2-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b4d2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b4d2-119">-InputObject</span></span>
<span data-ttu-id="0b4d2-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d2-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b4d2-121">-Name</span></span>
<span data-ttu-id="0b4d2-122">Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-122">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d2-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="0b4d2-123">-NoWait</span></span>
<span data-ttu-id="0b4d2-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="0b4d2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0b4d2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b4d2-125">-PassThru</span></span>
<span data-ttu-id="0b4d2-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="0b4d2-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0b4d2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b4d2-127">-ResourceGroupName</span></span>
<span data-ttu-id="0b4d2-128">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-128">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d2-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b4d2-129">-SubscriptionId</span></span>
<span data-ttu-id="0b4d2-130">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0b4d2-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d2-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0b4d2-132">-Confirm</span></span>
<span data-ttu-id="0b4d2-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b4d2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b4d2-134">-WhatIf</span></span>
<span data-ttu-id="0b4d2-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b4d2-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b4d2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b4d2-137">CommonParameters</span></span>
<span data-ttu-id="0b4d2-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b4d2-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b4d2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b4d2-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b4d2-140">INPUTS</span></span>

### <span data-ttu-id="0b4d2-141">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="0b4d2-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0b4d2-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b4d2-142">OUTPUTS</span></span>

### <span data-ttu-id="0b4d2-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0b4d2-143">System.Boolean</span></span>

## <span data-ttu-id="0b4d2-144">Note</span><span class="sxs-lookup"><span data-stu-id="0b4d2-144">NOTES</span></span>

<span data-ttu-id="0b4d2-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0b4d2-145">ALIASES</span></span>

<span data-ttu-id="0b4d2-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b4d2-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0b4d2-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0b4d2-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0b4d2-149">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="0b4d2-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0b4d2-150">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0b4d2-151">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0b4d2-152">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0b4d2-153">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0b4d2-154">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="0b4d2-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0b4d2-155">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0b4d2-156">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0b4d2-157">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0b4d2-158">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0b4d2-159">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="0b4d2-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0b4d2-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b4d2-160">RELATED LINKS</span></span>

