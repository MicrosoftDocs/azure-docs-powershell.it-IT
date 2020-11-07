---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsdrive
schema: 2.0.0
ms.openlocfilehash: ec2216a9234086702e8a9331888c04034d13a99f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863954"
---
# <span data-ttu-id="03834-101">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="03834-101">Get-AzsDrive</span></span>

## <span data-ttu-id="03834-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03834-102">SYNOPSIS</span></span>
<span data-ttu-id="03834-103">Restituire l'unità di archiviazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="03834-103">Return the requested a storage drive.</span></span>

## <span data-ttu-id="03834-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03834-104">SYNTAX</span></span>

### <span data-ttu-id="03834-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="03834-105">List (Default)</span></span>
```
Get-AzsDrive -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="03834-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="03834-106">Get</span></span>
```
Get-AzsDrive -Name <String> -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="03834-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="03834-107">GetViaIdentity</span></span>
```
Get-AzsDrive -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="03834-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03834-108">DESCRIPTION</span></span>
<span data-ttu-id="03834-109">Restituire l'unità di archiviazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="03834-109">Return the requested a storage drive.</span></span>

## <span data-ttu-id="03834-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03834-110">EXAMPLES</span></span>

### <span data-ttu-id="03834-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="03834-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name
```

<span data-ttu-id="03834-112">Ottenere un elenco di tutte le unità di archiviazione per un cluster specifico.</span><span class="sxs-lookup"><span data-stu-id="03834-112">Get a list of all storage drives for a given cluster.</span></span>

### <span data-ttu-id="03834-113">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="03834-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name -Name '{a185d466-4d21-4c1f-9489-7c9c66b6b172}:PD:{fd389cf7-2115-2144-5afe-27910562d6b3}'
```

<span data-ttu-id="03834-114">Ottenere un'unità di archiviazione per nome per un cluster specifico.</span><span class="sxs-lookup"><span data-stu-id="03834-114">Get a storage drive by name for a given cluster.</span></span>

## <span data-ttu-id="03834-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03834-115">PARAMETERS</span></span>

### <span data-ttu-id="03834-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03834-116">-DefaultProfile</span></span>
<span data-ttu-id="03834-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03834-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03834-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="03834-118">-Filter</span></span>
<span data-ttu-id="03834-119">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="03834-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="03834-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03834-120">-InputObject</span></span>
<span data-ttu-id="03834-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="03834-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="03834-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="03834-122">-Location</span></span>
<span data-ttu-id="03834-123">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="03834-123">Location of the resource.</span></span>

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

### <span data-ttu-id="03834-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="03834-124">-Name</span></span>
<span data-ttu-id="03834-125">Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="03834-125">Name of the storage drive.</span></span>

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

### <span data-ttu-id="03834-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03834-126">-PassThru</span></span>
<span data-ttu-id="03834-127">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="03834-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="03834-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03834-128">-ResourceGroupName</span></span>
<span data-ttu-id="03834-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="03834-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="03834-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="03834-130">-ScaleUnit</span></span>
<span data-ttu-id="03834-131">Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="03834-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="03834-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="03834-132">-Skip</span></span>
<span data-ttu-id="03834-133">Parametro OData skip.</span><span class="sxs-lookup"><span data-stu-id="03834-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="03834-134">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="03834-134">-StorageSubSystem</span></span>
<span data-ttu-id="03834-135">Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="03834-135">Name of the storage system.</span></span>

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

### <span data-ttu-id="03834-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03834-136">-SubscriptionId</span></span>
<span data-ttu-id="03834-137">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="03834-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="03834-138">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="03834-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="03834-139">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="03834-139">-Top</span></span>
<span data-ttu-id="03834-140">Parametro OData superiore.</span><span class="sxs-lookup"><span data-stu-id="03834-140">OData top parameter.</span></span>

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

### <span data-ttu-id="03834-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03834-141">CommonParameters</span></span>
<span data-ttu-id="03834-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03834-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03834-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03834-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03834-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03834-144">INPUTS</span></span>

### <span data-ttu-id="03834-145">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="03834-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="03834-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03834-146">OUTPUTS</span></span>

### <span data-ttu-id="03834-147">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20190501. IDrive</span><span class="sxs-lookup"><span data-stu-id="03834-147">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20190501.IDrive</span></span>



## <span data-ttu-id="03834-148">Note</span><span class="sxs-lookup"><span data-stu-id="03834-148">NOTES</span></span>

<span data-ttu-id="03834-149">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="03834-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="03834-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="03834-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="03834-151">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="03834-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="03834-152">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="03834-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="03834-153">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="03834-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="03834-154">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="03834-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="03834-155">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="03834-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="03834-156">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="03834-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="03834-157">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="03834-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="03834-158">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="03834-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="03834-159">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="03834-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="03834-160">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="03834-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="03834-161">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="03834-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="03834-162">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="03834-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="03834-163">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="03834-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="03834-164">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="03834-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="03834-165">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="03834-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="03834-166">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="03834-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="03834-167">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="03834-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="03834-168">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="03834-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="03834-169">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="03834-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="03834-170">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="03834-170">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="03834-171">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="03834-171">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="03834-172">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="03834-172">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="03834-173">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="03834-173">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="03834-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03834-174">RELATED LINKS</span></span>

