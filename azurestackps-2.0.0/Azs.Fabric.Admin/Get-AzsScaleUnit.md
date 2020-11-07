---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsscaleunit
schema: 2.0.0
ms.openlocfilehash: cef23066fe1bfcd0b428302aab6c8077a8f676b6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863945"
---
# <span data-ttu-id="c7e0e-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c7e0e-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="c7e0e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7e0e-102">SYNOPSIS</span></span>
<span data-ttu-id="c7e0e-103">Restituisce l'unità di scala richiesta.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-103">Returns the requested scale unit.</span></span>

## <span data-ttu-id="c7e0e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7e0e-104">SYNTAX</span></span>

### <span data-ttu-id="c7e0e-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c7e0e-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="c7e0e-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="c7e0e-106">Get</span></span>
```
Get-AzsScaleUnit -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="c7e0e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c7e0e-107">GetViaIdentity</span></span>
```
Get-AzsScaleUnit -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="c7e0e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7e0e-108">DESCRIPTION</span></span>
<span data-ttu-id="c7e0e-109">Restituisce l'unità di scala richiesta.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-109">Returns the requested scale unit.</span></span>

## <span data-ttu-id="c7e0e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7e0e-110">EXAMPLES</span></span>

### <span data-ttu-id="c7e0e-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="c7e0e-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsScaleUnit

A list of information about scale units.
```

<span data-ttu-id="c7e0e-112">Restituisce un elenco di informazioni sulle unità di misura.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="c7e0e-113">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="c7e0e-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsScaleUnit -Name "S-Cluster"

The information about a specific scale unit.
```

<span data-ttu-id="c7e0e-114">Restituire informazioni su un'unità di misura specifica.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="c7e0e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7e0e-115">PARAMETERS</span></span>

### <span data-ttu-id="c7e0e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7e0e-116">-DefaultProfile</span></span>
<span data-ttu-id="c7e0e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7e0e-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="c7e0e-118">-Filter</span></span>
<span data-ttu-id="c7e0e-119">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="c7e0e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7e0e-120">-InputObject</span></span>
<span data-ttu-id="c7e0e-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c7e0e-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c7e0e-122">-Location</span></span>
<span data-ttu-id="c7e0e-123">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-123">Location of the resource.</span></span>

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

### <span data-ttu-id="c7e0e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7e0e-124">-Name</span></span>
<span data-ttu-id="c7e0e-125">Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-125">Name of the scale units.</span></span>

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

### <span data-ttu-id="c7e0e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7e0e-126">-PassThru</span></span>
<span data-ttu-id="c7e0e-127">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="c7e0e-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c7e0e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7e0e-128">-ResourceGroupName</span></span>
<span data-ttu-id="c7e0e-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="c7e0e-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7e0e-130">-SubscriptionId</span></span>
<span data-ttu-id="c7e0e-131">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c7e0e-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-132">The subscription ID forms part of the URI for every service call.</span></span>


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

### <span data-ttu-id="c7e0e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7e0e-133">CommonParameters</span></span>
<span data-ttu-id="c7e0e-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7e0e-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7e0e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7e0e-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7e0e-136">INPUTS</span></span>

### <span data-ttu-id="c7e0e-137">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c7e0e-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="c7e0e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7e0e-138">OUTPUTS</span></span>

### <span data-ttu-id="c7e0e-139">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c7e0e-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleUnit</span></span>



## <span data-ttu-id="c7e0e-140">Note</span><span class="sxs-lookup"><span data-stu-id="c7e0e-140">NOTES</span></span>

<span data-ttu-id="c7e0e-141">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c7e0e-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c7e0e-143">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="c7e0e-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c7e0e-144">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="c7e0e-145">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="c7e0e-146">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="c7e0e-147">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="c7e0e-148">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="c7e0e-149">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="c7e0e-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="c7e0e-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c7e0e-151">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="c7e0e-152">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="c7e0e-153">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="c7e0e-154">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="c7e0e-155">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="c7e0e-156">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="c7e0e-157">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="c7e0e-158">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="c7e0e-159">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="c7e0e-160">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="c7e0e-161">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="c7e0e-162">`[StoragePool <String>]`: Nome del pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="c7e0e-163">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="c7e0e-164">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c7e0e-165">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c7e0e-166">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c7e0e-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="c7e0e-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7e0e-167">RELATED LINKS</span></span>

