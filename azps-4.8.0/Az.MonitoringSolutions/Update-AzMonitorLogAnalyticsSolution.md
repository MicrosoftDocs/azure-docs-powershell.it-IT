---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/update-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a39f347497fe6be31ccb26ce1f726d1eebe155e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191437"
---
# <span data-ttu-id="a38de-101">Update-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="a38de-101">Update-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="a38de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a38de-102">SYNOPSIS</span></span>
<span data-ttu-id="a38de-103">Aggiornare i tag di una soluzione.</span><span class="sxs-lookup"><span data-stu-id="a38de-103">Update the tags of a solution.</span></span>

## <span data-ttu-id="a38de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a38de-104">SYNTAX</span></span>

### <span data-ttu-id="a38de-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a38de-105">UpdateExpanded (Default)</span></span>
```
Update-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a38de-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a38de-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a38de-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a38de-107">DESCRIPTION</span></span>
<span data-ttu-id="a38de-108">Aggiornare i tag di una soluzione.</span><span class="sxs-lookup"><span data-stu-id="a38de-108">Update the tags of a solution.</span></span>

## <span data-ttu-id="a38de-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a38de-109">EXAMPLES</span></span>

### <span data-ttu-id="a38de-110">Esempio 1: aggiornare una soluzione di analisi del log di monitoraggio per nome</span><span class="sxs-lookup"><span data-stu-id="a38de-110">Example 1: Update a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Update-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)' -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="a38de-111">Questo comando aggiorna una soluzione di analisi del log di monitoraggio per nome.</span><span class="sxs-lookup"><span data-stu-id="a38de-111">This command updates a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="a38de-112">Esempio 2: aggiornare una soluzione di analisi del log di monitoraggio per oggetto</span><span class="sxs-lookup"><span data-stu-id="a38de-112">Example 2: Update a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'
PS C:\> Update-AzMonitorLogAnalyticsSolution -InputObject $monitor -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="a38de-113">Questo comando aggiorna una soluzione di analisi del log di monitoraggio per oggetto.</span><span class="sxs-lookup"><span data-stu-id="a38de-113">This command updates a monitor log analytics solution by object.</span></span>

## <span data-ttu-id="a38de-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a38de-114">PARAMETERS</span></span>

### <span data-ttu-id="a38de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a38de-115">-DefaultProfile</span></span>
<span data-ttu-id="a38de-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a38de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a38de-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a38de-117">-InputObject</span></span>
<span data-ttu-id="a38de-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a38de-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a38de-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a38de-119">-Name</span></span>
<span data-ttu-id="a38de-120">Nome soluzione utente.</span><span class="sxs-lookup"><span data-stu-id="a38de-120">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a38de-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a38de-121">-ResourceGroupName</span></span>
<span data-ttu-id="a38de-122">Nome del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a38de-122">The name of the resource group to get.</span></span>
<span data-ttu-id="a38de-123">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a38de-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a38de-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a38de-124">-SubscriptionId</span></span>
<span data-ttu-id="a38de-125">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a38de-125">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a38de-126">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a38de-126">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a38de-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="a38de-127">-Tag</span></span>
<span data-ttu-id="a38de-128">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="a38de-128">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a38de-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a38de-129">-Confirm</span></span>
<span data-ttu-id="a38de-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a38de-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a38de-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a38de-131">-WhatIf</span></span>
<span data-ttu-id="a38de-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a38de-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a38de-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a38de-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a38de-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a38de-134">CommonParameters</span></span>
<span data-ttu-id="a38de-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a38de-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a38de-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a38de-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a38de-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a38de-137">INPUTS</span></span>

### <span data-ttu-id="a38de-138">Microsoft. Azure. PowerShell. Cmdlets. MonitoringSolutions. Models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="a38de-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="a38de-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a38de-139">OUTPUTS</span></span>

### <span data-ttu-id="a38de-140">Microsoft. Azure. PowerShell. Cmdlets. MonitoringSolutions. Models. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="a38de-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="a38de-141">Note</span><span class="sxs-lookup"><span data-stu-id="a38de-141">NOTES</span></span>

<span data-ttu-id="a38de-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a38de-142">ALIASES</span></span>

<span data-ttu-id="a38de-143">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a38de-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a38de-144">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a38de-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a38de-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a38de-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a38de-146">INPUTOBJECT <IMonitoringSolutionsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a38de-146">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a38de-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="a38de-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a38de-148">`[ManagementAssociationName <String>]`: Nome ManagementAssociation utente.</span><span class="sxs-lookup"><span data-stu-id="a38de-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="a38de-149">`[ManagementConfigurationName <String>]`: Nome configurazione gestione utenti.</span><span class="sxs-lookup"><span data-stu-id="a38de-149">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="a38de-150">`[ProviderName <String>]`: Nome provider per la risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="a38de-150">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="a38de-151">`[ResourceGroupName <String>]`: Nome del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a38de-151">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="a38de-152">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a38de-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="a38de-153">`[ResourceName <String>]`: Nome risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="a38de-153">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="a38de-154">`[ResourceType <String>]`: Tipo di risorsa per la risorsa padre</span><span class="sxs-lookup"><span data-stu-id="a38de-154">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="a38de-155">`[SolutionName <String>]`: Nome soluzione utente.</span><span class="sxs-lookup"><span data-stu-id="a38de-155">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="a38de-156">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a38de-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a38de-157">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a38de-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a38de-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a38de-158">RELATED LINKS</span></span>

