---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/stop-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
ms.openlocfilehash: 539106e979babd1df41ca2505a2978132e825b89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007214"
---
# <span data-ttu-id="740dd-101">Stop-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="740dd-101">Stop-AzCloudService</span></span>

## <span data-ttu-id="740dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="740dd-102">SYNOPSIS</span></span>
<span data-ttu-id="740dd-103">Disattivare il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="740dd-103">Power off the cloud service.</span></span>
<span data-ttu-id="740dd-104">Si noti che le risorse sono ancora allegata e che si riceve un costo per le risorse.</span><span class="sxs-lookup"><span data-stu-id="740dd-104">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="740dd-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="740dd-105">SYNTAX</span></span>

### <span data-ttu-id="740dd-106">PowerOff (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="740dd-106">PowerOff (Default)</span></span>
```
Stop-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="740dd-107">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="740dd-107">PowerOffViaIdentity</span></span>
```
Stop-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="740dd-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="740dd-108">DESCRIPTION</span></span>
<span data-ttu-id="740dd-109">Disattivare il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="740dd-109">Power off the cloud service.</span></span>
<span data-ttu-id="740dd-110">Si noti che le risorse sono ancora allegate e che si riceve un costo per le risorse.</span><span class="sxs-lookup"><span data-stu-id="740dd-110">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="740dd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="740dd-111">EXAMPLES</span></span>

### <span data-ttu-id="740dd-112">Esempio 1: Arrestare il servizio cloud</span><span class="sxs-lookup"><span data-stu-id="740dd-112">Example 1: Stop cloud service</span></span>
```powershell
PS C:\> Stop-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="740dd-113">Questo comando interrompe tutte le istanze di ruoli che appartengono al servizio cloud denominato ContosoCS.</span><span class="sxs-lookup"><span data-stu-id="740dd-113">This command stops all the role instances that belong to the the cloud service named ContosoCS.</span></span>

## <span data-ttu-id="740dd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="740dd-114">PARAMETERS</span></span>

### <span data-ttu-id="740dd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="740dd-115">-AsJob</span></span>
<span data-ttu-id="740dd-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="740dd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="740dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="740dd-117">-DefaultProfile</span></span>
<span data-ttu-id="740dd-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="740dd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="740dd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="740dd-119">-InputObject</span></span>
<span data-ttu-id="740dd-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="740dd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: PowerOffViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="740dd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="740dd-121">-Name</span></span>
<span data-ttu-id="740dd-122">Nome del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="740dd-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="740dd-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="740dd-123">-NoWait</span></span>
<span data-ttu-id="740dd-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="740dd-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="740dd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="740dd-125">-PassThru</span></span>
<span data-ttu-id="740dd-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="740dd-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="740dd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="740dd-127">-ResourceGroupName</span></span>
<span data-ttu-id="740dd-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="740dd-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="740dd-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="740dd-129">-SubscriptionId</span></span>
<span data-ttu-id="740dd-130">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="740dd-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="740dd-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="740dd-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="740dd-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="740dd-132">-Confirm</span></span>
<span data-ttu-id="740dd-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="740dd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="740dd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="740dd-134">-WhatIf</span></span>
<span data-ttu-id="740dd-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="740dd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="740dd-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="740dd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="740dd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="740dd-137">CommonParameters</span></span>
<span data-ttu-id="740dd-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="740dd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="740dd-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="740dd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="740dd-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="740dd-140">INPUTS</span></span>

### <span data-ttu-id="740dd-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="740dd-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="740dd-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="740dd-142">OUTPUTS</span></span>

### <span data-ttu-id="740dd-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="740dd-143">System.Boolean</span></span>

## <span data-ttu-id="740dd-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="740dd-144">NOTES</span></span>

<span data-ttu-id="740dd-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="740dd-145">ALIASES</span></span>

<span data-ttu-id="740dd-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="740dd-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="740dd-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="740dd-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="740dd-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="740dd-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="740dd-149">INPUTOBJECT <ICloudServiceIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="740dd-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="740dd-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="740dd-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="740dd-151">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="740dd-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="740dd-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="740dd-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="740dd-153">`[RoleInstanceName <String>]`: nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="740dd-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="740dd-154">`[RoleName <String>]`: nome del ruolo.</span><span class="sxs-lookup"><span data-stu-id="740dd-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="740dd-155">`[SubscriptionId <String>]`: le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="740dd-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="740dd-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="740dd-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="740dd-157">`[UpdateDomain <Int32?>]`: specifica un valore intero che identifica il dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="740dd-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="740dd-158">I domini di aggiornamento sono identificati con un indice in base zero: il primo dominio di aggiornamento ha un ID pari a 0, il secondo con id 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="740dd-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="740dd-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="740dd-159">RELATED LINKS</span></span>

