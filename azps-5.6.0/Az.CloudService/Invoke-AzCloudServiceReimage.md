---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/invoke-azcloudservicereimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceReimage.md
ms.openlocfilehash: d82b3038ad797354f000de379964b3da3a7f135b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991688"
---
# <span data-ttu-id="64786-101">Invoke-AzCloudServiceReimage</span><span class="sxs-lookup"><span data-stu-id="64786-101">Invoke-AzCloudServiceReimage</span></span>

## <span data-ttu-id="64786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64786-102">SYNOPSIS</span></span>
<span data-ttu-id="64786-103">L'operazione asincrona reimage reinstalla il sistema operativo in istanze di ruoli Web o ruoli di lavoro.</span><span class="sxs-lookup"><span data-stu-id="64786-103">Reimage asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="64786-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64786-104">SYNTAX</span></span>

### <span data-ttu-id="64786-105">ReimageExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="64786-105">ReimageExpanded (Default)</span></span>
```
Invoke-AzCloudServiceReimage -Name <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="64786-106">ReimageViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="64786-106">ReimageViaIdentityExpanded</span></span>
```
Invoke-AzCloudServiceReimage -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64786-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="64786-107">DESCRIPTION</span></span>
<span data-ttu-id="64786-108">L'operazione asincrona reimage reinstalla il sistema operativo in istanze di ruoli Web o ruoli di lavoro.</span><span class="sxs-lookup"><span data-stu-id="64786-108">Reimage asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="64786-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64786-109">EXAMPLES</span></span>

### <span data-ttu-id="64786-110">Esempio 1: Istanze del ruolo Reimage del servizio cloud</span><span class="sxs-lookup"><span data-stu-id="64786-110">Example 1: Reimage role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Invoke-AzCloudServiceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="64786-111">Questo comando reimmagine 2 istanze di ruoli ContosoFrontEnd_IN_0 e ContosoBackEnd_IN_1 di un servizio cloud denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="64786-111">This command reimages 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="64786-112">Esempio 2: Visualizzare nuovamente tutti i ruoli del servizio cloud</span><span class="sxs-lookup"><span data-stu-id="64786-112">Example 2: Reimage all roles of cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="64786-113">Questo comando ricrea l'immagine di tutte le istanze di ruolo del servizio cloud denominate ContosoCS che appartengono al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="64786-113">This command reimages all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="64786-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64786-114">PARAMETERS</span></span>

### <span data-ttu-id="64786-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64786-115">-AsJob</span></span>
<span data-ttu-id="64786-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="64786-116">Run the command as a job</span></span>

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

### <span data-ttu-id="64786-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64786-117">-DefaultProfile</span></span>
<span data-ttu-id="64786-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64786-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64786-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64786-119">-InputObject</span></span>
<span data-ttu-id="64786-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="64786-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: ReimageViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64786-121">-Name</span><span class="sxs-lookup"><span data-stu-id="64786-121">-Name</span></span>
<span data-ttu-id="64786-122">Nome del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="64786-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64786-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="64786-123">-NoWait</span></span>
<span data-ttu-id="64786-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="64786-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="64786-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64786-125">-PassThru</span></span>
<span data-ttu-id="64786-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="64786-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="64786-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64786-127">-ResourceGroupName</span></span>
<span data-ttu-id="64786-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="64786-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64786-129">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="64786-129">-RoleInstance</span></span>
<span data-ttu-id="64786-130">Elenco dei nomi di istanza dei ruoli del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="64786-130">List of cloud service role instance names.</span></span>
<span data-ttu-id="64786-131">Il valore "\*" indica tutte le istanze del ruolo del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="64786-131">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="64786-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64786-132">-SubscriptionId</span></span>
<span data-ttu-id="64786-133">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="64786-133">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="64786-134">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="64786-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64786-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64786-135">-Confirm</span></span>
<span data-ttu-id="64786-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64786-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64786-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64786-137">-WhatIf</span></span>
<span data-ttu-id="64786-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64786-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64786-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64786-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64786-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64786-140">CommonParameters</span></span>
<span data-ttu-id="64786-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64786-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64786-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="64786-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64786-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="64786-143">INPUTS</span></span>

### <span data-ttu-id="64786-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="64786-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="64786-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64786-145">OUTPUTS</span></span>

### <span data-ttu-id="64786-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="64786-146">System.Boolean</span></span>

## <span data-ttu-id="64786-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="64786-147">NOTES</span></span>

<span data-ttu-id="64786-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="64786-148">ALIASES</span></span>

<span data-ttu-id="64786-149">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="64786-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64786-150">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="64786-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64786-151">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64786-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64786-152">INPUTOBJECT <ICloudServiceIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="64786-152">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64786-153">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="64786-153">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="64786-154">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="64786-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64786-155">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="64786-155">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="64786-156">`[RoleInstanceName <String>]`: nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="64786-156">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="64786-157">`[RoleName <String>]`: nome del ruolo.</span><span class="sxs-lookup"><span data-stu-id="64786-157">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="64786-158">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="64786-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="64786-159">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="64786-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="64786-160">`[UpdateDomain <Int32?>]`: specifica un valore intero che identifica il dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="64786-160">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="64786-161">I domini di aggiornamento sono identificati con un indice in base zero: il primo dominio di aggiornamento ha un ID pari a 0, il secondo con id 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="64786-161">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="64786-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64786-162">RELATED LINKS</span></span>

