---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: c04cbc2a92e6fa80c718cb32d95cc4059e4e3a6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031677"
---
# <span data-ttu-id="80d62-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="80d62-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="80d62-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80d62-102">SYNOPSIS</span></span>
<span data-ttu-id="80d62-103">Elimina la connessione dati con il nome indicato.</span><span class="sxs-lookup"><span data-stu-id="80d62-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="80d62-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80d62-104">SYNTAX</span></span>

### <span data-ttu-id="80d62-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="80d62-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="80d62-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="80d62-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="80d62-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80d62-107">DESCRIPTION</span></span>
<span data-ttu-id="80d62-108">Elimina la connessione dati con il nome indicato.</span><span class="sxs-lookup"><span data-stu-id="80d62-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="80d62-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80d62-109">EXAMPLES</span></span>

### <span data-ttu-id="80d62-110">Esempio 1: eliminare una connessione dati esistente per nome</span><span class="sxs-lookup"><span data-stu-id="80d62-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="80d62-111">Il comando precedente elimina la connessione dati denominata "mykustodataconnection" nel database "mykustodatabase" del cluster esistente "testnewkustocluster" disponibile nel gruppo di risorse "testrg"</span><span class="sxs-lookup"><span data-stu-id="80d62-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="80d62-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80d62-112">PARAMETERS</span></span>

### <span data-ttu-id="80d62-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80d62-113">-AsJob</span></span>
<span data-ttu-id="80d62-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="80d62-114">Run the command as a job</span></span>

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

### <span data-ttu-id="80d62-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="80d62-115">-ClusterName</span></span>
<span data-ttu-id="80d62-116">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="80d62-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="80d62-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="80d62-117">-DatabaseName</span></span>
<span data-ttu-id="80d62-118">Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="80d62-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="80d62-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80d62-119">-DefaultProfile</span></span>
<span data-ttu-id="80d62-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80d62-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80d62-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80d62-121">-InputObject</span></span>
<span data-ttu-id="80d62-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="80d62-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="80d62-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="80d62-123">-Name</span></span>
<span data-ttu-id="80d62-124">Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="80d62-124">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d62-125">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="80d62-125">-NoWait</span></span>
<span data-ttu-id="80d62-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="80d62-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="80d62-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80d62-127">-PassThru</span></span>
<span data-ttu-id="80d62-128">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="80d62-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="80d62-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80d62-129">-ResourceGroupName</span></span>
<span data-ttu-id="80d62-130">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="80d62-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="80d62-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80d62-131">-SubscriptionId</span></span>
<span data-ttu-id="80d62-132">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="80d62-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="80d62-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="80d62-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="80d62-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="80d62-134">-Confirm</span></span>
<span data-ttu-id="80d62-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80d62-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80d62-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80d62-136">-WhatIf</span></span>
<span data-ttu-id="80d62-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80d62-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80d62-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80d62-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80d62-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d62-139">CommonParameters</span></span>
<span data-ttu-id="80d62-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80d62-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d62-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80d62-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d62-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80d62-142">INPUTS</span></span>

### <span data-ttu-id="80d62-143">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="80d62-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="80d62-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80d62-144">OUTPUTS</span></span>

### <span data-ttu-id="80d62-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="80d62-145">System.Boolean</span></span>

## <span data-ttu-id="80d62-146">Note</span><span class="sxs-lookup"><span data-stu-id="80d62-146">NOTES</span></span>

<span data-ttu-id="80d62-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="80d62-147">ALIASES</span></span>

<span data-ttu-id="80d62-148">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80d62-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="80d62-149">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="80d62-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80d62-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="80d62-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="80d62-151">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="80d62-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="80d62-152">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="80d62-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="80d62-153">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="80d62-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="80d62-154">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="80d62-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="80d62-155">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="80d62-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="80d62-156">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="80d62-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="80d62-157">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="80d62-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="80d62-158">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="80d62-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="80d62-159">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="80d62-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="80d62-160">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="80d62-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="80d62-161">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="80d62-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="80d62-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80d62-162">RELATED LINKS</span></span>

