---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/stop-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3f98161e56019394dc67ab8909aac3fb70a611a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188999"
---
# <span data-ttu-id="71810-101">Stop-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="71810-101">Stop-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="71810-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71810-102">SYNOPSIS</span></span>
<span data-ttu-id="71810-103">Interrompere la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="71810-103">Stop the deployment.</span></span>

## <span data-ttu-id="71810-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71810-104">SYNTAX</span></span>

### <span data-ttu-id="71810-105">Interrompi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71810-105">Stop (Default)</span></span>
```
Stop-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="71810-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="71810-106">StopViaIdentity</span></span>
```
Stop-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="71810-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="71810-107">DESCRIPTION</span></span>
<span data-ttu-id="71810-108">Interrompere la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="71810-108">Stop the deployment.</span></span>

## <span data-ttu-id="71810-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71810-109">EXAMPLES</span></span>

### <span data-ttu-id="71810-110">Esempio 1: Interrompere il servizio Cloud Spring in base al nome.</span><span class="sxs-lookup"><span data-stu-id="71810-110">Example 1: Stop Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Stop-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="71810-111">Interrompere il servizio Cloud Spring in base al nome.</span><span class="sxs-lookup"><span data-stu-id="71810-111">Stop Spring Cloud Service by name.</span></span>

### <span data-ttu-id="71810-112">Esempio 2: interrompere la pipe del servizio cloud Spring.</span><span class="sxs-lookup"><span data-stu-id="71810-112">Example 2: Stop Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Stop-AzSpringCloud
```

<span data-ttu-id="71810-113">Interrompi la distribuzione di Spring Cloud Service.</span><span class="sxs-lookup"><span data-stu-id="71810-113">Stop Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="71810-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71810-114">PARAMETERS</span></span>

### <span data-ttu-id="71810-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="71810-115">-AppName</span></span>
<span data-ttu-id="71810-116">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="71810-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71810-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71810-117">-AsJob</span></span>
<span data-ttu-id="71810-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="71810-118">Run the command as a job</span></span>

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

### <span data-ttu-id="71810-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71810-119">-DefaultProfile</span></span>
<span data-ttu-id="71810-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71810-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71810-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71810-121">-InputObject</span></span>
<span data-ttu-id="71810-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="71810-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71810-123">-Name</span><span class="sxs-lookup"><span data-stu-id="71810-123">-Name</span></span>
<span data-ttu-id="71810-124">Nome della risorsa distribuzione.</span><span class="sxs-lookup"><span data-stu-id="71810-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71810-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="71810-125">-NoWait</span></span>
<span data-ttu-id="71810-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="71810-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="71810-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71810-127">-PassThru</span></span>
<span data-ttu-id="71810-128">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="71810-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="71810-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71810-129">-ResourceGroupName</span></span>
<span data-ttu-id="71810-130">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="71810-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="71810-131">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="71810-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71810-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="71810-132">-ServiceName</span></span>
<span data-ttu-id="71810-133">Nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="71810-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71810-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71810-134">-SubscriptionId</span></span>
<span data-ttu-id="71810-135">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="71810-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="71810-136">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="71810-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71810-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71810-137">-Confirm</span></span>
<span data-ttu-id="71810-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71810-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71810-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71810-139">-WhatIf</span></span>
<span data-ttu-id="71810-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71810-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71810-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71810-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71810-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71810-142">CommonParameters</span></span>
<span data-ttu-id="71810-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71810-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71810-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="71810-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71810-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="71810-145">INPUTS</span></span>

### <span data-ttu-id="71810-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="71810-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="71810-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71810-147">OUTPUTS</span></span>

### <span data-ttu-id="71810-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="71810-148">System.Boolean</span></span>

## <span data-ttu-id="71810-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="71810-149">NOTES</span></span>

<span data-ttu-id="71810-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="71810-150">ALIASES</span></span>

<span data-ttu-id="71810-151">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="71810-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="71810-152">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="71810-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71810-153">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="71810-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="71810-154">INPUTOBJECT <ISpringCloudIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="71810-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="71810-155">`[AppName <String>]`: nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="71810-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="71810-156">`[BindingName <String>]`: nome della risorsa di associazione.</span><span class="sxs-lookup"><span data-stu-id="71810-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="71810-157">`[CertificateName <String>]`: nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="71810-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="71810-158">`[DeploymentName <String>]`: nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="71810-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="71810-159">`[DomainName <String>]`: nome della risorsa di dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="71810-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="71810-160">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="71810-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="71810-161">`[Location <String>]`: l'area geografica</span><span class="sxs-lookup"><span data-stu-id="71810-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="71810-162">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="71810-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="71810-163">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="71810-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="71810-164">`[ServiceName <String>]`: nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="71810-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="71810-165">`[SubscriptionId <String>]`: recupera l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="71810-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="71810-166">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="71810-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="71810-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71810-167">RELATED LINKS</span></span>

