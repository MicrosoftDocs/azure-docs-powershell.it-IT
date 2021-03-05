---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
ms.openlocfilehash: f708d1b752c0d8106d7a8f9f7613fa74b6b19937
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988593"
---
# <span data-ttu-id="38d30-101">Update-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="38d30-101">Update-AzVMWareCluster</span></span>

## <span data-ttu-id="38d30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38d30-102">SYNOPSIS</span></span>
<span data-ttu-id="38d30-103">Aggiornare un cluster in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="38d30-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="38d30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38d30-104">SYNTAX</span></span>

### <span data-ttu-id="38d30-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="38d30-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="38d30-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="38d30-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWareCluster -InputObject <IVMWareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="38d30-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="38d30-107">DESCRIPTION</span></span>
<span data-ttu-id="38d30-108">Aggiornare un cluster in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="38d30-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="38d30-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38d30-109">EXAMPLES</span></span>

### <span data-ttu-id="38d30-110">Esempio 1: Aggiornare le dimensioni del cluster in base al nome</span><span class="sxs-lookup"><span data-stu-id="38d30-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="38d30-111">Aggiornare le dimensioni del cluster in base al nome</span><span class="sxs-lookup"><span data-stu-id="38d30-111">Update cluster size by name</span></span>

### <span data-ttu-id="38d30-112">Esempio 2: Aggiornare le dimensioni del cluster in base all'oggetto di input</span><span class="sxs-lookup"><span data-stu-id="38d30-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMWareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="38d30-113">Aggiornare le dimensioni del cluster in base all'oggetto di input</span><span class="sxs-lookup"><span data-stu-id="38d30-113">Update cluster size by input object</span></span>

## <span data-ttu-id="38d30-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38d30-114">PARAMETERS</span></span>

### <span data-ttu-id="38d30-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38d30-115">-AsJob</span></span>
<span data-ttu-id="38d30-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="38d30-116">Run the command as a job</span></span>

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

### <span data-ttu-id="38d30-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="38d30-117">-ClusterSize</span></span>
<span data-ttu-id="38d30-118">Le dimensioni del cluster</span><span class="sxs-lookup"><span data-stu-id="38d30-118">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d30-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d30-119">-DefaultProfile</span></span>
<span data-ttu-id="38d30-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38d30-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38d30-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38d30-121">-InputObject</span></span>
<span data-ttu-id="38d30-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="38d30-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38d30-123">-Name</span><span class="sxs-lookup"><span data-stu-id="38d30-123">-Name</span></span>
<span data-ttu-id="38d30-124">Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="38d30-124">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d30-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="38d30-125">-NoWait</span></span>
<span data-ttu-id="38d30-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="38d30-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="38d30-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="38d30-127">-PrivateCloudName</span></span>
<span data-ttu-id="38d30-128">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="38d30-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d30-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38d30-129">-ResourceGroupName</span></span>
<span data-ttu-id="38d30-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="38d30-130">The name of the resource group.</span></span>
<span data-ttu-id="38d30-131">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="38d30-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d30-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38d30-132">-SubscriptionId</span></span>
<span data-ttu-id="38d30-133">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="38d30-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d30-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38d30-134">-Confirm</span></span>
<span data-ttu-id="38d30-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38d30-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d30-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38d30-136">-WhatIf</span></span>
<span data-ttu-id="38d30-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38d30-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38d30-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38d30-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d30-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d30-139">CommonParameters</span></span>
<span data-ttu-id="38d30-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d30-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d30-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38d30-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d30-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="38d30-142">INPUTS</span></span>

### <span data-ttu-id="38d30-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="38d30-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="38d30-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38d30-144">OUTPUTS</span></span>

### <span data-ttu-id="38d30-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="38d30-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="38d30-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="38d30-146">NOTES</span></span>

<span data-ttu-id="38d30-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="38d30-147">ALIASES</span></span>

<span data-ttu-id="38d30-148">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="38d30-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="38d30-149">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="38d30-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="38d30-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="38d30-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="38d30-151">INPUTOBJECT <IVMWareIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="38d30-151">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="38d30-152">`[AuthorizationName <String>]`: nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="38d30-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="38d30-153">`[ClusterName <String>]`: nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="38d30-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="38d30-154">`[HcxEnterpriseSiteName <String>]`: nome del sito HCX Enterprise nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="38d30-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="38d30-155">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="38d30-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="38d30-156">`[Location <String>]`: Area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="38d30-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="38d30-157">`[PrivateCloudName <String>]`: nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="38d30-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="38d30-158">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="38d30-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="38d30-159">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="38d30-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="38d30-160">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="38d30-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="38d30-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38d30-161">RELATED LINKS</span></span>

