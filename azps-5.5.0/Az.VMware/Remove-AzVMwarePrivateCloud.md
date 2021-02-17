---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
ms.openlocfilehash: 76ad6df6dbbd9b019e4c89fdbca55107264f0406
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207507"
---
# <span data-ttu-id="132cf-101">Remove-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="132cf-101">Remove-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="132cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="132cf-102">SYNOPSIS</span></span>
<span data-ttu-id="132cf-103">Eliminare un cloud privato</span><span class="sxs-lookup"><span data-stu-id="132cf-103">Delete a private cloud</span></span>

## <span data-ttu-id="132cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="132cf-104">SYNTAX</span></span>

### <span data-ttu-id="132cf-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="132cf-105">Delete (Default)</span></span>
```
Remove-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="132cf-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="132cf-106">DeleteViaIdentity</span></span>
```
Remove-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="132cf-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="132cf-107">DESCRIPTION</span></span>
<span data-ttu-id="132cf-108">Eliminare un cloud privato</span><span class="sxs-lookup"><span data-stu-id="132cf-108">Delete a private cloud</span></span>

## <span data-ttu-id="132cf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="132cf-109">EXAMPLES</span></span>

### <span data-ttu-id="132cf-110">Esempio 1: Eliminare il cloud privato</span><span class="sxs-lookup"><span data-stu-id="132cf-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="132cf-111">Eliminare il cloud privato</span><span class="sxs-lookup"><span data-stu-id="132cf-111">Delete private cloud</span></span>

## <span data-ttu-id="132cf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="132cf-112">PARAMETERS</span></span>

### <span data-ttu-id="132cf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="132cf-113">-AsJob</span></span>
<span data-ttu-id="132cf-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="132cf-114">Run the command as a job</span></span>

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

### <span data-ttu-id="132cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="132cf-115">-DefaultProfile</span></span>
<span data-ttu-id="132cf-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="132cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="132cf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="132cf-117">-InputObject</span></span>
<span data-ttu-id="132cf-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="132cf-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="132cf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="132cf-119">-Name</span></span>
<span data-ttu-id="132cf-120">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="132cf-120">Name of the private cloud</span></span>

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

### <span data-ttu-id="132cf-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="132cf-121">-NoWait</span></span>
<span data-ttu-id="132cf-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="132cf-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="132cf-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="132cf-123">-PassThru</span></span>
<span data-ttu-id="132cf-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="132cf-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="132cf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="132cf-125">-ResourceGroupName</span></span>
<span data-ttu-id="132cf-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="132cf-126">The name of the resource group.</span></span>
<span data-ttu-id="132cf-127">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="132cf-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="132cf-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="132cf-128">-SubscriptionId</span></span>
<span data-ttu-id="132cf-129">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="132cf-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="132cf-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="132cf-130">-Confirm</span></span>
<span data-ttu-id="132cf-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="132cf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="132cf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="132cf-132">-WhatIf</span></span>
<span data-ttu-id="132cf-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="132cf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="132cf-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="132cf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="132cf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="132cf-135">CommonParameters</span></span>
<span data-ttu-id="132cf-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="132cf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="132cf-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="132cf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="132cf-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="132cf-138">INPUTS</span></span>

### <span data-ttu-id="132cf-139">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="132cf-139">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="132cf-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="132cf-140">OUTPUTS</span></span>

### <span data-ttu-id="132cf-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="132cf-141">System.Boolean</span></span>

## <span data-ttu-id="132cf-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="132cf-142">NOTES</span></span>

<span data-ttu-id="132cf-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="132cf-143">ALIASES</span></span>

<span data-ttu-id="132cf-144">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="132cf-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="132cf-145">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="132cf-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="132cf-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="132cf-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="132cf-147">INPUTOBJECT <IVMwareIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="132cf-147">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="132cf-148">`[AuthorizationName <String>]`: nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="132cf-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="132cf-149">`[ClusterName <String>]`: nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="132cf-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="132cf-150">`[HcxEnterpriseSiteName <String>]`: nome del sito HCX Enterprise nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="132cf-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="132cf-151">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="132cf-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="132cf-152">`[Location <String>]`: Area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="132cf-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="132cf-153">`[PrivateCloudName <String>]`: nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="132cf-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="132cf-154">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="132cf-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="132cf-155">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="132cf-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="132cf-156">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="132cf-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="132cf-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="132cf-157">RELATED LINKS</span></span>

