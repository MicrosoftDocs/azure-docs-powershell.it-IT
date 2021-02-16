---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 9d87cfff428a5c3c176bea4deff95d0c652dc45a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185799"
---
# <span data-ttu-id="cb11a-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="cb11a-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="cb11a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb11a-102">SYNOPSIS</span></span>
<span data-ttu-id="cb11a-103">Patch del campo Contrassegni di un monitor SAP per la sottoscrizione, il gruppo di risorse e il nome del monitor specificati.</span><span class="sxs-lookup"><span data-stu-id="cb11a-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="cb11a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb11a-104">SYNTAX</span></span>

### <span data-ttu-id="cb11a-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cb11a-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cb11a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cb11a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cb11a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cb11a-107">DESCRIPTION</span></span>
<span data-ttu-id="cb11a-108">Patch del campo Contrassegni di un monitor SAP per la sottoscrizione, il gruppo di risorse e il nome del monitor specificati.</span><span class="sxs-lookup"><span data-stu-id="cb11a-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="cb11a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb11a-109">EXAMPLES</span></span>

### <span data-ttu-id="cb11a-110">Esempio 1: Aggiornare un monitor SAP in base al nome</span><span class="sxs-lookup"><span data-stu-id="cb11a-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="cb11a-111">Questo comando aggiorna un monitor SAP in base al nome.</span><span class="sxs-lookup"><span data-stu-id="cb11a-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="cb11a-112">Esempio 2: Aggiornare un monitor SAP in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="cb11a-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="cb11a-113">Questo comando aggiorna un monitor SAP in base all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cb11a-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="cb11a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb11a-114">PARAMETERS</span></span>

### <span data-ttu-id="cb11a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb11a-115">-DefaultProfile</span></span>
<span data-ttu-id="cb11a-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb11a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb11a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb11a-117">-InputObject</span></span>
<span data-ttu-id="cb11a-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cb11a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cb11a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cb11a-119">-Name</span></span>
<span data-ttu-id="cb11a-120">Nome della risorsa monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="cb11a-120">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="cb11a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb11a-121">-ResourceGroupName</span></span>
<span data-ttu-id="cb11a-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cb11a-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="cb11a-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb11a-123">-SubscriptionId</span></span>
<span data-ttu-id="cb11a-124">ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cb11a-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cb11a-125">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cb11a-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cb11a-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="cb11a-126">-Tag</span></span>
<span data-ttu-id="cb11a-127">Campo Contrassegni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cb11a-127">Tags field of the resource.</span></span>

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

### <span data-ttu-id="cb11a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb11a-128">-Confirm</span></span>
<span data-ttu-id="cb11a-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb11a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb11a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb11a-130">-WhatIf</span></span>
<span data-ttu-id="cb11a-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb11a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb11a-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb11a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb11a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb11a-133">CommonParameters</span></span>
<span data-ttu-id="cb11a-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb11a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb11a-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cb11a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb11a-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="cb11a-136">INPUTS</span></span>

### <span data-ttu-id="cb11a-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="cb11a-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="cb11a-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb11a-138">OUTPUTS</span></span>

### <span data-ttu-id="cb11a-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="cb11a-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="cb11a-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="cb11a-140">NOTES</span></span>

<span data-ttu-id="cb11a-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cb11a-141">ALIASES</span></span>

<span data-ttu-id="cb11a-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="cb11a-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cb11a-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cb11a-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb11a-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cb11a-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cb11a-145">INPUTOBJECT <IHanaOnAzureIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="cb11a-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cb11a-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="cb11a-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cb11a-147">`[Location <String>]`: posizione del vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="cb11a-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="cb11a-148">`[OperationKind <AccessPolicyUpdateKind?>]`: nome dell'operazione</span><span class="sxs-lookup"><span data-stu-id="cb11a-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="cb11a-149">`[ProviderInstanceName <String>]`: nome dell'istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="cb11a-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="cb11a-150">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cb11a-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="cb11a-151">`[ResourceName <String>]`: nome della risorsa di identità.</span><span class="sxs-lookup"><span data-stu-id="cb11a-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="cb11a-152">`[SapMonitorName <String>]`: nome della risorsa monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="cb11a-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="cb11a-153">`[Scope <String>]`: ambito del provider di risorse della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cb11a-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="cb11a-154">Risorsa padre estesa da Identità gestite.</span><span class="sxs-lookup"><span data-stu-id="cb11a-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="cb11a-155">`[SubscriptionId <String>]`: ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cb11a-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cb11a-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cb11a-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cb11a-157">`[VaultName <String>]`: nome del vault</span><span class="sxs-lookup"><span data-stu-id="cb11a-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="cb11a-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb11a-158">RELATED LINKS</span></span>

