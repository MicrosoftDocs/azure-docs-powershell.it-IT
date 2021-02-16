---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/invoke-azcloudservicerebuild
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRebuild.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRebuild.md
ms.openlocfilehash: 1efeb45704898588c7ba8f08148f88d0eaf3e5c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199439"
---
# <span data-ttu-id="adf3f-101">Invoke-AzCloudServiceRebuild</span><span class="sxs-lookup"><span data-stu-id="adf3f-101">Invoke-AzCloudServiceRebuild</span></span>

## <span data-ttu-id="adf3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adf3f-102">SYNOPSIS</span></span>
<span data-ttu-id="adf3f-103">Rebuild Role Instances reinstalla il sistema operativo in istanze di ruoli Web o ruoli di lavoro e inizializza le risorse di archiviazione usate.</span><span class="sxs-lookup"><span data-stu-id="adf3f-103">Rebuild Role Instances reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="adf3f-104">Se non si vogliono inizializzare le risorse di archiviazione, è possibile usare le istanze del ruolo Reimage.</span><span class="sxs-lookup"><span data-stu-id="adf3f-104">If you do not want to initialize storage resources, you can use Reimage Role Instances.</span></span>

## <span data-ttu-id="adf3f-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="adf3f-105">SYNTAX</span></span>

### <span data-ttu-id="adf3f-106">RebuildExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="adf3f-106">RebuildExpanded (Default)</span></span>
```
Invoke-AzCloudServiceRebuild -CloudServiceName <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="adf3f-107">RebuildViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="adf3f-107">RebuildViaIdentityExpanded</span></span>
```
Invoke-AzCloudServiceRebuild -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="adf3f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="adf3f-108">DESCRIPTION</span></span>
<span data-ttu-id="adf3f-109">Ricrea istanze del ruolo reinstalla il sistema operativo in istanze di ruoli Web o ruoli di lavoro e inizializza le risorse di archiviazione usate.</span><span class="sxs-lookup"><span data-stu-id="adf3f-109">Rebuild Role Instances reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="adf3f-110">Se non si vogliono inizializzare le risorse di archiviazione, è possibile usare le istanze del ruolo Reimage.</span><span class="sxs-lookup"><span data-stu-id="adf3f-110">If you do not want to initialize storage resources, you can use Reimage Role Instances.</span></span>

## <span data-ttu-id="adf3f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="adf3f-111">EXAMPLES</span></span>

### <span data-ttu-id="adf3f-112">Esempio 1: Ricreare le istanze del ruolo del servizio cloud</span><span class="sxs-lookup"><span data-stu-id="adf3f-112">Example 1: Rebuild role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Invoke-AzCloudServiceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="adf3f-113">Questo comando ricostruisce 2 istanze di ruoli ContosoFrontEnd_IN_0 e ContosoBackEnd_IN_1 del servizio cloud denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="adf3f-113">This command rebuilds 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="adf3f-114">Esempio 2: Ricostruire tutti i ruoli del servizio cloud</span><span class="sxs-lookup"><span data-stu-id="adf3f-114">Example 2: Rebuild all roles of cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="adf3f-115">Questo comando ricostruisce tutte le istanze di ruolo del servizio cloud denominate ContosoCS che appartengono al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="adf3f-115">This command rebuilds all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="adf3f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adf3f-116">PARAMETERS</span></span>

### <span data-ttu-id="adf3f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="adf3f-117">-AsJob</span></span>
<span data-ttu-id="adf3f-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="adf3f-118">Run the command as a job</span></span>

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

### <span data-ttu-id="adf3f-119">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="adf3f-119">-CloudServiceName</span></span>
<span data-ttu-id="adf3f-120">Nome del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="adf3f-120">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf3f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adf3f-121">-DefaultProfile</span></span>
<span data-ttu-id="adf3f-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="adf3f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adf3f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adf3f-123">-InputObject</span></span>
<span data-ttu-id="adf3f-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="adf3f-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RebuildViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adf3f-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="adf3f-125">-NoWait</span></span>
<span data-ttu-id="adf3f-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="adf3f-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="adf3f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adf3f-127">-PassThru</span></span>
<span data-ttu-id="adf3f-128">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="adf3f-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="adf3f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adf3f-129">-ResourceGroupName</span></span>
<span data-ttu-id="adf3f-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="adf3f-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf3f-131">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="adf3f-131">-RoleInstance</span></span>
<span data-ttu-id="adf3f-132">Elenco dei nomi di istanza dei ruoli del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="adf3f-132">List of cloud service role instance names.</span></span>
<span data-ttu-id="adf3f-133">Il valore "\*" indica tutte le istanze del ruolo del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="adf3f-133">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="adf3f-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="adf3f-134">-SubscriptionId</span></span>
<span data-ttu-id="adf3f-135">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="adf3f-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="adf3f-136">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="adf3f-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf3f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="adf3f-137">-Confirm</span></span>
<span data-ttu-id="adf3f-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adf3f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adf3f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adf3f-139">-WhatIf</span></span>
<span data-ttu-id="adf3f-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="adf3f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adf3f-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="adf3f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adf3f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adf3f-142">CommonParameters</span></span>
<span data-ttu-id="adf3f-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adf3f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adf3f-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="adf3f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adf3f-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="adf3f-145">INPUTS</span></span>

### <span data-ttu-id="adf3f-146">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="adf3f-146">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="adf3f-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="adf3f-147">OUTPUTS</span></span>

### <span data-ttu-id="adf3f-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="adf3f-148">System.Boolean</span></span>

## <span data-ttu-id="adf3f-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="adf3f-149">NOTES</span></span>

<span data-ttu-id="adf3f-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="adf3f-150">ALIASES</span></span>

<span data-ttu-id="adf3f-151">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="adf3f-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="adf3f-152">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="adf3f-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="adf3f-153">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="adf3f-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="adf3f-154">INPUTOBJECT <ICloudServiceIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="adf3f-154">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="adf3f-155">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="adf3f-155">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="adf3f-156">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="adf3f-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="adf3f-157">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="adf3f-157">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="adf3f-158">`[RoleInstanceName <String>]`: nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="adf3f-158">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="adf3f-159">`[RoleName <String>]`: nome del ruolo.</span><span class="sxs-lookup"><span data-stu-id="adf3f-159">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="adf3f-160">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="adf3f-160">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="adf3f-161">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="adf3f-161">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="adf3f-162">`[UpdateDomain <Int32?>]`: specifica un valore intero che identifica il dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="adf3f-162">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="adf3f-163">I domini di aggiornamento sono identificati con un indice in base zero: il primo dominio di aggiornamento ha un ID pari a 0, il secondo con id 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="adf3f-163">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="adf3f-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="adf3f-164">RELATED LINKS</span></span>

