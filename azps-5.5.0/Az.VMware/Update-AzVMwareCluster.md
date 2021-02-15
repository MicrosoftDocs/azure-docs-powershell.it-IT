---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
ms.openlocfilehash: cfe9a8aa16803433055eb0cec5993cedcbcb5874
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182527"
---
# <span data-ttu-id="0175d-101">Update-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="0175d-101">Update-AzVMwareCluster</span></span>

## <span data-ttu-id="0175d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0175d-102">SYNOPSIS</span></span>
<span data-ttu-id="0175d-103">Aggiornare un cluster in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="0175d-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="0175d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0175d-104">SYNTAX</span></span>

### <span data-ttu-id="0175d-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0175d-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0175d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0175d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMwareCluster -InputObject <IVMwareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0175d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0175d-107">DESCRIPTION</span></span>
<span data-ttu-id="0175d-108">Aggiornare un cluster in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="0175d-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="0175d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0175d-109">EXAMPLES</span></span>

### <span data-ttu-id="0175d-110">Esempio 1: Aggiornare le dimensioni del cluster in base al nome</span><span class="sxs-lookup"><span data-stu-id="0175d-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="0175d-111">Aggiornare le dimensioni del cluster in base al nome</span><span class="sxs-lookup"><span data-stu-id="0175d-111">Update cluster size by name</span></span>

### <span data-ttu-id="0175d-112">Esempio 2: Aggiornare le dimensioni del cluster in base all'oggetto di input</span><span class="sxs-lookup"><span data-stu-id="0175d-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMwareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="0175d-113">Aggiornare le dimensioni del cluster in base all'oggetto di input</span><span class="sxs-lookup"><span data-stu-id="0175d-113">Update cluster size by input object</span></span>

## <span data-ttu-id="0175d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0175d-114">PARAMETERS</span></span>

### <span data-ttu-id="0175d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0175d-115">-AsJob</span></span>
<span data-ttu-id="0175d-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="0175d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0175d-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="0175d-117">-ClusterSize</span></span>
<span data-ttu-id="0175d-118">Le dimensioni del cluster</span><span class="sxs-lookup"><span data-stu-id="0175d-118">The cluster size</span></span>

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

### <span data-ttu-id="0175d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0175d-119">-DefaultProfile</span></span>
<span data-ttu-id="0175d-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0175d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0175d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0175d-121">-InputObject</span></span>
<span data-ttu-id="0175d-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0175d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0175d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0175d-123">-Name</span></span>
<span data-ttu-id="0175d-124">Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="0175d-124">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="0175d-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0175d-125">-NoWait</span></span>
<span data-ttu-id="0175d-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="0175d-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0175d-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="0175d-127">-PrivateCloudName</span></span>
<span data-ttu-id="0175d-128">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="0175d-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="0175d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0175d-129">-ResourceGroupName</span></span>
<span data-ttu-id="0175d-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0175d-130">The name of the resource group.</span></span>
<span data-ttu-id="0175d-131">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0175d-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0175d-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0175d-132">-SubscriptionId</span></span>
<span data-ttu-id="0175d-133">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0175d-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0175d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0175d-134">-Confirm</span></span>
<span data-ttu-id="0175d-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0175d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0175d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0175d-136">-WhatIf</span></span>
<span data-ttu-id="0175d-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0175d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0175d-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0175d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0175d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0175d-139">CommonParameters</span></span>
<span data-ttu-id="0175d-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0175d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0175d-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0175d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0175d-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="0175d-142">INPUTS</span></span>

### <span data-ttu-id="0175d-143">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="0175d-143">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="0175d-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0175d-144">OUTPUTS</span></span>

### <span data-ttu-id="0175d-145">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="0175d-145">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="0175d-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="0175d-146">NOTES</span></span>

<span data-ttu-id="0175d-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0175d-147">ALIASES</span></span>

<span data-ttu-id="0175d-148">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="0175d-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0175d-149">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0175d-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0175d-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0175d-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0175d-151">INPUTOBJECT <IVMwareIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="0175d-151">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0175d-152">`[AuthorizationName <String>]`: nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="0175d-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="0175d-153">`[ClusterName <String>]`: nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="0175d-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="0175d-154">`[HcxEnterpriseSiteName <String>]`: nome del sito HCX Enterprise nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="0175d-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="0175d-155">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="0175d-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0175d-156">`[Location <String>]`: Area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="0175d-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="0175d-157">`[PrivateCloudName <String>]`: nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="0175d-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="0175d-158">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0175d-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0175d-159">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0175d-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="0175d-160">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0175d-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="0175d-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0175d-161">RELATED LINKS</span></span>

