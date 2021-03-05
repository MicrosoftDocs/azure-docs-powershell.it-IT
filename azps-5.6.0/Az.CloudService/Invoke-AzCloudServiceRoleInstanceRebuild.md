---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancerebuild
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
ms.openlocfilehash: 1f204b40bcf6cbd81449a6478d9d7d4e3f7d432d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007230"
---
# <span data-ttu-id="3bd3f-101">Invoke-AzCloudServiceRoleInstanceRebuild</span><span class="sxs-lookup"><span data-stu-id="3bd3f-101">Invoke-AzCloudServiceRoleInstanceRebuild</span></span>

## <span data-ttu-id="3bd3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bd3f-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd3f-103">L'operazione asincrona Ricostruisci istanza ruolo reinstalla il sistema operativo in istanze di ruoli Web o ruoli di lavoro e inizializza le risorse di archiviazione usate.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-103">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="3bd3f-104">Se non si vogliono inizializzare le risorse di archiviazione, è possibile usare l'istanza del ruolo Reimage.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-104">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="3bd3f-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3bd3f-105">SYNTAX</span></span>

### <span data-ttu-id="3bd3f-106">Ricostruisci (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3bd3f-106">Rebuild (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3bd3f-107">RebuildViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3bd3f-107">RebuildViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3bd3f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3bd3f-108">DESCRIPTION</span></span>
<span data-ttu-id="3bd3f-109">L'operazione asincrona Ricostruisci istanza ruolo reinstalla il sistema operativo in istanze di ruoli Web o ruoli di lavoro e inizializza le risorse di archiviazione usate.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-109">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="3bd3f-110">Se non si vogliono inizializzare le risorse di archiviazione, è possibile usare l'istanza del ruolo Reimage.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-110">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="3bd3f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3bd3f-111">EXAMPLES</span></span>

### <span data-ttu-id="3bd3f-112">Esempio 1: Ricostruire l'istanza del ruolo di un servizio cloud</span><span class="sxs-lookup"><span data-stu-id="3bd3f-112">Example 1: Rebuild role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="3bd3f-113">Questo comando ricrea l'istanza del ruolo ContosoFrontEnd_IN_0 nome di un servizio cloud denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-113">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="3bd3f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bd3f-114">PARAMETERS</span></span>

### <span data-ttu-id="3bd3f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3bd3f-115">-AsJob</span></span>
<span data-ttu-id="3bd3f-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="3bd3f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3bd3f-117">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="3bd3f-117">-CloudServiceName</span></span>
<span data-ttu-id="3bd3f-118">.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-118">.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd3f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd3f-119">-DefaultProfile</span></span>
<span data-ttu-id="3bd3f-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bd3f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bd3f-121">-InputObject</span></span>
<span data-ttu-id="3bd3f-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RebuildViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd3f-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3bd3f-123">-NoWait</span></span>
<span data-ttu-id="3bd3f-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="3bd3f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3bd3f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bd3f-125">-PassThru</span></span>
<span data-ttu-id="3bd3f-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="3bd3f-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3bd3f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bd3f-127">-ResourceGroupName</span></span>
<span data-ttu-id="3bd3f-128">.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-128">.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd3f-129">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="3bd3f-129">-RoleInstanceName</span></span>
<span data-ttu-id="3bd3f-130">Nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-130">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd3f-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3bd3f-131">-SubscriptionId</span></span>
<span data-ttu-id="3bd3f-132">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3bd3f-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd3f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3bd3f-134">-Confirm</span></span>
<span data-ttu-id="3bd3f-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bd3f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bd3f-136">-WhatIf</span></span>
<span data-ttu-id="3bd3f-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bd3f-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bd3f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd3f-139">CommonParameters</span></span>
<span data-ttu-id="3bd3f-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd3f-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd3f-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="3bd3f-142">INPUTS</span></span>

### <span data-ttu-id="3bd3f-143">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="3bd3f-143">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="3bd3f-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3bd3f-144">OUTPUTS</span></span>

### <span data-ttu-id="3bd3f-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3bd3f-145">System.Boolean</span></span>

## <span data-ttu-id="3bd3f-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="3bd3f-146">NOTES</span></span>

<span data-ttu-id="3bd3f-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3bd3f-147">ALIASES</span></span>

<span data-ttu-id="3bd3f-148">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="3bd3f-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3bd3f-149">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3bd3f-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3bd3f-151">INPUTOBJECT <ICloudServiceIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="3bd3f-151">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3bd3f-152">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="3bd3f-152">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="3bd3f-153">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="3bd3f-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3bd3f-154">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="3bd3f-154">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="3bd3f-155">`[RoleInstanceName <String>]`: nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-155">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="3bd3f-156">`[RoleName <String>]`: nome del ruolo.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-156">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="3bd3f-157">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-157">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3bd3f-158">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3bd3f-159">`[UpdateDomain <Int32?>]`: specifica un valore intero che identifica il dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-159">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="3bd3f-160">I domini di aggiornamento sono identificati con un indice in base zero: il primo dominio di aggiornamento ha un ID pari a 0, il secondo con id 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="3bd3f-160">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="3bd3f-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3bd3f-161">RELATED LINKS</span></span>

