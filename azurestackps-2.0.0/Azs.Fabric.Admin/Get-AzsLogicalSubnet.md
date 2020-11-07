---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azslogicalsubnet
schema: 2.0.0
ms.openlocfilehash: eae4d8e861b6b229cfa3e5fe9b4e424a69c487c2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863946"
---
# <span data-ttu-id="a886d-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="a886d-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="a886d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a886d-102">SYNOPSIS</span></span>
<span data-ttu-id="a886d-103">Restituisce la subnet logica richiesta.</span><span class="sxs-lookup"><span data-stu-id="a886d-103">Returns the requested logical subnet.</span></span>

## <span data-ttu-id="a886d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a886d-104">SYNTAX</span></span>

### <span data-ttu-id="a886d-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a886d-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="a886d-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="a886d-106">Get</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="a886d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a886d-107">GetViaIdentity</span></span>
```
Get-AzsLogicalSubnet -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="a886d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a886d-108">DESCRIPTION</span></span>
<span data-ttu-id="a886d-109">Restituisce la subnet logica richiesta.</span><span class="sxs-lookup"><span data-stu-id="a886d-109">Returns the requested logical subnet.</span></span>

## <span data-ttu-id="a886d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a886d-110">EXAMPLES</span></span>

### <span data-ttu-id="a886d-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="a886d-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork

A list of all logical networks at a location.
```

<span data-ttu-id="a886d-112">Ottenere tutte le reti logiche in una posizione.</span><span class="sxs-lookup"><span data-stu-id="a886d-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="a886d-113">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="a886d-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"

A a specific logical networks at a location based on a name.
```

<span data-ttu-id="a886d-114">Ottenere una rete logica specifica in una posizione basata su un nome.</span><span class="sxs-lookup"><span data-stu-id="a886d-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="a886d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a886d-115">PARAMETERS</span></span>

### <span data-ttu-id="a886d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a886d-116">-DefaultProfile</span></span>
<span data-ttu-id="a886d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a886d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a886d-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="a886d-118">-Filter</span></span>
<span data-ttu-id="a886d-119">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="a886d-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="a886d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a886d-120">-InputObject</span></span>
<span data-ttu-id="a886d-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a886d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a886d-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a886d-122">-Location</span></span>
<span data-ttu-id="a886d-123">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a886d-123">Location of the resource.</span></span>

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

### <span data-ttu-id="a886d-124">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="a886d-124">-LogicalNetwork</span></span>
<span data-ttu-id="a886d-125">Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="a886d-125">Name of the logical network.</span></span>

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

### <span data-ttu-id="a886d-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="a886d-126">-Name</span></span>
<span data-ttu-id="a886d-127">Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="a886d-127">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="a886d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a886d-128">-PassThru</span></span>
<span data-ttu-id="a886d-129">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="a886d-129">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a886d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a886d-130">-ResourceGroupName</span></span>
<span data-ttu-id="a886d-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a886d-131">Name of the resource group.</span></span>

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

### <span data-ttu-id="a886d-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a886d-132">-SubscriptionId</span></span>
<span data-ttu-id="a886d-133">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a886d-133">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a886d-134">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a886d-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a886d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a886d-135">CommonParameters</span></span>
<span data-ttu-id="a886d-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a886d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a886d-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a886d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a886d-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a886d-138">INPUTS</span></span>

### <span data-ttu-id="a886d-139">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="a886d-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="a886d-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a886d-140">OUTPUTS</span></span>

### <span data-ttu-id="a886d-141">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. ILogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="a886d-141">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.ILogicalSubnet</span></span>



## <span data-ttu-id="a886d-142">Note</span><span class="sxs-lookup"><span data-stu-id="a886d-142">NOTES</span></span>

<span data-ttu-id="a886d-143">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a886d-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a886d-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a886d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a886d-145">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a886d-145">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a886d-146">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a886d-146">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="a886d-147">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="a886d-147">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="a886d-148">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="a886d-148">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="a886d-149">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="a886d-149">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="a886d-150">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="a886d-150">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="a886d-151">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="a886d-151">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="a886d-152">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="a886d-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a886d-153">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="a886d-153">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="a886d-154">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="a886d-154">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="a886d-155">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a886d-155">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="a886d-156">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="a886d-156">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="a886d-157">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="a886d-157">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="a886d-158">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="a886d-158">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="a886d-159">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="a886d-159">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="a886d-160">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a886d-160">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="a886d-161">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="a886d-161">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="a886d-162">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="a886d-162">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="a886d-163">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="a886d-163">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="a886d-164">`[StoragePool <String>]`: Nome del pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a886d-164">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="a886d-165">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a886d-165">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="a886d-166">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a886d-166">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a886d-167">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a886d-167">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a886d-168">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a886d-168">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="a886d-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a886d-169">RELATED LINKS</span></span>

