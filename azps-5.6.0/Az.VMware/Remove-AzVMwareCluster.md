---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/remove-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareCluster.md
ms.openlocfilehash: 878691dcc0cdc2a94dd5cc8509d9d74231aaee35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987137"
---
# <span data-ttu-id="5fcf9-101">Remove-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="5fcf9-101">Remove-AzVMWareCluster</span></span>

## <span data-ttu-id="5fcf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fcf9-102">SYNOPSIS</span></span>
<span data-ttu-id="5fcf9-103">Eliminare un cluster in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="5fcf9-103">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="5fcf9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5fcf9-104">SYNTAX</span></span>

### <span data-ttu-id="5fcf9-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5fcf9-105">Delete (Default)</span></span>
```
Remove-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5fcf9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5fcf9-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5fcf9-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5fcf9-107">DESCRIPTION</span></span>
<span data-ttu-id="5fcf9-108">Eliminare un cluster in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="5fcf9-108">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="5fcf9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5fcf9-109">EXAMPLES</span></span>

### <span data-ttu-id="5fcf9-110">Esempio 1: Eliminare un cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="5fcf9-110">Example 1: Delete cluster in private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="5fcf9-111">Eliminare un cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="5fcf9-111">Delete cluster in private cloud</span></span>

## <span data-ttu-id="5fcf9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fcf9-112">PARAMETERS</span></span>

### <span data-ttu-id="5fcf9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fcf9-113">-AsJob</span></span>
<span data-ttu-id="5fcf9-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="5fcf9-114">Run the command as a job</span></span>

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

### <span data-ttu-id="5fcf9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fcf9-115">-DefaultProfile</span></span>
<span data-ttu-id="5fcf9-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5fcf9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fcf9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fcf9-117">-InputObject</span></span>
<span data-ttu-id="5fcf9-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5fcf9-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcf9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5fcf9-119">-Name</span></span>
<span data-ttu-id="5fcf9-120">Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="5fcf9-120">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fcf9-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5fcf9-121">-NoWait</span></span>
<span data-ttu-id="5fcf9-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="5fcf9-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5fcf9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5fcf9-123">-PassThru</span></span>
<span data-ttu-id="5fcf9-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="5fcf9-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5fcf9-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="5fcf9-125">-PrivateCloudName</span></span>
<span data-ttu-id="5fcf9-126">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="5fcf9-126">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fcf9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fcf9-127">-ResourceGroupName</span></span>
<span data-ttu-id="5fcf9-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5fcf9-128">The name of the resource group.</span></span>
<span data-ttu-id="5fcf9-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="5fcf9-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fcf9-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5fcf9-130">-SubscriptionId</span></span>
<span data-ttu-id="5fcf9-131">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5fcf9-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fcf9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fcf9-132">-Confirm</span></span>
<span data-ttu-id="5fcf9-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fcf9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fcf9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fcf9-134">-WhatIf</span></span>
<span data-ttu-id="5fcf9-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5fcf9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fcf9-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5fcf9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fcf9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fcf9-137">CommonParameters</span></span>
<span data-ttu-id="5fcf9-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fcf9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fcf9-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5fcf9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fcf9-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="5fcf9-140">INPUTS</span></span>

### <span data-ttu-id="5fcf9-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="5fcf9-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="5fcf9-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5fcf9-142">OUTPUTS</span></span>

### <span data-ttu-id="5fcf9-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5fcf9-143">System.Boolean</span></span>

## <span data-ttu-id="5fcf9-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="5fcf9-144">NOTES</span></span>

<span data-ttu-id="5fcf9-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5fcf9-145">ALIASES</span></span>

<span data-ttu-id="5fcf9-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="5fcf9-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5fcf9-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="5fcf9-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5fcf9-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5fcf9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5fcf9-149">INPUTOBJECT <IVMWareIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="5fcf9-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5fcf9-150">`[AuthorizationName <String>]`: nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="5fcf9-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="5fcf9-151">`[ClusterName <String>]`: nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="5fcf9-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="5fcf9-152">`[HcxEnterpriseSiteName <String>]`: nome del sito HCX Enterprise nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="5fcf9-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="5fcf9-153">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="5fcf9-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5fcf9-154">`[Location <String>]`: Area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="5fcf9-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="5fcf9-155">`[PrivateCloudName <String>]`: nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="5fcf9-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="5fcf9-156">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5fcf9-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5fcf9-157">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="5fcf9-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="5fcf9-158">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5fcf9-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="5fcf9-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5fcf9-159">RELATED LINKS</span></span>

