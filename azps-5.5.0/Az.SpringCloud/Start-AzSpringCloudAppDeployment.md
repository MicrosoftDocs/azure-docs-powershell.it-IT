---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/start-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 7cab91bf5c7e95258f17a73da4e2b177e30444c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197775"
---
# <span data-ttu-id="7d34e-101">Start-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="7d34e-101">Start-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="7d34e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d34e-102">SYNOPSIS</span></span>
<span data-ttu-id="7d34e-103">Avviare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7d34e-103">Start the deployment.</span></span>

## <span data-ttu-id="7d34e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d34e-104">SYNTAX</span></span>

### <span data-ttu-id="7d34e-105">Start (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d34e-105">Start (Default)</span></span>
```
Start-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7d34e-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7d34e-106">StartViaIdentity</span></span>
```
Start-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7d34e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7d34e-107">DESCRIPTION</span></span>
<span data-ttu-id="7d34e-108">Avviare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7d34e-108">Start the deployment.</span></span>

## <span data-ttu-id="7d34e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d34e-109">EXAMPLES</span></span>

### <span data-ttu-id="7d34e-110">Esempio 1: Avviare il servizio Cloud Spring in base al nome.</span><span class="sxs-lookup"><span data-stu-id="7d34e-110">Example 1: Start Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Start-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="7d34e-111">Avvia il servizio Cloud Spring in base al nome.</span><span class="sxs-lookup"><span data-stu-id="7d34e-111">Start Spring Cloud Service by name.</span></span>

### <span data-ttu-id="7d34e-112">Esempio 2: Avviare il servizio Cloud Spring da pipe.</span><span class="sxs-lookup"><span data-stu-id="7d34e-112">Example 2: Start Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Start-AzSpringCloud
```

<span data-ttu-id="7d34e-113">Avvia il servizio Cloud Spring dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="7d34e-113">Start Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="7d34e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d34e-114">PARAMETERS</span></span>

### <span data-ttu-id="7d34e-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="7d34e-115">-AppName</span></span>
<span data-ttu-id="7d34e-116">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="7d34e-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="7d34e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d34e-117">-AsJob</span></span>
<span data-ttu-id="7d34e-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="7d34e-118">Run the command as a job</span></span>

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

### <span data-ttu-id="7d34e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d34e-119">-DefaultProfile</span></span>
<span data-ttu-id="7d34e-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d34e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d34e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d34e-121">-InputObject</span></span>
<span data-ttu-id="7d34e-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7d34e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d34e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7d34e-123">-Name</span></span>
<span data-ttu-id="7d34e-124">Nome della risorsa distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7d34e-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d34e-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7d34e-125">-NoWait</span></span>
<span data-ttu-id="7d34e-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="7d34e-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7d34e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d34e-127">-PassThru</span></span>
<span data-ttu-id="7d34e-128">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="7d34e-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7d34e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d34e-129">-ResourceGroupName</span></span>
<span data-ttu-id="7d34e-130">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7d34e-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7d34e-131">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="7d34e-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7d34e-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7d34e-132">-ServiceName</span></span>
<span data-ttu-id="7d34e-133">Nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="7d34e-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="7d34e-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d34e-134">-SubscriptionId</span></span>
<span data-ttu-id="7d34e-135">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7d34e-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7d34e-136">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="7d34e-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7d34e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d34e-137">-Confirm</span></span>
<span data-ttu-id="7d34e-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d34e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d34e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d34e-139">-WhatIf</span></span>
<span data-ttu-id="7d34e-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d34e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d34e-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d34e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d34e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d34e-142">CommonParameters</span></span>
<span data-ttu-id="7d34e-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d34e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d34e-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7d34e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d34e-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="7d34e-145">INPUTS</span></span>

### <span data-ttu-id="7d34e-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="7d34e-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="7d34e-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d34e-147">OUTPUTS</span></span>

### <span data-ttu-id="7d34e-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7d34e-148">System.Boolean</span></span>

## <span data-ttu-id="7d34e-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="7d34e-149">NOTES</span></span>

<span data-ttu-id="7d34e-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7d34e-150">ALIASES</span></span>

<span data-ttu-id="7d34e-151">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="7d34e-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7d34e-152">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="7d34e-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7d34e-153">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7d34e-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7d34e-154">INPUTOBJECT <ISpringCloudIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="7d34e-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7d34e-155">`[AppName <String>]`: nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="7d34e-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="7d34e-156">`[BindingName <String>]`: nome della risorsa di associazione.</span><span class="sxs-lookup"><span data-stu-id="7d34e-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="7d34e-157">`[CertificateName <String>]`: nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="7d34e-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="7d34e-158">`[DeploymentName <String>]`: nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7d34e-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="7d34e-159">`[DomainName <String>]`: nome della risorsa di dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7d34e-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="7d34e-160">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="7d34e-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7d34e-161">`[Location <String>]`: l'area geografica</span><span class="sxs-lookup"><span data-stu-id="7d34e-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="7d34e-162">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7d34e-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="7d34e-163">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="7d34e-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="7d34e-164">`[ServiceName <String>]`: nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="7d34e-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="7d34e-165">`[SubscriptionId <String>]`: recupera l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7d34e-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="7d34e-166">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="7d34e-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7d34e-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d34e-167">RELATED LINKS</span></span>

