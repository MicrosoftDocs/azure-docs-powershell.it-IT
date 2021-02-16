---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
ms.openlocfilehash: 51a889abe0d1842f66a0ed9b17f3b07acd85a54b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208899"
---
# <span data-ttu-id="b2a20-101">Get-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="b2a20-101">Get-AzVMwareCluster</span></span>

## <span data-ttu-id="b2a20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2a20-102">SYNOPSIS</span></span>
<span data-ttu-id="b2a20-103">Ottenere un cluster in base al nome in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="b2a20-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="b2a20-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2a20-104">SYNTAX</span></span>

### <span data-ttu-id="b2a20-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b2a20-105">List (Default)</span></span>
```
Get-AzVMwareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b2a20-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="b2a20-106">Get</span></span>
```
Get-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b2a20-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b2a20-107">GetViaIdentity</span></span>
```
Get-AzVMwareCluster -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b2a20-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b2a20-108">DESCRIPTION</span></span>
<span data-ttu-id="b2a20-109">Ottenere un cluster in base al nome in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="b2a20-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="b2a20-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2a20-110">EXAMPLES</span></span>

### <span data-ttu-id="b2a20-111">Esempio 1: Ottenere il cluster</span><span class="sxs-lookup"><span data-stu-id="b2a20-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="b2a20-112">Ottieni cluster</span><span class="sxs-lookup"><span data-stu-id="b2a20-112">Get cluster</span></span>

### <span data-ttu-id="b2a20-113">Esempio 2: Gruppi di elenchi</span><span class="sxs-lookup"><span data-stu-id="b2a20-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="b2a20-114">Cluster di elenchi</span><span class="sxs-lookup"><span data-stu-id="b2a20-114">List clusters</span></span>

## <span data-ttu-id="b2a20-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2a20-115">PARAMETERS</span></span>

### <span data-ttu-id="b2a20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2a20-116">-DefaultProfile</span></span>
<span data-ttu-id="b2a20-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2a20-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2a20-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2a20-118">-InputObject</span></span>
<span data-ttu-id="b2a20-119">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b2a20-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2a20-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b2a20-120">-Name</span></span>
<span data-ttu-id="b2a20-121">Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="b2a20-121">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="b2a20-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="b2a20-122">-PrivateCloudName</span></span>
<span data-ttu-id="b2a20-123">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="b2a20-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="b2a20-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2a20-124">-ResourceGroupName</span></span>
<span data-ttu-id="b2a20-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2a20-125">The name of the resource group.</span></span>
<span data-ttu-id="b2a20-126">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b2a20-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b2a20-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b2a20-127">-SubscriptionId</span></span>
<span data-ttu-id="b2a20-128">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b2a20-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b2a20-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2a20-129">CommonParameters</span></span>
<span data-ttu-id="b2a20-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2a20-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2a20-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b2a20-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2a20-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="b2a20-132">INPUTS</span></span>

### <span data-ttu-id="b2a20-133">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="b2a20-133">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="b2a20-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2a20-134">OUTPUTS</span></span>

### <span data-ttu-id="b2a20-135">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="b2a20-135">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="b2a20-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="b2a20-136">NOTES</span></span>

<span data-ttu-id="b2a20-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b2a20-137">ALIASES</span></span>

<span data-ttu-id="b2a20-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b2a20-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b2a20-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b2a20-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b2a20-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b2a20-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b2a20-141">INPUTOBJECT <IVMwareIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="b2a20-141">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b2a20-142">`[AuthorizationName <String>]`: nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="b2a20-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="b2a20-143">`[ClusterName <String>]`: nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="b2a20-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="b2a20-144">`[HcxEnterpriseSiteName <String>]`: nome del sito HCX Enterprise nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="b2a20-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="b2a20-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b2a20-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b2a20-146">`[Location <String>]`: Area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="b2a20-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="b2a20-147">`[PrivateCloudName <String>]`: nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="b2a20-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="b2a20-148">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2a20-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b2a20-149">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b2a20-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="b2a20-150">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b2a20-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="b2a20-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2a20-151">RELATED LINKS</span></span>

