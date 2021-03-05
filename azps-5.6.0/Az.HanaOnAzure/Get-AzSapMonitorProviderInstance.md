---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 66f5a875f05b9c5d2fcdcc8a63eba9d149a9ba7a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013373"
---
# <span data-ttu-id="a1c5d-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="a1c5d-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="a1c5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1c5d-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c5d-103">Ottiene le proprietà di un'istanza del provider per la sottoscrizione, il gruppo di risorse, il nome SapMonitor e il nome della risorsa specificati.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="a1c5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1c5d-104">SYNTAX</span></span>

### <span data-ttu-id="a1c5d-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1c5d-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a1c5d-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="a1c5d-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a1c5d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a1c5d-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1c5d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a1c5d-108">DESCRIPTION</span></span>
<span data-ttu-id="a1c5d-109">Ottiene le proprietà di un'istanza del provider per la sottoscrizione, il gruppo di risorse, il nome SapMonitor e il nome della risorsa specificati.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="a1c5d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1c5d-110">EXAMPLES</span></span>

### <span data-ttu-id="a1c5d-111">Esempio 1: Ottenere tutte le istanze in un monitor SAP</span><span class="sxs-lookup"><span data-stu-id="a1c5d-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="a1c5d-112">Questo comando recupera tutte le istanze in un monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="a1c5d-113">Esempio 2: Ottenere un'istanza di un monitor SAP in base al nome</span><span class="sxs-lookup"><span data-stu-id="a1c5d-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="a1c5d-114">Questo comando recupera un'istanza di monitor SAP in base al nome.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="a1c5d-115">Esempio 3: Ottenere un'istanza di un monitor SAP per oggetto</span><span class="sxs-lookup"><span data-stu-id="a1c5d-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="a1c5d-116">Questo comando recupera un'istanza di sap monitor per oggetto.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="a1c5d-117">Esempio 4: Ottenere un'istanza di monitor SAP tramite pipeline</span><span class="sxs-lookup"><span data-stu-id="a1c5d-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="a1c5d-118">Questo comando recupera un'istanza di monitor SAP tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="a1c5d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1c5d-119">PARAMETERS</span></span>

### <span data-ttu-id="a1c5d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c5d-120">-DefaultProfile</span></span>
<span data-ttu-id="a1c5d-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1c5d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1c5d-122">-InputObject</span></span>
<span data-ttu-id="a1c5d-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c5d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a1c5d-124">-Name</span></span>
<span data-ttu-id="a1c5d-125">Nome dell'istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-125">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c5d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1c5d-126">-ResourceGroupName</span></span>
<span data-ttu-id="a1c5d-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-127">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c5d-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="a1c5d-128">-SapMonitorName</span></span>
<span data-ttu-id="a1c5d-129">Nome della risorsa monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-129">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c5d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a1c5d-130">-SubscriptionId</span></span>
<span data-ttu-id="a1c5d-131">ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a1c5d-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c5d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c5d-133">CommonParameters</span></span>
<span data-ttu-id="a1c5d-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c5d-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c5d-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="a1c5d-136">INPUTS</span></span>

### <span data-ttu-id="a1c5d-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="a1c5d-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="a1c5d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1c5d-138">OUTPUTS</span></span>

### <span data-ttu-id="a1c5d-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="a1c5d-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="a1c5d-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="a1c5d-140">NOTES</span></span>

<span data-ttu-id="a1c5d-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a1c5d-141">ALIASES</span></span>

<span data-ttu-id="a1c5d-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="a1c5d-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a1c5d-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a1c5d-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a1c5d-145">INPUTOBJECT <IHanaOnAzureIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a1c5d-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a1c5d-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="a1c5d-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a1c5d-147">`[Location <String>]`: posizione del vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="a1c5d-148">`[OperationKind <AccessPolicyUpdateKind?>]`: nome dell'operazione</span><span class="sxs-lookup"><span data-stu-id="a1c5d-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="a1c5d-149">`[ProviderInstanceName <String>]`: nome dell'istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="a1c5d-150">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="a1c5d-151">`[ResourceName <String>]`: nome della risorsa di identità.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="a1c5d-152">`[SapMonitorName <String>]`: nome della risorsa monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="a1c5d-153">`[Scope <String>]`: ambito del provider di risorse della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="a1c5d-154">Risorsa padre estesa da Identità gestite.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="a1c5d-155">`[SubscriptionId <String>]`: ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a1c5d-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a1c5d-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a1c5d-157">`[VaultName <String>]`: nome del vault</span><span class="sxs-lookup"><span data-stu-id="a1c5d-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="a1c5d-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1c5d-158">RELATED LINKS</span></span>

