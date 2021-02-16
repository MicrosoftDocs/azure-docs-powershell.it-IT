---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareCluster.md
ms.openlocfilehash: 3b47213cab20abdee5d87e721f3c9a19a10f042c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195503"
---
# <span data-ttu-id="b392b-101">Remove-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="b392b-101">Remove-AzVMwareCluster</span></span>

## <span data-ttu-id="b392b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b392b-102">SYNOPSIS</span></span>
<span data-ttu-id="b392b-103">Eliminare un cluster in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="b392b-103">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="b392b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b392b-104">SYNTAX</span></span>

### <span data-ttu-id="b392b-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b392b-105">Delete (Default)</span></span>
```
Remove-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b392b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b392b-106">DeleteViaIdentity</span></span>
```
Remove-AzVMwareCluster -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b392b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b392b-107">DESCRIPTION</span></span>
<span data-ttu-id="b392b-108">Eliminare un cluster in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="b392b-108">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="b392b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b392b-109">EXAMPLES</span></span>

### <span data-ttu-id="b392b-110">Esempio 1: Eliminare un cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="b392b-110">Example 1: Delete cluster in private cloud</span></span>
```powershell
PS C:\> Remove-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="b392b-111">Eliminare un cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="b392b-111">Delete cluster in private cloud</span></span>

## <span data-ttu-id="b392b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b392b-112">PARAMETERS</span></span>

### <span data-ttu-id="b392b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b392b-113">-AsJob</span></span>
<span data-ttu-id="b392b-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="b392b-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b392b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b392b-115">-DefaultProfile</span></span>
<span data-ttu-id="b392b-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b392b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b392b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b392b-117">-InputObject</span></span>
<span data-ttu-id="b392b-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b392b-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b392b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b392b-119">-Name</span></span>
<span data-ttu-id="b392b-120">Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="b392b-120">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="b392b-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b392b-121">-NoWait</span></span>
<span data-ttu-id="b392b-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="b392b-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b392b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b392b-123">-PassThru</span></span>
<span data-ttu-id="b392b-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="b392b-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b392b-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="b392b-125">-PrivateCloudName</span></span>
<span data-ttu-id="b392b-126">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="b392b-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="b392b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b392b-127">-ResourceGroupName</span></span>
<span data-ttu-id="b392b-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b392b-128">The name of the resource group.</span></span>
<span data-ttu-id="b392b-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b392b-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b392b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b392b-130">-SubscriptionId</span></span>
<span data-ttu-id="b392b-131">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b392b-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b392b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b392b-132">-Confirm</span></span>
<span data-ttu-id="b392b-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b392b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b392b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b392b-134">-WhatIf</span></span>
<span data-ttu-id="b392b-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b392b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b392b-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b392b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b392b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b392b-137">CommonParameters</span></span>
<span data-ttu-id="b392b-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b392b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b392b-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b392b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b392b-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="b392b-140">INPUTS</span></span>

### <span data-ttu-id="b392b-141">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="b392b-141">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="b392b-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b392b-142">OUTPUTS</span></span>

### <span data-ttu-id="b392b-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b392b-143">System.Boolean</span></span>

## <span data-ttu-id="b392b-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="b392b-144">NOTES</span></span>

<span data-ttu-id="b392b-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b392b-145">ALIASES</span></span>

<span data-ttu-id="b392b-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b392b-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b392b-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b392b-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b392b-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b392b-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b392b-149">INPUTOBJECT <IVMwareIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="b392b-149">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b392b-150">`[AuthorizationName <String>]`: nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="b392b-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="b392b-151">`[ClusterName <String>]`: nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="b392b-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="b392b-152">`[HcxEnterpriseSiteName <String>]`: nome del sito HCX Enterprise nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="b392b-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="b392b-153">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b392b-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b392b-154">`[Location <String>]`: Area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="b392b-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="b392b-155">`[PrivateCloudName <String>]`: nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="b392b-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="b392b-156">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b392b-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b392b-157">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b392b-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="b392b-158">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b392b-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="b392b-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b392b-159">RELATED LINKS</span></span>

