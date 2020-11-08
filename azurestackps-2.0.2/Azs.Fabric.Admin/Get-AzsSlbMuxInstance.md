---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsslbmuxinstance
schema: 2.0.0
ms.openlocfilehash: 64e33236bbdd3f07969f6633356c98b593ee672f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030133"
---
# <span data-ttu-id="2274e-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="2274e-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="2274e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2274e-102">SYNOPSIS</span></span>
<span data-ttu-id="2274e-103">Restituisce l'istanza del multiplexer di bilanciamento del carico software richiesto.</span><span class="sxs-lookup"><span data-stu-id="2274e-103">Returns the requested software load balancer multiplexer instance.</span></span>

## <span data-ttu-id="2274e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2274e-104">SYNTAX</span></span>

### <span data-ttu-id="2274e-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2274e-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="2274e-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="2274e-106">Get</span></span>
```
Get-AzsSlbMuxInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="2274e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2274e-107">GetViaIdentity</span></span>
```
Get-AzsSlbMuxInstance -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="2274e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2274e-108">DESCRIPTION</span></span>
<span data-ttu-id="2274e-109">Restituisce l'istanza del multiplexer di bilanciamento del carico software richiesto.</span><span class="sxs-lookup"><span data-stu-id="2274e-109">Returns the requested software load balancer multiplexer instance.</span></span>

## <span data-ttu-id="2274e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2274e-110">EXAMPLES</span></span>

### <span data-ttu-id="2274e-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="2274e-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsSlbMuxInstance

A list of all software load balancer multiplexer instance at a location.
```

<span data-ttu-id="2274e-112">Ottenere tutte le istanze del multiplatore del bilanciamento del carico software in una posizione.</span><span class="sxs-lookup"><span data-stu-id="2274e-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="2274e-113">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="2274e-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsSlbMuxInstance -Name "AzS-SLB01"

A specific software load balancer multiplexer instance at a location given a name.
```

<span data-ttu-id="2274e-114">Ottenere una specifica istanza del programma di bilanciamento del carico del software in una posizione assegnata un nome.</span><span class="sxs-lookup"><span data-stu-id="2274e-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="2274e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2274e-115">PARAMETERS</span></span>

### <span data-ttu-id="2274e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2274e-116">-DefaultProfile</span></span>
<span data-ttu-id="2274e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2274e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2274e-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="2274e-118">-Filter</span></span>
<span data-ttu-id="2274e-119">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="2274e-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="2274e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2274e-120">-InputObject</span></span>
<span data-ttu-id="2274e-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2274e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2274e-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2274e-122">-Location</span></span>
<span data-ttu-id="2274e-123">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2274e-123">Location of the resource.</span></span>

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

### <span data-ttu-id="2274e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="2274e-124">-Name</span></span>
<span data-ttu-id="2274e-125">Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="2274e-125">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="2274e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2274e-126">-PassThru</span></span>
<span data-ttu-id="2274e-127">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="2274e-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2274e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2274e-128">-ResourceGroupName</span></span>
<span data-ttu-id="2274e-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2274e-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="2274e-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2274e-130">-SubscriptionId</span></span>
<span data-ttu-id="2274e-131">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2274e-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2274e-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2274e-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2274e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2274e-133">CommonParameters</span></span>
<span data-ttu-id="2274e-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2274e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2274e-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2274e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2274e-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2274e-136">INPUTS</span></span>

### <span data-ttu-id="2274e-137">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2274e-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="2274e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2274e-138">OUTPUTS</span></span>

### <span data-ttu-id="2274e-139">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. ISlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="2274e-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.ISlbMuxInstance</span></span>



## <span data-ttu-id="2274e-140">Note</span><span class="sxs-lookup"><span data-stu-id="2274e-140">NOTES</span></span>

<span data-ttu-id="2274e-141">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2274e-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2274e-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2274e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2274e-143">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="2274e-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2274e-144">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2274e-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="2274e-145">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="2274e-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="2274e-146">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="2274e-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="2274e-147">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="2274e-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="2274e-148">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="2274e-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="2274e-149">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="2274e-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="2274e-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="2274e-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2274e-151">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="2274e-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="2274e-152">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="2274e-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="2274e-153">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2274e-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="2274e-154">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="2274e-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="2274e-155">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="2274e-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="2274e-156">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="2274e-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="2274e-157">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="2274e-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="2274e-158">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2274e-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="2274e-159">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="2274e-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="2274e-160">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="2274e-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="2274e-161">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="2274e-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="2274e-162">`[StoragePool <String>]`: Nome del pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2274e-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="2274e-163">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2274e-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="2274e-164">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2274e-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2274e-165">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2274e-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2274e-166">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2274e-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="2274e-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2274e-167">RELATED LINKS</span></span>

