---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 9d87cfff428a5c3c176bea4deff95d0c652dc45a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189715"
---
# <span data-ttu-id="ca783-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="ca783-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="ca783-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca783-102">SYNOPSIS</span></span>
<span data-ttu-id="ca783-103">Patch il campo Tags di un monitor SAP per l'abbonamento, il gruppo di risorse e il nome del monitor specificati.</span><span class="sxs-lookup"><span data-stu-id="ca783-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="ca783-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca783-104">SYNTAX</span></span>

### <span data-ttu-id="ca783-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ca783-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ca783-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ca783-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ca783-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca783-107">DESCRIPTION</span></span>
<span data-ttu-id="ca783-108">Patch il campo Tags di un monitor SAP per l'abbonamento, il gruppo di risorse e il nome del monitor specificati.</span><span class="sxs-lookup"><span data-stu-id="ca783-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="ca783-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca783-109">EXAMPLES</span></span>

### <span data-ttu-id="ca783-110">Esempio 1: aggiornare un monitor SAP per nome</span><span class="sxs-lookup"><span data-stu-id="ca783-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="ca783-111">Questo comando aggiorna un monitor SAP per nome.</span><span class="sxs-lookup"><span data-stu-id="ca783-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="ca783-112">Esempio 2: aggiornare un monitor SAP per oggetto</span><span class="sxs-lookup"><span data-stu-id="ca783-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="ca783-113">Questo comando aggiorna un monitor SAP per oggetto.</span><span class="sxs-lookup"><span data-stu-id="ca783-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="ca783-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca783-114">PARAMETERS</span></span>

### <span data-ttu-id="ca783-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca783-115">-DefaultProfile</span></span>
<span data-ttu-id="ca783-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca783-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca783-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca783-117">-InputObject</span></span>
<span data-ttu-id="ca783-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ca783-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca783-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca783-119">-Name</span></span>
<span data-ttu-id="ca783-120">Nome della risorsa monitoraggio SAP.</span><span class="sxs-lookup"><span data-stu-id="ca783-120">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca783-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca783-121">-ResourceGroupName</span></span>
<span data-ttu-id="ca783-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca783-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="ca783-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca783-123">-SubscriptionId</span></span>
<span data-ttu-id="ca783-124">ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ca783-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ca783-125">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ca783-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ca783-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="ca783-126">-Tag</span></span>
<span data-ttu-id="ca783-127">Campo tag della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ca783-127">Tags field of the resource.</span></span>

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

### <span data-ttu-id="ca783-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca783-128">-Confirm</span></span>
<span data-ttu-id="ca783-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca783-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca783-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca783-130">-WhatIf</span></span>
<span data-ttu-id="ca783-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca783-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca783-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca783-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca783-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca783-133">CommonParameters</span></span>
<span data-ttu-id="ca783-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca783-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca783-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca783-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca783-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca783-136">INPUTS</span></span>

### <span data-ttu-id="ca783-137">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="ca783-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="ca783-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca783-138">OUTPUTS</span></span>

### <span data-ttu-id="ca783-139">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="ca783-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="ca783-140">Note</span><span class="sxs-lookup"><span data-stu-id="ca783-140">NOTES</span></span>

<span data-ttu-id="ca783-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ca783-141">ALIASES</span></span>

<span data-ttu-id="ca783-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca783-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ca783-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ca783-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ca783-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ca783-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ca783-145">INPUTOBJECT <IHanaOnAzureIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ca783-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ca783-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="ca783-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ca783-147">`[Location <String>]`: La posizione del Vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="ca783-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="ca783-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Nome dell'operazione</span><span class="sxs-lookup"><span data-stu-id="ca783-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="ca783-149">`[ProviderInstanceName <String>]`: Nome dell'istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="ca783-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="ca783-150">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca783-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="ca783-151">`[ResourceName <String>]`: Il nome della risorsa identità.</span><span class="sxs-lookup"><span data-stu-id="ca783-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="ca783-152">`[SapMonitorName <String>]`: Nome della risorsa di monitoraggio SAP.</span><span class="sxs-lookup"><span data-stu-id="ca783-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="ca783-153">`[Scope <String>]`: L'ambito del provider di risorse della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ca783-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="ca783-154">Risorsa padre estesa da identità gestite.</span><span class="sxs-lookup"><span data-stu-id="ca783-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="ca783-155">`[SubscriptionId <String>]`: ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ca783-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ca783-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ca783-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ca783-157">`[VaultName <String>]`: Nome del Vault</span><span class="sxs-lookup"><span data-stu-id="ca783-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="ca783-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca783-158">RELATED LINKS</span></span>
