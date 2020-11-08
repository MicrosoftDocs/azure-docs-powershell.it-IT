---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegateway
schema: 2.0.0
ms.openlocfilehash: a9c883fab422252aad167d92da3adf55edd9a78b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030087"
---
# <span data-ttu-id="a45b0-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="a45b0-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="a45b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a45b0-102">SYNOPSIS</span></span>
<span data-ttu-id="a45b0-103">Restituisce il gateway Edge richiesto.</span><span class="sxs-lookup"><span data-stu-id="a45b0-103">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="a45b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a45b0-104">SYNTAX</span></span>

### <span data-ttu-id="a45b0-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a45b0-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="a45b0-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="a45b0-106">Get</span></span>
```
Get-AzsEdgeGateway -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="a45b0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a45b0-107">GetViaIdentity</span></span>
```
Get-AzsEdgeGateway -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="a45b0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a45b0-108">DESCRIPTION</span></span>
<span data-ttu-id="a45b0-109">Restituisce il gateway Edge richiesto.</span><span class="sxs-lookup"><span data-stu-id="a45b0-109">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="a45b0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a45b0-110">EXAMPLES</span></span>

### <span data-ttu-id="a45b0-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="a45b0-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsEdgeGateway

Get a list of all edge gateways.
```

<span data-ttu-id="a45b0-112">Restituisce l'elenco di tutti i gateway di Edge in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="a45b0-112">Returns the list of all edge gateways at a certain location.</span></span>


## <span data-ttu-id="a45b0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a45b0-113">PARAMETERS</span></span>

### <span data-ttu-id="a45b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a45b0-114">-DefaultProfile</span></span>
<span data-ttu-id="a45b0-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a45b0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a45b0-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="a45b0-116">-Filter</span></span>
<span data-ttu-id="a45b0-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="a45b0-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="a45b0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a45b0-118">-InputObject</span></span>
<span data-ttu-id="a45b0-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a45b0-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a45b0-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a45b0-120">-Location</span></span>
<span data-ttu-id="a45b0-121">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a45b0-121">Location of the resource.</span></span>

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

### <span data-ttu-id="a45b0-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a45b0-122">-Name</span></span>
<span data-ttu-id="a45b0-123">Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="a45b0-123">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="a45b0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a45b0-124">-PassThru</span></span>
<span data-ttu-id="a45b0-125">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="a45b0-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a45b0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a45b0-126">-ResourceGroupName</span></span>
<span data-ttu-id="a45b0-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a45b0-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="a45b0-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a45b0-128">-SubscriptionId</span></span>
<span data-ttu-id="a45b0-129">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a45b0-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a45b0-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a45b0-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a45b0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a45b0-131">CommonParameters</span></span>
<span data-ttu-id="a45b0-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a45b0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a45b0-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a45b0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a45b0-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a45b0-134">INPUTS</span></span>

### <span data-ttu-id="a45b0-135">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="a45b0-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="a45b0-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a45b0-136">OUTPUTS</span></span>

### <span data-ttu-id="a45b0-137">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="a45b0-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGateway</span></span>



## <span data-ttu-id="a45b0-138">Note</span><span class="sxs-lookup"><span data-stu-id="a45b0-138">NOTES</span></span>

<span data-ttu-id="a45b0-139">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a45b0-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a45b0-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a45b0-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a45b0-141">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a45b0-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a45b0-142">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a45b0-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="a45b0-143">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="a45b0-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="a45b0-144">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="a45b0-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="a45b0-145">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="a45b0-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="a45b0-146">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="a45b0-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="a45b0-147">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="a45b0-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="a45b0-148">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="a45b0-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a45b0-149">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="a45b0-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="a45b0-150">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="a45b0-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="a45b0-151">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a45b0-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="a45b0-152">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="a45b0-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="a45b0-153">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="a45b0-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="a45b0-154">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="a45b0-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="a45b0-155">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="a45b0-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="a45b0-156">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a45b0-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="a45b0-157">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="a45b0-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="a45b0-158">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="a45b0-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="a45b0-159">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="a45b0-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="a45b0-160">`[StoragePool <String>]`: Nome del pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a45b0-160">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="a45b0-161">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a45b0-161">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="a45b0-162">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a45b0-162">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a45b0-163">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a45b0-163">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a45b0-164">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a45b0-164">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="a45b0-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a45b0-165">RELATED LINKS</span></span>

