---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancereimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
ms.openlocfilehash: 644912b841475c660852adcda2cba320d9026618
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965054"
---
# <span data-ttu-id="d54db-101">Invoke-AzCloudServiceRoleInstanceReimage</span><span class="sxs-lookup"><span data-stu-id="d54db-101">Invoke-AzCloudServiceRoleInstanceReimage</span></span>

## <span data-ttu-id="d54db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d54db-102">SYNOPSIS</span></span>
<span data-ttu-id="d54db-103">L'operazione asincrona Istanza ruolo di Reimage reinstalla il sistema operativo in istanze di ruoli Web o ruoli di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d54db-103">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="d54db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d54db-104">SYNTAX</span></span>

### <span data-ttu-id="d54db-105">Reimage (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d54db-105">Reimage (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d54db-106">ReimageViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d54db-106">ReimageViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d54db-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d54db-107">DESCRIPTION</span></span>
<span data-ttu-id="d54db-108">L'operazione asincrona Istanza ruolo di Reimage reinstalla il sistema operativo in istanze di ruoli Web o ruoli di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d54db-108">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="d54db-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d54db-109">EXAMPLES</span></span>

### <span data-ttu-id="d54db-110">Esempio 1: Istanza del ruolo Reimage di un servizio cloud</span><span class="sxs-lookup"><span data-stu-id="d54db-110">Example 1: Reimage role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="d54db-111">Questo comando ricrea l'istanza del ruolo ContosoFrontEnd_IN_0 nome di un servizio cloud denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="d54db-111">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="d54db-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d54db-112">PARAMETERS</span></span>

### <span data-ttu-id="d54db-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d54db-113">-AsJob</span></span>
<span data-ttu-id="d54db-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="d54db-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d54db-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="d54db-115">-CloudServiceName</span></span>
<span data-ttu-id="d54db-116">.</span><span class="sxs-lookup"><span data-stu-id="d54db-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d54db-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d54db-117">-DefaultProfile</span></span>
<span data-ttu-id="d54db-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d54db-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d54db-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d54db-119">-InputObject</span></span>
<span data-ttu-id="d54db-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d54db-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: ReimageViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d54db-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d54db-121">-NoWait</span></span>
<span data-ttu-id="d54db-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="d54db-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d54db-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d54db-123">-PassThru</span></span>
<span data-ttu-id="d54db-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="d54db-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d54db-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d54db-125">-ResourceGroupName</span></span>
<span data-ttu-id="d54db-126">.</span><span class="sxs-lookup"><span data-stu-id="d54db-126">.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d54db-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="d54db-127">-RoleInstanceName</span></span>
<span data-ttu-id="d54db-128">Nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="d54db-128">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d54db-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d54db-129">-SubscriptionId</span></span>
<span data-ttu-id="d54db-130">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d54db-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d54db-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d54db-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d54db-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d54db-132">-Confirm</span></span>
<span data-ttu-id="d54db-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d54db-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d54db-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d54db-134">-WhatIf</span></span>
<span data-ttu-id="d54db-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d54db-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d54db-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d54db-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d54db-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d54db-137">CommonParameters</span></span>
<span data-ttu-id="d54db-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d54db-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d54db-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d54db-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d54db-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="d54db-140">INPUTS</span></span>

### <span data-ttu-id="d54db-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="d54db-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="d54db-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d54db-142">OUTPUTS</span></span>

### <span data-ttu-id="d54db-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d54db-143">System.Boolean</span></span>

## <span data-ttu-id="d54db-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="d54db-144">NOTES</span></span>

<span data-ttu-id="d54db-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d54db-145">ALIASES</span></span>

<span data-ttu-id="d54db-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="d54db-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d54db-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d54db-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d54db-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d54db-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d54db-149">INPUTOBJECT <ICloudServiceIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="d54db-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d54db-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="d54db-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="d54db-151">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="d54db-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d54db-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="d54db-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="d54db-153">`[RoleInstanceName <String>]`: nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="d54db-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="d54db-154">`[RoleName <String>]`: nome del ruolo.</span><span class="sxs-lookup"><span data-stu-id="d54db-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="d54db-155">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d54db-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d54db-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d54db-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d54db-157">`[UpdateDomain <Int32?>]`: specifica un valore intero che identifica il dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="d54db-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="d54db-158">I domini di aggiornamento sono identificati con un indice in base zero: il primo dominio di aggiornamento ha un ID pari a 0, il secondo con id 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="d54db-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="d54db-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d54db-159">RELATED LINKS</span></span>

