---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsippool
schema: 2.0.0
ms.openlocfilehash: 532dcd2a91591b639b93b5b67851a4118457068b
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023226"
---
# <span data-ttu-id="cae49-101">Get-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="cae49-101">Get-AzsIPPool</span></span>

## <span data-ttu-id="cae49-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cae49-102">SYNOPSIS</span></span>
<span data-ttu-id="cae49-103">Restituire il pool IP richiesto.</span><span class="sxs-lookup"><span data-stu-id="cae49-103">Return the requested IP pool.</span></span>

## <span data-ttu-id="cae49-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cae49-104">SYNTAX</span></span>

### <span data-ttu-id="cae49-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cae49-105">List (Default)</span></span>
```
Get-AzsIPPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="cae49-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="cae49-106">Get</span></span>
```
Get-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="cae49-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cae49-107">GetViaIdentity</span></span>
```
Get-AzsIPPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="cae49-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cae49-108">DESCRIPTION</span></span>
<span data-ttu-id="cae49-109">Restituire il pool IP richiesto.</span><span class="sxs-lookup"><span data-stu-id="cae49-109">Return the requested IP pool.</span></span>

## <span data-ttu-id="cae49-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cae49-110">EXAMPLES</span></span>

### <span data-ttu-id="cae49-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="cae49-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsIpPool

Return an all infrastructure ip pools.
```

<span data-ttu-id="cae49-112">Ottenere tutti i pool IP dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cae49-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="cae49-113">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="cae49-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"

Get an infrastructure ip pool based on name.
```

<span data-ttu-id="cae49-114">Ottenere un pool IP dell'infrastruttura in base al nome.</span><span class="sxs-lookup"><span data-stu-id="cae49-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="cae49-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cae49-115">PARAMETERS</span></span>

### <span data-ttu-id="cae49-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae49-116">-DefaultProfile</span></span>


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

### <span data-ttu-id="cae49-117">-Filtro</span><span class="sxs-lookup"><span data-stu-id="cae49-117">-Filter</span></span>
<span data-ttu-id="cae49-118">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="cae49-118">OData filter parameter.</span></span>

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

### <span data-ttu-id="cae49-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cae49-119">-InputObject</span></span>
<span data-ttu-id="cae49-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cae49-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cae49-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="cae49-121">-Location</span></span>
<span data-ttu-id="cae49-122">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cae49-122">Location of the resource.</span></span>

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

### <span data-ttu-id="cae49-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="cae49-123">-Name</span></span>
<span data-ttu-id="cae49-124">Nome del pool IP.</span><span class="sxs-lookup"><span data-stu-id="cae49-124">IP pool name.</span></span>

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

### <span data-ttu-id="cae49-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cae49-125">-PassThru</span></span>
<span data-ttu-id="cae49-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="cae49-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cae49-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cae49-127">-ResourceGroupName</span></span>
<span data-ttu-id="cae49-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cae49-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="cae49-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cae49-129">-SubscriptionId</span></span>
<span data-ttu-id="cae49-130">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cae49-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cae49-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cae49-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cae49-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae49-132">CommonParameters</span></span>
<span data-ttu-id="cae49-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cae49-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae49-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cae49-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae49-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cae49-135">INPUTS</span></span>

### <span data-ttu-id="cae49-136">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="cae49-136">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="cae49-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cae49-137">OUTPUTS</span></span>

### <span data-ttu-id="cae49-138">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="cae49-138">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="cae49-139">Note</span><span class="sxs-lookup"><span data-stu-id="cae49-139">NOTES</span></span>

<span data-ttu-id="cae49-140">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cae49-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cae49-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cae49-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cae49-142">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="cae49-142">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cae49-143">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cae49-143">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="cae49-144">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="cae49-144">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="cae49-145">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="cae49-145">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="cae49-146">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="cae49-146">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="cae49-147">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="cae49-147">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="cae49-148">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="cae49-148">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="cae49-149">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="cae49-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cae49-150">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cae49-150">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="cae49-151">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cae49-151">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="cae49-152">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cae49-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="cae49-153">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="cae49-153">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="cae49-154">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="cae49-154">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="cae49-155">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="cae49-155">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="cae49-156">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="cae49-156">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="cae49-157">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cae49-157">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="cae49-158">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="cae49-158">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="cae49-159">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="cae49-159">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="cae49-160">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="cae49-160">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="cae49-161">`[StoragePool <String>]`: Nome del pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cae49-161">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="cae49-162">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cae49-162">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="cae49-163">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cae49-163">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cae49-164">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cae49-164">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cae49-165">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cae49-165">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="cae49-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cae49-166">RELATED LINKS</span></span>

