---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 55ca24a7213dea4e9d0743689c080ebbb439430a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193300"
---
# <span data-ttu-id="40bc6-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="40bc6-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="40bc6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40bc6-102">SYNOPSIS</span></span>
<span data-ttu-id="40bc6-103">Ottiene le proprietà di un'istanza del provider per l'abbonamento, il gruppo di risorse, il nome SapMonitor e il nome della risorsa specificati.</span><span class="sxs-lookup"><span data-stu-id="40bc6-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="40bc6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40bc6-104">SYNTAX</span></span>

### <span data-ttu-id="40bc6-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="40bc6-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="40bc6-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="40bc6-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="40bc6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="40bc6-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="40bc6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40bc6-108">DESCRIPTION</span></span>
<span data-ttu-id="40bc6-109">Ottiene le proprietà di un'istanza del provider per l'abbonamento, il gruppo di risorse, il nome SapMonitor e il nome della risorsa specificati.</span><span class="sxs-lookup"><span data-stu-id="40bc6-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="40bc6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40bc6-110">EXAMPLES</span></span>

### <span data-ttu-id="40bc6-111">Esempio 1: ottenere tutte le istanze in un monitor SAP</span><span class="sxs-lookup"><span data-stu-id="40bc6-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="40bc6-112">Questo comando consente di ottenere tutte le istanze in un monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="40bc6-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="40bc6-113">Esempio 2: ottenere un'istanza di SAP monitor per nome</span><span class="sxs-lookup"><span data-stu-id="40bc6-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="40bc6-114">Questo comando consente di ottenere un'istanza di SAP monitor per nome.</span><span class="sxs-lookup"><span data-stu-id="40bc6-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="40bc6-115">Esempio 3: ottenere un'istanza di SAP monitor by Object</span><span class="sxs-lookup"><span data-stu-id="40bc6-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="40bc6-116">Questo comando consente di ottenere un'istanza di SAP monitor by Object.</span><span class="sxs-lookup"><span data-stu-id="40bc6-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="40bc6-117">Esempio 4: ottenere un'istanza di SAP monitor by pipeline</span><span class="sxs-lookup"><span data-stu-id="40bc6-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="40bc6-118">Questo comando consente di ottenere un'istanza di monitor SAP tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="40bc6-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="40bc6-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40bc6-119">PARAMETERS</span></span>

### <span data-ttu-id="40bc6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40bc6-120">-DefaultProfile</span></span>
<span data-ttu-id="40bc6-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40bc6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40bc6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40bc6-122">-InputObject</span></span>
<span data-ttu-id="40bc6-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="40bc6-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="40bc6-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="40bc6-124">-Name</span></span>
<span data-ttu-id="40bc6-125">Nome dell'istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="40bc6-125">Name of the provider instance.</span></span>

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

### <span data-ttu-id="40bc6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40bc6-126">-ResourceGroupName</span></span>
<span data-ttu-id="40bc6-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="40bc6-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="40bc6-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="40bc6-128">-SapMonitorName</span></span>
<span data-ttu-id="40bc6-129">Nome della risorsa monitoraggio SAP.</span><span class="sxs-lookup"><span data-stu-id="40bc6-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="40bc6-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40bc6-130">-SubscriptionId</span></span>
<span data-ttu-id="40bc6-131">ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="40bc6-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="40bc6-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="40bc6-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="40bc6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40bc6-133">CommonParameters</span></span>
<span data-ttu-id="40bc6-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40bc6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40bc6-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40bc6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40bc6-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40bc6-136">INPUTS</span></span>

### <span data-ttu-id="40bc6-137">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="40bc6-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="40bc6-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40bc6-138">OUTPUTS</span></span>

### <span data-ttu-id="40bc6-139">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="40bc6-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="40bc6-140">Note</span><span class="sxs-lookup"><span data-stu-id="40bc6-140">NOTES</span></span>

<span data-ttu-id="40bc6-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="40bc6-141">ALIASES</span></span>

<span data-ttu-id="40bc6-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40bc6-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="40bc6-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="40bc6-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="40bc6-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="40bc6-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="40bc6-145">INPUTOBJECT <IHanaOnAzureIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="40bc6-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="40bc6-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="40bc6-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="40bc6-147">`[Location <String>]`: La posizione del Vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="40bc6-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="40bc6-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Nome dell'operazione</span><span class="sxs-lookup"><span data-stu-id="40bc6-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="40bc6-149">`[ProviderInstanceName <String>]`: Nome dell'istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="40bc6-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="40bc6-150">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="40bc6-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="40bc6-151">`[ResourceName <String>]`: Il nome della risorsa identità.</span><span class="sxs-lookup"><span data-stu-id="40bc6-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="40bc6-152">`[SapMonitorName <String>]`: Nome della risorsa di monitoraggio SAP.</span><span class="sxs-lookup"><span data-stu-id="40bc6-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="40bc6-153">`[Scope <String>]`: L'ambito del provider di risorse della risorsa.</span><span class="sxs-lookup"><span data-stu-id="40bc6-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="40bc6-154">Risorsa padre estesa da identità gestite.</span><span class="sxs-lookup"><span data-stu-id="40bc6-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="40bc6-155">`[SubscriptionId <String>]`: ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="40bc6-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="40bc6-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="40bc6-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="40bc6-157">`[VaultName <String>]`: Nome del Vault</span><span class="sxs-lookup"><span data-stu-id="40bc6-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="40bc6-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40bc6-158">RELATED LINKS</span></span>
