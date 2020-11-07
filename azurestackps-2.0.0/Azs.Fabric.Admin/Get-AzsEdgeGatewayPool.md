---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegatewaypool
schema: 2.0.0
ms.openlocfilehash: 79b4ae3a4bd3807b08ea45be9a9a328455f03b67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861782"
---
# <span data-ttu-id="3a790-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="3a790-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="3a790-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a790-102">SYNOPSIS</span></span>


## <span data-ttu-id="3a790-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a790-103">SYNTAX</span></span>

### <span data-ttu-id="3a790-104">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3a790-104">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="3a790-105">Ottieni</span><span class="sxs-lookup"><span data-stu-id="3a790-105">Get</span></span>
```
Get-AzsEdgeGatewayPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="3a790-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3a790-106">GetViaIdentity</span></span>
```
Get-AzsEdgeGatewayPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="3a790-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a790-107">DESCRIPTION</span></span>


## <span data-ttu-id="3a790-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a790-108">EXAMPLES</span></span>

### <span data-ttu-id="3a790-109">Esempio 1: ottenere un elenco di tutti i pool di gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="3a790-109">Example 1: Get a list of all Edge Gateway pools.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a list of all Edge Gateway pools.
```

<span data-ttu-id="3a790-110">Ottenere un elenco di tutti i pool di gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="3a790-110">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="3a790-111">Esempio 2: ottenere un pool di gateway Edge specifico.</span><span class="sxs-lookup"><span data-stu-id="3a790-111">Example 2: Get a specific edge gateway pool.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a specific edge gateway pool.
```

<span data-ttu-id="3a790-112">Ottenere un pool di gateway Edge specifico.</span><span class="sxs-lookup"><span data-stu-id="3a790-112">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="3a790-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a790-113">PARAMETERS</span></span>

### <span data-ttu-id="3a790-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a790-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="3a790-115">-Filtro</span><span class="sxs-lookup"><span data-stu-id="3a790-115">-Filter</span></span>


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

### <span data-ttu-id="3a790-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a790-116">-InputObject</span></span>
<span data-ttu-id="3a790-117">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3a790-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3a790-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3a790-118">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3a790-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a790-119">-Name</span></span>


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

### <span data-ttu-id="3a790-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a790-120">-PassThru</span></span>


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

### <span data-ttu-id="3a790-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a790-121">-ResourceGroupName</span></span>


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

### <span data-ttu-id="3a790-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a790-122">-SubscriptionId</span></span>


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

### <span data-ttu-id="3a790-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a790-123">CommonParameters</span></span>
<span data-ttu-id="3a790-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a790-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a790-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a790-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a790-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a790-126">INPUTS</span></span>

### <span data-ttu-id="3a790-127">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3a790-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="3a790-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a790-128">OUTPUTS</span></span>

### <span data-ttu-id="3a790-129">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="3a790-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGatewayPool</span></span>



## <span data-ttu-id="3a790-130">Note</span><span class="sxs-lookup"><span data-stu-id="3a790-130">NOTES</span></span>

<span data-ttu-id="3a790-131">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="3a790-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3a790-132">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3a790-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3a790-133">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="3a790-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="3a790-134">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3a790-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="3a790-135">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="3a790-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="3a790-136">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="3a790-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="3a790-137">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="3a790-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="3a790-138">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="3a790-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="3a790-139">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="3a790-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="3a790-140">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="3a790-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3a790-141">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="3a790-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="3a790-142">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="3a790-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="3a790-143">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3a790-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="3a790-144">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="3a790-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="3a790-145">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="3a790-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="3a790-146">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="3a790-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="3a790-147">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="3a790-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="3a790-148">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3a790-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="3a790-149">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="3a790-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="3a790-150">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="3a790-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="3a790-151">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="3a790-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="3a790-152">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3a790-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="3a790-153">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3a790-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3a790-154">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3a790-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3a790-155">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3a790-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="3a790-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a790-156">RELATED LINKS</span></span>

