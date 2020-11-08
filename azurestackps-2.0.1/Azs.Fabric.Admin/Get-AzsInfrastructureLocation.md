---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructurelocation
schema: 2.0.0
ms.openlocfilehash: 0d0f2856503943d19653dd09a8cb1c125fec9517
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023243"
---
# <span data-ttu-id="5b00d-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="5b00d-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="5b00d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b00d-102">SYNOPSIS</span></span>
<span data-ttu-id="5b00d-103">Restituisce il percorso del tessuto richiesto.</span><span class="sxs-lookup"><span data-stu-id="5b00d-103">Returns the requested fabric location.</span></span>

## <span data-ttu-id="5b00d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b00d-104">SYNTAX</span></span>

### <span data-ttu-id="5b00d-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b00d-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5b00d-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="5b00d-106">Get</span></span>
```
Get-AzsInfrastructureLocation -FabricLocation <String> [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="5b00d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5b00d-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureLocation -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="5b00d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b00d-108">DESCRIPTION</span></span>
<span data-ttu-id="5b00d-109">Restituisce il percorso del tessuto richiesto.</span><span class="sxs-lookup"><span data-stu-id="5b00d-109">Returns the requested fabric location.</span></span>

## <span data-ttu-id="5b00d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b00d-110">EXAMPLES</span></span>

### <span data-ttu-id="5b00d-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="5b00d-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation

Return a list of all fabric locations.
```

<span data-ttu-id="5b00d-112">Ottenere un elenco di tutte le posizioni in tessuto.</span><span class="sxs-lookup"><span data-stu-id="5b00d-112">Get a list of all fabric locations.</span></span>

### <span data-ttu-id="5b00d-113">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="5b00d-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation -Location "local"

Return a location based on the name.
```

<span data-ttu-id="5b00d-114">Ottenere una posizione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="5b00d-114">Get a location based on the name.</span></span>

## <span data-ttu-id="5b00d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b00d-115">PARAMETERS</span></span>

### <span data-ttu-id="5b00d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b00d-116">-DefaultProfile</span></span>
<span data-ttu-id="5b00d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b00d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b00d-118">-FabricLocation</span><span class="sxs-lookup"><span data-stu-id="5b00d-118">-FabricLocation</span></span>
<span data-ttu-id="5b00d-119">Posizione del tessuto.</span><span class="sxs-lookup"><span data-stu-id="5b00d-119">Fabric location.</span></span>

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

### <span data-ttu-id="5b00d-120">-Filtro</span><span class="sxs-lookup"><span data-stu-id="5b00d-120">-Filter</span></span>
<span data-ttu-id="5b00d-121">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="5b00d-121">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5b00d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b00d-122">-InputObject</span></span>
<span data-ttu-id="5b00d-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5b00d-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5b00d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b00d-124">-PassThru</span></span>
<span data-ttu-id="5b00d-125">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="5b00d-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5b00d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b00d-126">-ResourceGroupName</span></span>
<span data-ttu-id="5b00d-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5b00d-127">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5b00d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b00d-128">-SubscriptionId</span></span>
<span data-ttu-id="5b00d-129">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5b00d-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5b00d-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5b00d-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5b00d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b00d-131">CommonParameters</span></span>
<span data-ttu-id="5b00d-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b00d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b00d-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b00d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b00d-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b00d-134">INPUTS</span></span>

### <span data-ttu-id="5b00d-135">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5b00d-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="5b00d-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b00d-136">OUTPUTS</span></span>

### <span data-ttu-id="5b00d-137">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IFabricLocation</span><span class="sxs-lookup"><span data-stu-id="5b00d-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFabricLocation</span></span>



## <span data-ttu-id="5b00d-138">Note</span><span class="sxs-lookup"><span data-stu-id="5b00d-138">NOTES</span></span>

<span data-ttu-id="5b00d-139">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="5b00d-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5b00d-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5b00d-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5b00d-141">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="5b00d-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5b00d-142">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5b00d-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="5b00d-143">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="5b00d-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="5b00d-144">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="5b00d-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="5b00d-145">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="5b00d-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="5b00d-146">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="5b00d-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="5b00d-147">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="5b00d-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="5b00d-148">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="5b00d-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5b00d-149">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="5b00d-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="5b00d-150">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="5b00d-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="5b00d-151">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5b00d-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="5b00d-152">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="5b00d-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="5b00d-153">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="5b00d-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="5b00d-154">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="5b00d-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="5b00d-155">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="5b00d-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="5b00d-156">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5b00d-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="5b00d-157">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="5b00d-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="5b00d-158">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="5b00d-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="5b00d-159">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="5b00d-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="5b00d-160">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5b00d-160">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="5b00d-161">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5b00d-161">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5b00d-162">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5b00d-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5b00d-163">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5b00d-163">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="5b00d-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b00d-164">RELATED LINKS</span></span>

