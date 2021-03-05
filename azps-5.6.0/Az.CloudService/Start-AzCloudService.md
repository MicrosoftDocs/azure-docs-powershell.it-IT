---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/start-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Start-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Start-AzCloudService.md
ms.openlocfilehash: 7bbd639c670112a227e90ee1f9a4b07171673fbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986171"
---
# <span data-ttu-id="57cf7-101">Start-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="57cf7-101">Start-AzCloudService</span></span>

## <span data-ttu-id="57cf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="57cf7-103">Avvia il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="57cf7-103">Starts the cloud service.</span></span>

## <span data-ttu-id="57cf7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57cf7-104">SYNTAX</span></span>

### <span data-ttu-id="57cf7-105">Start (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="57cf7-105">Start (Default)</span></span>
```
Start-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="57cf7-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="57cf7-106">StartViaIdentity</span></span>
```
Start-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="57cf7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="57cf7-107">DESCRIPTION</span></span>
<span data-ttu-id="57cf7-108">Avvia il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="57cf7-108">Starts the cloud service.</span></span>

## <span data-ttu-id="57cf7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57cf7-109">EXAMPLES</span></span>

### <span data-ttu-id="57cf7-110">Esempio 1: Avviare il servizio cloud</span><span class="sxs-lookup"><span data-stu-id="57cf7-110">Example 1: Start cloud service</span></span>
```powershell
PS C:\> Start-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="57cf7-111">Questo comando avvia tutte le istanze di ruoli che appartengono al servizio cloud denominato ContosoCS.</span><span class="sxs-lookup"><span data-stu-id="57cf7-111">This command starts all the role instances that belong to the the cloud service named ContosoCS.</span></span>

## <span data-ttu-id="57cf7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57cf7-112">PARAMETERS</span></span>

### <span data-ttu-id="57cf7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57cf7-113">-AsJob</span></span>
<span data-ttu-id="57cf7-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="57cf7-114">Run the command as a job</span></span>

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

### <span data-ttu-id="57cf7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57cf7-115">-DefaultProfile</span></span>
<span data-ttu-id="57cf7-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57cf7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57cf7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57cf7-117">-InputObject</span></span>
<span data-ttu-id="57cf7-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="57cf7-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57cf7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="57cf7-119">-Name</span></span>
<span data-ttu-id="57cf7-120">Nome del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="57cf7-120">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57cf7-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="57cf7-121">-NoWait</span></span>
<span data-ttu-id="57cf7-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="57cf7-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="57cf7-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57cf7-123">-PassThru</span></span>
<span data-ttu-id="57cf7-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="57cf7-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="57cf7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57cf7-125">-ResourceGroupName</span></span>
<span data-ttu-id="57cf7-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="57cf7-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57cf7-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57cf7-127">-SubscriptionId</span></span>
<span data-ttu-id="57cf7-128">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="57cf7-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="57cf7-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="57cf7-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57cf7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57cf7-130">-Confirm</span></span>
<span data-ttu-id="57cf7-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57cf7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57cf7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57cf7-132">-WhatIf</span></span>
<span data-ttu-id="57cf7-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57cf7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57cf7-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57cf7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57cf7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57cf7-135">CommonParameters</span></span>
<span data-ttu-id="57cf7-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57cf7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57cf7-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="57cf7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57cf7-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="57cf7-138">INPUTS</span></span>

### <span data-ttu-id="57cf7-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="57cf7-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="57cf7-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57cf7-140">OUTPUTS</span></span>

### <span data-ttu-id="57cf7-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57cf7-141">System.Boolean</span></span>

## <span data-ttu-id="57cf7-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="57cf7-142">NOTES</span></span>

<span data-ttu-id="57cf7-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="57cf7-143">ALIASES</span></span>

<span data-ttu-id="57cf7-144">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="57cf7-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57cf7-145">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="57cf7-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57cf7-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="57cf7-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57cf7-147">INPUTOBJECT <ICloudServiceIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="57cf7-147">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57cf7-148">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="57cf7-148">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="57cf7-149">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="57cf7-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57cf7-150">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="57cf7-150">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="57cf7-151">`[RoleInstanceName <String>]`: nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="57cf7-151">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="57cf7-152">`[RoleName <String>]`: nome del ruolo.</span><span class="sxs-lookup"><span data-stu-id="57cf7-152">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="57cf7-153">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="57cf7-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="57cf7-154">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="57cf7-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="57cf7-155">`[UpdateDomain <Int32?>]`: specifica un valore intero che identifica il dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="57cf7-155">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="57cf7-156">I domini di aggiornamento sono identificati con un indice in base zero: il primo dominio di aggiornamento ha un ID pari a 0, il secondo con id 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="57cf7-156">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="57cf7-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57cf7-157">RELATED LINKS</span></span>

