---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 1ec82e745c7f6521a62db80ca109078bb1681172
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475265"
---
# <span data-ttu-id="9ed7c-101">Get-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="9ed7c-101">Get-AzSapMonitor</span></span>

## <span data-ttu-id="9ed7c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9ed7c-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed7c-103">Ottiene le proprietà di un monitor SAP per l'abbonamento, il gruppo di risorse e il nome della risorsa specificati.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-103">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="9ed7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ed7c-104">SYNTAX</span></span>

### <span data-ttu-id="9ed7c-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9ed7c-105">List (Default)</span></span>
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9ed7c-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="9ed7c-106">Get</span></span>
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9ed7c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9ed7c-107">GetViaIdentity</span></span>
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9ed7c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ed7c-108">DESCRIPTION</span></span>
<span data-ttu-id="9ed7c-109">Ottiene le proprietà di un monitor SAP per l'abbonamento, il gruppo di risorse e il nome della risorsa specificati.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-109">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="9ed7c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ed7c-110">EXAMPLES</span></span>

### <span data-ttu-id="9ed7c-111">Esempio 1: ottenere tutti i monitoraggi SAP in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="9ed7c-111">Example 1: Get all SAP monitors under a subscription</span></span>
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="9ed7c-112">Questo comando consente di ottenere monitoraggi SAP in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-112">This command gets SAP monitors under a subscription.</span></span>

### <span data-ttu-id="9ed7c-113">Esempio 2: ottenere un monitor SAP per nome</span><span class="sxs-lookup"><span data-stu-id="9ed7c-113">Example 2: Get a SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="9ed7c-114">Questo comando ottiene un monitor SAP per nome.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-114">This command gets a SAP monitor by name.</span></span>

### <span data-ttu-id="9ed7c-115">Esempio 3: ottenere un monitor SAP per oggetto</span><span class="sxs-lookup"><span data-stu-id="9ed7c-115">Example 3: Get a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="9ed7c-116">Questo comando ottiene un monitor SAP per oggetto.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-116">This command gets a SAP monitor by object.</span></span>

### <span data-ttu-id="9ed7c-117">Esempio 4: ottenere un monitor SAP tramite pipeline</span><span class="sxs-lookup"><span data-stu-id="9ed7c-117">Example 4: Get a SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="9ed7c-118">Questo comando ottiene un monitor SAP tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-118">This command gets a SAP monitor by pipeline.</span></span>

## <span data-ttu-id="9ed7c-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9ed7c-119">PARAMETERS</span></span>

### <span data-ttu-id="9ed7c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed7c-120">-DefaultProfile</span></span>
<span data-ttu-id="9ed7c-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ed7c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ed7c-122">-InputObject</span></span>
<span data-ttu-id="9ed7c-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9ed7c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ed7c-124">-Name</span></span>
<span data-ttu-id="9ed7c-125">Nome della risorsa monitoraggio SAP.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-125">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ed7c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ed7c-126">-ResourceGroupName</span></span>
<span data-ttu-id="9ed7c-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-127">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ed7c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ed7c-128">-SubscriptionId</span></span>
<span data-ttu-id="9ed7c-129">ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-129">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9ed7c-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9ed7c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed7c-131">CommonParameters</span></span>
<span data-ttu-id="9ed7c-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed7c-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ed7c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed7c-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9ed7c-134">INPUTS</span></span>

### <span data-ttu-id="9ed7c-135">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="9ed7c-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="9ed7c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ed7c-136">OUTPUTS</span></span>

### <span data-ttu-id="9ed7c-137">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="9ed7c-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="9ed7c-138">Note</span><span class="sxs-lookup"><span data-stu-id="9ed7c-138">NOTES</span></span>

<span data-ttu-id="9ed7c-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9ed7c-139">ALIASES</span></span>

<span data-ttu-id="9ed7c-140">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9ed7c-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9ed7c-141">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9ed7c-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9ed7c-143">INPUTOBJECT <IHanaOnAzureIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="9ed7c-143">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9ed7c-144">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="9ed7c-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9ed7c-145">`[Location <String>]`: La posizione del Vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-145">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="9ed7c-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Nome dell'operazione</span><span class="sxs-lookup"><span data-stu-id="9ed7c-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="9ed7c-147">`[ProviderInstanceName <String>]`: Nome dell'istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-147">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="9ed7c-148">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="9ed7c-149">`[ResourceName <String>]`: Il nome della risorsa identità.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-149">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="9ed7c-150">`[SapMonitorName <String>]`: Nome della risorsa di monitoraggio SAP.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-150">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="9ed7c-151">`[Scope <String>]`: L'ambito del provider di risorse della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-151">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="9ed7c-152">Risorsa padre estesa da identità gestite.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-152">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="9ed7c-153">`[SubscriptionId <String>]`: ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-153">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9ed7c-154">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9ed7c-155">`[VaultName <String>]`: Nome del Vault</span><span class="sxs-lookup"><span data-stu-id="9ed7c-155">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="9ed7c-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ed7c-156">RELATED LINKS</span></span>

