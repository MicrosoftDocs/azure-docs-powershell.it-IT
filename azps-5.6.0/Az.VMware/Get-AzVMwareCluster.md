---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
ms.openlocfilehash: 842d0c26d4034a8c07415dfe8524b32623c07e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987194"
---
# <span data-ttu-id="d4057-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="d4057-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="d4057-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4057-102">SYNOPSIS</span></span>
<span data-ttu-id="d4057-103">Ottenere un cluster in base al nome in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="d4057-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="d4057-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4057-104">SYNTAX</span></span>

### <span data-ttu-id="d4057-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d4057-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d4057-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d4057-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d4057-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d4057-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d4057-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d4057-108">DESCRIPTION</span></span>
<span data-ttu-id="d4057-109">Ottenere un cluster in base al nome in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="d4057-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="d4057-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4057-110">EXAMPLES</span></span>

### <span data-ttu-id="d4057-111">Esempio 1: Ottenere il cluster</span><span class="sxs-lookup"><span data-stu-id="d4057-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="d4057-112">Ottieni cluster</span><span class="sxs-lookup"><span data-stu-id="d4057-112">Get cluster</span></span>

### <span data-ttu-id="d4057-113">Esempio 2: Gruppi di elenchi</span><span class="sxs-lookup"><span data-stu-id="d4057-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="d4057-114">Cluster di elenchi</span><span class="sxs-lookup"><span data-stu-id="d4057-114">List clusters</span></span>

## <span data-ttu-id="d4057-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4057-115">PARAMETERS</span></span>

### <span data-ttu-id="d4057-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4057-116">-DefaultProfile</span></span>
<span data-ttu-id="d4057-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4057-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4057-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4057-118">-InputObject</span></span>
<span data-ttu-id="d4057-119">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d4057-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4057-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d4057-120">-Name</span></span>
<span data-ttu-id="d4057-121">Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="d4057-121">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4057-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="d4057-122">-PrivateCloudName</span></span>
<span data-ttu-id="d4057-123">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="d4057-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="d4057-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4057-124">-ResourceGroupName</span></span>
<span data-ttu-id="d4057-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d4057-125">The name of the resource group.</span></span>
<span data-ttu-id="d4057-126">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d4057-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d4057-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4057-127">-SubscriptionId</span></span>
<span data-ttu-id="d4057-128">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d4057-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d4057-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4057-129">CommonParameters</span></span>
<span data-ttu-id="d4057-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4057-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4057-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d4057-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4057-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="d4057-132">INPUTS</span></span>

### <span data-ttu-id="d4057-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="d4057-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="d4057-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4057-134">OUTPUTS</span></span>

### <span data-ttu-id="d4057-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="d4057-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="d4057-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="d4057-136">NOTES</span></span>

<span data-ttu-id="d4057-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d4057-137">ALIASES</span></span>

<span data-ttu-id="d4057-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="d4057-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d4057-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d4057-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4057-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d4057-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d4057-141">INPUTOBJECT <IVMWareIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="d4057-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d4057-142">`[AuthorizationName <String>]`: nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="d4057-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="d4057-143">`[ClusterName <String>]`: nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="d4057-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="d4057-144">`[HcxEnterpriseSiteName <String>]`: nome del sito HCX Enterprise nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="d4057-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="d4057-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="d4057-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d4057-146">`[Location <String>]`: Area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="d4057-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="d4057-147">`[PrivateCloudName <String>]`: nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="d4057-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="d4057-148">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d4057-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d4057-149">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d4057-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="d4057-150">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d4057-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="d4057-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4057-151">RELATED LINKS</span></span>

