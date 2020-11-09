---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
ms.openlocfilehash: b8e1f819c01edac24ff23c629de130036442c9e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301663"
---
# <span data-ttu-id="6a10a-101">Update-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="6a10a-101">Update-AzVMWareCluster</span></span>

## <span data-ttu-id="6a10a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a10a-102">SYNOPSIS</span></span>
<span data-ttu-id="6a10a-103">Aggiornare un cluster in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="6a10a-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="6a10a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a10a-104">SYNTAX</span></span>

### <span data-ttu-id="6a10a-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6a10a-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6a10a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6a10a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWareCluster -InputObject <IVMWareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6a10a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a10a-107">DESCRIPTION</span></span>
<span data-ttu-id="6a10a-108">Aggiornare un cluster in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="6a10a-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="6a10a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a10a-109">EXAMPLES</span></span>

### <span data-ttu-id="6a10a-110">Esempio 1: aggiornare le dimensioni del cluster per nome</span><span class="sxs-lookup"><span data-stu-id="6a10a-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="6a10a-111">Aggiornare le dimensioni del cluster per nome</span><span class="sxs-lookup"><span data-stu-id="6a10a-111">Update cluster size by name</span></span>

### <span data-ttu-id="6a10a-112">Esempio 2: aggiornare le dimensioni del cluster per l'oggetto di input</span><span class="sxs-lookup"><span data-stu-id="6a10a-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMWareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="6a10a-113">Aggiornare la dimensione del cluster per oggetto di input</span><span class="sxs-lookup"><span data-stu-id="6a10a-113">Update cluster size by input object</span></span>

## <span data-ttu-id="6a10a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a10a-114">PARAMETERS</span></span>

### <span data-ttu-id="6a10a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a10a-115">-AsJob</span></span>
<span data-ttu-id="6a10a-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="6a10a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6a10a-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="6a10a-117">-ClusterSize</span></span>
<span data-ttu-id="6a10a-118">Dimensioni del cluster</span><span class="sxs-lookup"><span data-stu-id="6a10a-118">The cluster size</span></span>

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

### <span data-ttu-id="6a10a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a10a-119">-DefaultProfile</span></span>
<span data-ttu-id="6a10a-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a10a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a10a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a10a-121">-InputObject</span></span>
<span data-ttu-id="6a10a-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6a10a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a10a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a10a-123">-Name</span></span>
<span data-ttu-id="6a10a-124">Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="6a10a-124">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="6a10a-125">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="6a10a-125">-NoWait</span></span>
<span data-ttu-id="6a10a-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="6a10a-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6a10a-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="6a10a-127">-PrivateCloudName</span></span>
<span data-ttu-id="6a10a-128">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="6a10a-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="6a10a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a10a-129">-ResourceGroupName</span></span>
<span data-ttu-id="6a10a-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6a10a-130">The name of the resource group.</span></span>
<span data-ttu-id="6a10a-131">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="6a10a-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6a10a-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a10a-132">-SubscriptionId</span></span>
<span data-ttu-id="6a10a-133">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6a10a-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6a10a-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6a10a-134">-Confirm</span></span>
<span data-ttu-id="6a10a-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a10a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a10a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a10a-136">-WhatIf</span></span>
<span data-ttu-id="6a10a-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a10a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a10a-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a10a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a10a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a10a-139">CommonParameters</span></span>
<span data-ttu-id="6a10a-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a10a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a10a-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a10a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a10a-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a10a-142">INPUTS</span></span>

### <span data-ttu-id="6a10a-143">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="6a10a-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="6a10a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a10a-144">OUTPUTS</span></span>

### <span data-ttu-id="6a10a-145">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="6a10a-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="6a10a-146">Note</span><span class="sxs-lookup"><span data-stu-id="6a10a-146">NOTES</span></span>

<span data-ttu-id="6a10a-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6a10a-147">ALIASES</span></span>

<span data-ttu-id="6a10a-148">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a10a-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a10a-149">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="6a10a-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a10a-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6a10a-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a10a-151">INPUTOBJECT <IVMWareIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="6a10a-151">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6a10a-152">`[AuthorizationName <String>]`: Nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="6a10a-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="6a10a-153">`[ClusterName <String>]`: Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="6a10a-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="6a10a-154">`[HcxEnterpriseSiteName <String>]`: Nome del sito aziendale di HCX nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="6a10a-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="6a10a-155">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="6a10a-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6a10a-156">`[Location <String>]`: Area di Azure</span><span class="sxs-lookup"><span data-stu-id="6a10a-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="6a10a-157">`[PrivateCloudName <String>]`: Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="6a10a-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="6a10a-158">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6a10a-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6a10a-159">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="6a10a-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="6a10a-160">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6a10a-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="6a10a-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a10a-161">RELATED LINKS</span></span>

