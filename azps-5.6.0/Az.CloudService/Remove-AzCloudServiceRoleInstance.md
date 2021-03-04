---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/remove-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 5a29444c5f6d05ddbf614e86cd13af6818d24d79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956461"
---
# <span data-ttu-id="b08fb-101">Remove-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="b08fb-101">Remove-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="b08fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b08fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b08fb-103">Elimina le istanze di ruoli in un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b08fb-103">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="b08fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b08fb-104">SYNTAX</span></span>

### <span data-ttu-id="b08fb-105">DeleteExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b08fb-105">DeleteExpanded (Default)</span></span>
```
Remove-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstance <String[]> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b08fb-106">DeleteViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b08fb-106">DeleteViaIdentityExpanded</span></span>
```
Remove-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b08fb-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b08fb-107">DESCRIPTION</span></span>
<span data-ttu-id="b08fb-108">Elimina le istanze di ruoli in un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b08fb-108">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="b08fb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b08fb-109">EXAMPLES</span></span>

### <span data-ttu-id="b08fb-110">Esempio 1: Rimuovere un'istanza del ruolo del servizio cloud</span><span class="sxs-lookup"><span data-stu-id="b08fb-110">Example 1: Remove a cloud service role instance</span></span>
```powershell
PS C:\> Remove-AzCloudServiceInstance -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="b08fb-111">Questo comando rimuove l'istanza di ruolo ContosoFrontEnd_IN_0 del servizio cloud denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="b08fb-111">This command removes the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="b08fb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b08fb-112">PARAMETERS</span></span>

### <span data-ttu-id="b08fb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b08fb-113">-AsJob</span></span>
<span data-ttu-id="b08fb-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="b08fb-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b08fb-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="b08fb-115">-CloudServiceName</span></span>
<span data-ttu-id="b08fb-116">Nome del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b08fb-116">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b08fb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b08fb-117">-DefaultProfile</span></span>
<span data-ttu-id="b08fb-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b08fb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b08fb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b08fb-119">-InputObject</span></span>
<span data-ttu-id="b08fb-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b08fb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: DeleteViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b08fb-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b08fb-121">-NoWait</span></span>
<span data-ttu-id="b08fb-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="b08fb-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b08fb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b08fb-123">-PassThru</span></span>
<span data-ttu-id="b08fb-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="b08fb-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b08fb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b08fb-125">-ResourceGroupName</span></span>
<span data-ttu-id="b08fb-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b08fb-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b08fb-127">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="b08fb-127">-RoleInstance</span></span>
<span data-ttu-id="b08fb-128">Elenco dei nomi di istanza dei ruoli del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b08fb-128">List of cloud service role instance names.</span></span>
<span data-ttu-id="b08fb-129">Il valore "\*" indica tutte le istanze del ruolo del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b08fb-129">Value of '\*' will signify all role instances of the cloud service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b08fb-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b08fb-130">-SubscriptionId</span></span>
<span data-ttu-id="b08fb-131">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b08fb-131">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b08fb-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b08fb-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b08fb-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b08fb-133">-Confirm</span></span>
<span data-ttu-id="b08fb-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b08fb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b08fb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b08fb-135">-WhatIf</span></span>
<span data-ttu-id="b08fb-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b08fb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b08fb-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b08fb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b08fb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b08fb-138">CommonParameters</span></span>
<span data-ttu-id="b08fb-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b08fb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b08fb-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b08fb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b08fb-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="b08fb-141">INPUTS</span></span>

### <span data-ttu-id="b08fb-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="b08fb-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="b08fb-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b08fb-143">OUTPUTS</span></span>

### <span data-ttu-id="b08fb-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b08fb-144">System.Boolean</span></span>

## <span data-ttu-id="b08fb-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="b08fb-145">NOTES</span></span>

<span data-ttu-id="b08fb-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b08fb-146">ALIASES</span></span>

<span data-ttu-id="b08fb-147">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b08fb-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b08fb-148">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b08fb-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b08fb-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b08fb-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b08fb-150">INPUTOBJECT <ICloudServiceIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b08fb-150">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b08fb-151">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b08fb-151">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="b08fb-152">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b08fb-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b08fb-153">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b08fb-153">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="b08fb-154">`[RoleInstanceName <String>]`: nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="b08fb-154">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="b08fb-155">`[RoleName <String>]`: nome del ruolo.</span><span class="sxs-lookup"><span data-stu-id="b08fb-155">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="b08fb-156">`[SubscriptionId <String>]`: le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b08fb-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b08fb-157">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b08fb-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b08fb-158">`[UpdateDomain <Int32?>]`: specifica un valore intero che identifica il dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b08fb-158">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="b08fb-159">I domini di aggiornamento sono identificati con un indice in base zero: il primo dominio di aggiornamento ha un ID pari a 0, il secondo con id 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="b08fb-159">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="b08fb-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b08fb-160">RELATED LINKS</span></span>

