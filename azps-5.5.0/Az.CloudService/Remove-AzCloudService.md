---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/remove-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudService.md
ms.openlocfilehash: 07d7747a16af8d61b8ddbf05030445e599bb7e33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200702"
---
# <span data-ttu-id="b7fd0-101">Remove-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="b7fd0-101">Remove-AzCloudService</span></span>

## <span data-ttu-id="b7fd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="b7fd0-103">Elimina un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-103">Deletes a cloud service.</span></span>

## <span data-ttu-id="b7fd0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7fd0-104">SYNTAX</span></span>

### <span data-ttu-id="b7fd0-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b7fd0-105">Delete (Default)</span></span>
```
Remove-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b7fd0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b7fd0-106">DeleteViaIdentity</span></span>
```
Remove-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b7fd0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b7fd0-107">DESCRIPTION</span></span>
<span data-ttu-id="b7fd0-108">Elimina un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-108">Deletes a cloud service.</span></span>

## <span data-ttu-id="b7fd0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7fd0-109">EXAMPLES</span></span>

### <span data-ttu-id="b7fd0-110">Esempio 1: Rimuovere un servizio cloud</span><span class="sxs-lookup"><span data-stu-id="b7fd0-110">Example 1: Remove a cloud service</span></span>
```powershell
PS C:\> Remove-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="b7fd0-111">Questo comando rimuove il servizio cloud denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-111">This command removes the cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="b7fd0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7fd0-112">PARAMETERS</span></span>

### <span data-ttu-id="b7fd0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7fd0-113">-AsJob</span></span>
<span data-ttu-id="b7fd0-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="b7fd0-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b7fd0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7fd0-115">-DefaultProfile</span></span>
<span data-ttu-id="b7fd0-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7fd0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7fd0-117">-InputObject</span></span>
<span data-ttu-id="b7fd0-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7fd0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b7fd0-119">-Name</span></span>
<span data-ttu-id="b7fd0-120">Nome del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-120">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fd0-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b7fd0-121">-NoWait</span></span>
<span data-ttu-id="b7fd0-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="b7fd0-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b7fd0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7fd0-123">-PassThru</span></span>
<span data-ttu-id="b7fd0-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="b7fd0-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b7fd0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7fd0-125">-ResourceGroupName</span></span>
<span data-ttu-id="b7fd0-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-126">Name of the resource group.</span></span>

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

### <span data-ttu-id="b7fd0-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7fd0-127">-SubscriptionId</span></span>
<span data-ttu-id="b7fd0-128">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b7fd0-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b7fd0-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7fd0-130">-Confirm</span></span>
<span data-ttu-id="b7fd0-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7fd0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7fd0-132">-WhatIf</span></span>
<span data-ttu-id="b7fd0-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7fd0-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7fd0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7fd0-135">CommonParameters</span></span>
<span data-ttu-id="b7fd0-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7fd0-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7fd0-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="b7fd0-138">INPUTS</span></span>

### <span data-ttu-id="b7fd0-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="b7fd0-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="b7fd0-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7fd0-140">OUTPUTS</span></span>

### <span data-ttu-id="b7fd0-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b7fd0-141">System.Boolean</span></span>

## <span data-ttu-id="b7fd0-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="b7fd0-142">NOTES</span></span>

<span data-ttu-id="b7fd0-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b7fd0-143">ALIASES</span></span>

<span data-ttu-id="b7fd0-144">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b7fd0-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b7fd0-145">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7fd0-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b7fd0-147">INPUTOBJECT <ICloudServiceIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="b7fd0-147">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b7fd0-148">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b7fd0-148">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="b7fd0-149">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b7fd0-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b7fd0-150">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b7fd0-150">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="b7fd0-151">`[RoleInstanceName <String>]`: nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-151">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="b7fd0-152">`[RoleName <String>]`: nome del ruolo.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-152">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="b7fd0-153">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b7fd0-154">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b7fd0-155">`[UpdateDomain <Int32?>]`: specifica un valore intero che identifica il dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-155">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="b7fd0-156">I domini di aggiornamento sono identificati con un indice in base zero: il primo dominio di aggiornamento ha un ID pari a 0, il secondo con id 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="b7fd0-156">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="b7fd0-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7fd0-157">RELATED LINKS</span></span>

