---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 25b7b5c93f769982364a0df8f14f5fbe2f804fa2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197783"
---
# <span data-ttu-id="91c06-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="91c06-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="91c06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91c06-102">SYNOPSIS</span></span>
<span data-ttu-id="91c06-103">Operazione di eliminazione di una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="91c06-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="91c06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91c06-104">SYNTAX</span></span>

### <span data-ttu-id="91c06-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="91c06-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="91c06-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="91c06-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="91c06-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="91c06-107">DESCRIPTION</span></span>
<span data-ttu-id="91c06-108">Operazione di eliminazione di una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="91c06-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="91c06-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91c06-109">EXAMPLES</span></span>

### <span data-ttu-id="91c06-110">Esempio 1: Rimuovere la distribuzione di Cloud Spring in base al nome.</span><span class="sxs-lookup"><span data-stu-id="91c06-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="91c06-111">Rimuovi La distribuzione di Spring Cloud in base al nome.</span><span class="sxs-lookup"><span data-stu-id="91c06-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="91c06-112">Esempio 2: Rimuovere la distribuzione cloud spring dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="91c06-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="91c06-113">Rimuovi Spring Cloud Deployment dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="91c06-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="91c06-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91c06-114">PARAMETERS</span></span>

### <span data-ttu-id="91c06-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="91c06-115">-AppName</span></span>
<span data-ttu-id="91c06-116">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="91c06-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="91c06-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91c06-117">-AsJob</span></span>
<span data-ttu-id="91c06-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="91c06-118">Run the command as a job</span></span>

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

### <span data-ttu-id="91c06-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c06-119">-DefaultProfile</span></span>
<span data-ttu-id="91c06-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91c06-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91c06-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91c06-121">-InputObject</span></span>
<span data-ttu-id="91c06-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="91c06-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91c06-123">-Name</span><span class="sxs-lookup"><span data-stu-id="91c06-123">-Name</span></span>
<span data-ttu-id="91c06-124">Nome della risorsa distribuzione.</span><span class="sxs-lookup"><span data-stu-id="91c06-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c06-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="91c06-125">-NoWait</span></span>
<span data-ttu-id="91c06-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="91c06-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="91c06-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91c06-127">-PassThru</span></span>
<span data-ttu-id="91c06-128">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="91c06-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="91c06-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91c06-129">-ResourceGroupName</span></span>
<span data-ttu-id="91c06-130">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="91c06-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="91c06-131">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="91c06-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="91c06-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="91c06-132">-ServiceName</span></span>
<span data-ttu-id="91c06-133">Nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="91c06-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="91c06-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91c06-134">-SubscriptionId</span></span>
<span data-ttu-id="91c06-135">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="91c06-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="91c06-136">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="91c06-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="91c06-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91c06-137">-Confirm</span></span>
<span data-ttu-id="91c06-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91c06-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91c06-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91c06-139">-WhatIf</span></span>
<span data-ttu-id="91c06-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91c06-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91c06-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91c06-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91c06-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c06-142">CommonParameters</span></span>
<span data-ttu-id="91c06-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91c06-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c06-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="91c06-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c06-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="91c06-145">INPUTS</span></span>

### <span data-ttu-id="91c06-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="91c06-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="91c06-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91c06-147">OUTPUTS</span></span>

### <span data-ttu-id="91c06-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="91c06-148">System.Boolean</span></span>

## <span data-ttu-id="91c06-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="91c06-149">NOTES</span></span>

<span data-ttu-id="91c06-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="91c06-150">ALIASES</span></span>

<span data-ttu-id="91c06-151">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="91c06-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="91c06-152">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="91c06-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="91c06-153">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="91c06-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="91c06-154">INPUTOBJECT <ISpringCloudIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="91c06-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="91c06-155">`[AppName <String>]`: nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="91c06-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="91c06-156">`[BindingName <String>]`: nome della risorsa di associazione.</span><span class="sxs-lookup"><span data-stu-id="91c06-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="91c06-157">`[CertificateName <String>]`: nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="91c06-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="91c06-158">`[DeploymentName <String>]`: nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="91c06-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="91c06-159">`[DomainName <String>]`: nome della risorsa di dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="91c06-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="91c06-160">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="91c06-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="91c06-161">`[Location <String>]`: l'area geografica</span><span class="sxs-lookup"><span data-stu-id="91c06-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="91c06-162">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="91c06-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="91c06-163">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="91c06-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="91c06-164">`[ServiceName <String>]`: nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="91c06-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="91c06-165">`[SubscriptionId <String>]`: recupera l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="91c06-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="91c06-166">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="91c06-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="91c06-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91c06-167">RELATED LINKS</span></span>

