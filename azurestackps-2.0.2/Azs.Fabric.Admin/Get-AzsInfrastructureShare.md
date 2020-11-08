---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureshare
schema: 2.0.0
ms.openlocfilehash: e5fce1490b27bb569ce493a66a1c2646b73466a4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030135"
---
# <span data-ttu-id="93da7-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="93da7-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="93da7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93da7-102">SYNOPSIS</span></span>
<span data-ttu-id="93da7-103">Restituisce la condivisione file in tessuto richiesto.</span><span class="sxs-lookup"><span data-stu-id="93da7-103">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="93da7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93da7-104">SYNTAX</span></span>

### <span data-ttu-id="93da7-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="93da7-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="93da7-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="93da7-106">Get</span></span>
```
Get-AzsInfrastructureShare -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="93da7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="93da7-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureShare -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="93da7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93da7-108">DESCRIPTION</span></span>
<span data-ttu-id="93da7-109">Restituisce la condivisione file in tessuto richiesto.</span><span class="sxs-lookup"><span data-stu-id="93da7-109">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="93da7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93da7-110">EXAMPLES</span></span>

### <span data-ttu-id="93da7-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="93da7-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare
```

<span data-ttu-id="93da7-112">Restituisce un elenco di tutte le condivisioni file.</span><span class="sxs-lookup"><span data-stu-id="93da7-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="93da7-113">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="93da7-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare -Name SU1_ObjStore_1
```

<span data-ttu-id="93da7-114">Restituisce una condivisione di file in base al nome.</span><span class="sxs-lookup"><span data-stu-id="93da7-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="93da7-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93da7-115">PARAMETERS</span></span>

### <span data-ttu-id="93da7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93da7-116">-DefaultProfile</span></span>
<span data-ttu-id="93da7-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93da7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93da7-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="93da7-118">-Filter</span></span>
<span data-ttu-id="93da7-119">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="93da7-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="93da7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93da7-120">-InputObject</span></span>
<span data-ttu-id="93da7-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="93da7-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="93da7-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="93da7-122">-Location</span></span>
<span data-ttu-id="93da7-123">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="93da7-123">Location of the resource.</span></span>

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

### <span data-ttu-id="93da7-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="93da7-124">-Name</span></span>
<span data-ttu-id="93da7-125">Nome condivisione file in tessuto.</span><span class="sxs-lookup"><span data-stu-id="93da7-125">Fabric file share name.</span></span>

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

### <span data-ttu-id="93da7-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93da7-126">-PassThru</span></span>
<span data-ttu-id="93da7-127">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="93da7-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="93da7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93da7-128">-ResourceGroupName</span></span>
<span data-ttu-id="93da7-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="93da7-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="93da7-130">-Skip</span><span class="sxs-lookup"><span data-stu-id="93da7-130">-Skip</span></span>
<span data-ttu-id="93da7-131">Parametro OData skip.</span><span class="sxs-lookup"><span data-stu-id="93da7-131">OData skip parameter.</span></span>

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

### <span data-ttu-id="93da7-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93da7-132">-SubscriptionId</span></span>
<span data-ttu-id="93da7-133">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="93da7-133">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="93da7-134">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="93da7-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="93da7-135">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="93da7-135">-Top</span></span>
<span data-ttu-id="93da7-136">Parametro OData superiore.</span><span class="sxs-lookup"><span data-stu-id="93da7-136">OData top parameter.</span></span>

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

### <span data-ttu-id="93da7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93da7-137">CommonParameters</span></span>
<span data-ttu-id="93da7-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93da7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93da7-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93da7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93da7-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93da7-140">INPUTS</span></span>

### <span data-ttu-id="93da7-141">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="93da7-141">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="93da7-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93da7-142">OUTPUTS</span></span>

### <span data-ttu-id="93da7-143">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IFileShare</span><span class="sxs-lookup"><span data-stu-id="93da7-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFileShare</span></span>



## <span data-ttu-id="93da7-144">Note</span><span class="sxs-lookup"><span data-stu-id="93da7-144">NOTES</span></span>

<span data-ttu-id="93da7-145">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="93da7-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="93da7-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="93da7-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="93da7-147">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="93da7-147">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="93da7-148">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="93da7-148">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="93da7-149">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="93da7-149">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="93da7-150">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="93da7-150">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="93da7-151">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="93da7-151">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="93da7-152">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="93da7-152">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="93da7-153">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="93da7-153">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="93da7-154">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="93da7-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="93da7-155">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="93da7-155">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="93da7-156">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="93da7-156">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="93da7-157">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="93da7-157">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="93da7-158">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="93da7-158">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="93da7-159">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="93da7-159">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="93da7-160">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="93da7-160">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="93da7-161">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="93da7-161">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="93da7-162">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="93da7-162">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="93da7-163">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="93da7-163">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="93da7-164">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="93da7-164">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="93da7-165">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="93da7-165">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="93da7-166">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="93da7-166">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="93da7-167">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="93da7-167">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="93da7-168">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="93da7-168">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="93da7-169">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="93da7-169">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="93da7-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93da7-170">RELATED LINKS</span></span>

