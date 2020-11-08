---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsvolume
schema: 2.0.0
ms.openlocfilehash: a423470454e77c58a8b611a47c737e5d86bfd1cf
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023262"
---
# <span data-ttu-id="73182-101">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="73182-101">Get-AzsVolume</span></span>

## <span data-ttu-id="73182-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73182-102">SYNOPSIS</span></span>
<span data-ttu-id="73182-103">Restituire il volume di archiviazione richiesto.</span><span class="sxs-lookup"><span data-stu-id="73182-103">Return the requested a storage volume.</span></span>

## <span data-ttu-id="73182-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73182-104">SYNTAX</span></span>

### <span data-ttu-id="73182-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="73182-105">List (Default)</span></span>
```
Get-AzsVolume -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="73182-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="73182-106">Get</span></span>
```
Get-AzsVolume -Name <String> -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="73182-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="73182-107">GetViaIdentity</span></span>
```
Get-AzsVolume -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="73182-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73182-108">DESCRIPTION</span></span>
<span data-ttu-id="73182-109">Restituire il volume di archiviazione richiesto.</span><span class="sxs-lookup"><span data-stu-id="73182-109">Return the requested a storage volume.</span></span>

## <span data-ttu-id="73182-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73182-110">EXAMPLES</span></span>

### <span data-ttu-id="73182-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="73182-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsVolume -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name
```

<span data-ttu-id="73182-112">Ottenere un elenco di tutti i volumi di archiviazione in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="73182-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="73182-113">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="73182-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsVolume -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name -Name ee594cf5-cf54-46b4-a641-139553307195
```

<span data-ttu-id="73182-114">Ottenere un volume di archiviazione per nome in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="73182-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="73182-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73182-115">PARAMETERS</span></span>

### <span data-ttu-id="73182-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73182-116">-DefaultProfile</span></span>
<span data-ttu-id="73182-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73182-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73182-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="73182-118">-Filter</span></span>
<span data-ttu-id="73182-119">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="73182-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="73182-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73182-120">-InputObject</span></span>
<span data-ttu-id="73182-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="73182-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="73182-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="73182-122">-Location</span></span>
<span data-ttu-id="73182-123">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="73182-123">Location of the resource.</span></span>

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

### <span data-ttu-id="73182-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="73182-124">-Name</span></span>
<span data-ttu-id="73182-125">Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="73182-125">Name of the storage volume.</span></span>

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

### <span data-ttu-id="73182-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73182-126">-PassThru</span></span>
<span data-ttu-id="73182-127">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="73182-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="73182-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73182-128">-ResourceGroupName</span></span>
<span data-ttu-id="73182-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="73182-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="73182-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="73182-130">-ScaleUnit</span></span>
<span data-ttu-id="73182-131">Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="73182-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="73182-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="73182-132">-Skip</span></span>
<span data-ttu-id="73182-133">Parametro OData skip.</span><span class="sxs-lookup"><span data-stu-id="73182-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="73182-134">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="73182-134">-StorageSubSystem</span></span>
<span data-ttu-id="73182-135">Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="73182-135">Name of the storage system.</span></span>

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

### <span data-ttu-id="73182-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73182-136">-SubscriptionId</span></span>
<span data-ttu-id="73182-137">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="73182-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="73182-138">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="73182-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="73182-139">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="73182-139">-Top</span></span>
<span data-ttu-id="73182-140">Parametro OData superiore.</span><span class="sxs-lookup"><span data-stu-id="73182-140">OData top parameter.</span></span>

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

### <span data-ttu-id="73182-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73182-141">CommonParameters</span></span>
<span data-ttu-id="73182-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73182-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73182-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73182-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73182-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73182-144">INPUTS</span></span>

### <span data-ttu-id="73182-145">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="73182-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="73182-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73182-146">OUTPUTS</span></span>

### <span data-ttu-id="73182-147">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20190501. IVolume</span><span class="sxs-lookup"><span data-stu-id="73182-147">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20190501.IVolume</span></span>



## <span data-ttu-id="73182-148">Note</span><span class="sxs-lookup"><span data-stu-id="73182-148">NOTES</span></span>

<span data-ttu-id="73182-149">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="73182-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73182-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="73182-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="73182-151">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="73182-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="73182-152">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="73182-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="73182-153">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="73182-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="73182-154">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="73182-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="73182-155">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="73182-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="73182-156">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="73182-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="73182-157">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="73182-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="73182-158">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="73182-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="73182-159">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="73182-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="73182-160">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="73182-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="73182-161">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="73182-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="73182-162">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="73182-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="73182-163">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="73182-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="73182-164">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="73182-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="73182-165">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="73182-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="73182-166">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="73182-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="73182-167">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="73182-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="73182-168">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="73182-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="73182-169">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="73182-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="73182-170">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="73182-170">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="73182-171">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="73182-171">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="73182-172">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="73182-172">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="73182-173">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="73182-173">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="73182-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73182-174">RELATED LINKS</span></span>

