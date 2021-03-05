---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/restart-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
ms.openlocfilehash: f184696dbcfce35bf6e52f889d2c787214330e70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985304"
---
# <span data-ttu-id="dd32a-101">Restart-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="dd32a-101">Restart-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="dd32a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd32a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd32a-103">L'operazione asincrona Riavvia istanza ruolo richiede il riavvio di un'istanza del ruolo nel servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="dd32a-103">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="dd32a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd32a-104">SYNTAX</span></span>

### <span data-ttu-id="dd32a-105">Riavvia (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dd32a-105">Restart (Default)</span></span>
```
Restart-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dd32a-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dd32a-106">RestartViaIdentity</span></span>
```
Restart-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dd32a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dd32a-107">DESCRIPTION</span></span>
<span data-ttu-id="dd32a-108">L'operazione asincrona Riavvia istanza ruolo richiede il riavvio di un'istanza del ruolo nel servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="dd32a-108">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="dd32a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd32a-109">EXAMPLES</span></span>

### <span data-ttu-id="dd32a-110">Esempio 1: Riavviare l'istanza del ruolo di un servizio cloud</span><span class="sxs-lookup"><span data-stu-id="dd32a-110">Example 1: Restart role instance of a cloud service</span></span>
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="dd32a-111">Questo comando riavvia l'istanza del ruolo ContosoFrontEnd_IN_0 servizio cloud denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="dd32a-111">This command restarts role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="dd32a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd32a-112">PARAMETERS</span></span>

### <span data-ttu-id="dd32a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd32a-113">-AsJob</span></span>
<span data-ttu-id="dd32a-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="dd32a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="dd32a-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="dd32a-115">-CloudServiceName</span></span>
<span data-ttu-id="dd32a-116">.</span><span class="sxs-lookup"><span data-stu-id="dd32a-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd32a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd32a-117">-DefaultProfile</span></span>
<span data-ttu-id="dd32a-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd32a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd32a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd32a-119">-InputObject</span></span>
<span data-ttu-id="dd32a-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="dd32a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd32a-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dd32a-121">-NoWait</span></span>
<span data-ttu-id="dd32a-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="dd32a-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dd32a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd32a-123">-PassThru</span></span>
<span data-ttu-id="dd32a-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="dd32a-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dd32a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd32a-125">-ResourceGroupName</span></span>
<span data-ttu-id="dd32a-126">.</span><span class="sxs-lookup"><span data-stu-id="dd32a-126">.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd32a-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="dd32a-127">-RoleInstanceName</span></span>
<span data-ttu-id="dd32a-128">Nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="dd32a-128">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd32a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd32a-129">-SubscriptionId</span></span>
<span data-ttu-id="dd32a-130">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dd32a-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dd32a-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="dd32a-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd32a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd32a-132">-Confirm</span></span>
<span data-ttu-id="dd32a-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd32a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd32a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd32a-134">-WhatIf</span></span>
<span data-ttu-id="dd32a-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd32a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd32a-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd32a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd32a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd32a-137">CommonParameters</span></span>
<span data-ttu-id="dd32a-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd32a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd32a-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dd32a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd32a-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="dd32a-140">INPUTS</span></span>

### <span data-ttu-id="dd32a-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="dd32a-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="dd32a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd32a-142">OUTPUTS</span></span>

### <span data-ttu-id="dd32a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dd32a-143">System.Boolean</span></span>

## <span data-ttu-id="dd32a-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="dd32a-144">NOTES</span></span>

<span data-ttu-id="dd32a-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="dd32a-145">ALIASES</span></span>

<span data-ttu-id="dd32a-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="dd32a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dd32a-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="dd32a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd32a-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dd32a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dd32a-149">INPUTOBJECT <ICloudServiceIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="dd32a-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dd32a-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="dd32a-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="dd32a-151">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="dd32a-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dd32a-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="dd32a-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="dd32a-153">`[RoleInstanceName <String>]`: nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="dd32a-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="dd32a-154">`[RoleName <String>]`: nome del ruolo.</span><span class="sxs-lookup"><span data-stu-id="dd32a-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="dd32a-155">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dd32a-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dd32a-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="dd32a-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="dd32a-157">`[UpdateDomain <Int32?>]`: specifica un valore intero che identifica il dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="dd32a-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="dd32a-158">I domini di aggiornamento sono identificati con un indice in base zero: il primo dominio di aggiornamento ha un ID pari a 0, il secondo con id 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="dd32a-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="dd32a-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd32a-159">RELATED LINKS</span></span>

