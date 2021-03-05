---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
ms.openlocfilehash: 8d1918599832f5740515dc6334192bf9b4cc54ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967133"
---
# <span data-ttu-id="6f565-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="6f565-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="6f565-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f565-102">SYNOPSIS</span></span>
<span data-ttu-id="6f565-103">Eliminare un cloud privato</span><span class="sxs-lookup"><span data-stu-id="6f565-103">Delete a private cloud</span></span>

## <span data-ttu-id="6f565-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f565-104">SYNTAX</span></span>

### <span data-ttu-id="6f565-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6f565-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6f565-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6f565-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6f565-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6f565-107">DESCRIPTION</span></span>
<span data-ttu-id="6f565-108">Eliminare un cloud privato</span><span class="sxs-lookup"><span data-stu-id="6f565-108">Delete a private cloud</span></span>

## <span data-ttu-id="6f565-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f565-109">EXAMPLES</span></span>

### <span data-ttu-id="6f565-110">Esempio 1: Eliminare il cloud privato</span><span class="sxs-lookup"><span data-stu-id="6f565-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="6f565-111">Eliminare il cloud privato</span><span class="sxs-lookup"><span data-stu-id="6f565-111">Delete private cloud</span></span>

## <span data-ttu-id="6f565-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f565-112">PARAMETERS</span></span>

### <span data-ttu-id="6f565-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f565-113">-AsJob</span></span>
<span data-ttu-id="6f565-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="6f565-114">Run the command as a job</span></span>

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

### <span data-ttu-id="6f565-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f565-115">-DefaultProfile</span></span>
<span data-ttu-id="6f565-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6f565-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f565-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f565-117">-InputObject</span></span>
<span data-ttu-id="6f565-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6f565-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6f565-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6f565-119">-Name</span></span>
<span data-ttu-id="6f565-120">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="6f565-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f565-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6f565-121">-NoWait</span></span>
<span data-ttu-id="6f565-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="6f565-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6f565-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f565-123">-PassThru</span></span>
<span data-ttu-id="6f565-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="6f565-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6f565-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f565-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f565-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6f565-126">The name of the resource group.</span></span>
<span data-ttu-id="6f565-127">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="6f565-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6f565-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6f565-128">-SubscriptionId</span></span>
<span data-ttu-id="6f565-129">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6f565-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6f565-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f565-130">-Confirm</span></span>
<span data-ttu-id="6f565-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f565-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f565-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f565-132">-WhatIf</span></span>
<span data-ttu-id="6f565-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6f565-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f565-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6f565-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f565-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f565-135">CommonParameters</span></span>
<span data-ttu-id="6f565-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f565-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f565-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6f565-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f565-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="6f565-138">INPUTS</span></span>

### <span data-ttu-id="6f565-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="6f565-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="6f565-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f565-140">OUTPUTS</span></span>

### <span data-ttu-id="6f565-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6f565-141">System.Boolean</span></span>

## <span data-ttu-id="6f565-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="6f565-142">NOTES</span></span>

<span data-ttu-id="6f565-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6f565-143">ALIASES</span></span>

<span data-ttu-id="6f565-144">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="6f565-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6f565-145">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="6f565-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6f565-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6f565-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6f565-147">INPUTOBJECT <IVMWareIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="6f565-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6f565-148">`[AuthorizationName <String>]`: nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="6f565-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="6f565-149">`[ClusterName <String>]`: nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="6f565-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="6f565-150">`[HcxEnterpriseSiteName <String>]`: nome del sito HCX Enterprise nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="6f565-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="6f565-151">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="6f565-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6f565-152">`[Location <String>]`: Area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="6f565-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="6f565-153">`[PrivateCloudName <String>]`: nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="6f565-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="6f565-154">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6f565-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6f565-155">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="6f565-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="6f565-156">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6f565-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="6f565-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f565-157">RELATED LINKS</span></span>

