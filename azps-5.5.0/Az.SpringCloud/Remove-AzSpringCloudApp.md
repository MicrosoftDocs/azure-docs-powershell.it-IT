---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: e363a7bedc891c736f06b60c093483010e6b261d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201550"
---
# <span data-ttu-id="2e149-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="2e149-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="2e149-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e149-102">SYNOPSIS</span></span>
<span data-ttu-id="2e149-103">Operazione per l'eliminazione di un'app.</span><span class="sxs-lookup"><span data-stu-id="2e149-103">Operation to delete an App.</span></span>

## <span data-ttu-id="2e149-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e149-104">SYNTAX</span></span>

### <span data-ttu-id="2e149-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2e149-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2e149-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2e149-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2e149-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2e149-107">DESCRIPTION</span></span>
<span data-ttu-id="2e149-108">Operazione per l'eliminazione di un'app.</span><span class="sxs-lookup"><span data-stu-id="2e149-108">Operation to delete an App.</span></span>

## <span data-ttu-id="2e149-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e149-109">EXAMPLES</span></span>

### <span data-ttu-id="2e149-110">Esempio 1: Rimuovere l'app Spring Cloud in base al nome.</span><span class="sxs-lookup"><span data-stu-id="2e149-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="2e149-111">Rimuovi l'app Spring Cloud in base al nome.</span><span class="sxs-lookup"><span data-stu-id="2e149-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="2e149-112">Esempio 2: Rimuovere l'app Spring Cloud dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="2e149-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="2e149-113">Rimuovi l'app Cloud Spring dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="2e149-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="2e149-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e149-114">PARAMETERS</span></span>

### <span data-ttu-id="2e149-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e149-115">-AsJob</span></span>
<span data-ttu-id="2e149-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="2e149-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2e149-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e149-117">-DefaultProfile</span></span>
<span data-ttu-id="2e149-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e149-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e149-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e149-119">-InputObject</span></span>
<span data-ttu-id="2e149-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2e149-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2e149-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2e149-121">-Name</span></span>
<span data-ttu-id="2e149-122">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="2e149-122">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e149-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2e149-123">-NoWait</span></span>
<span data-ttu-id="2e149-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="2e149-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2e149-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e149-125">-PassThru</span></span>
<span data-ttu-id="2e149-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="2e149-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2e149-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e149-127">-ResourceGroupName</span></span>
<span data-ttu-id="2e149-128">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2e149-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2e149-129">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="2e149-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2e149-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2e149-130">-ServiceName</span></span>
<span data-ttu-id="2e149-131">Nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="2e149-131">The name of the Service resource.</span></span>

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

### <span data-ttu-id="2e149-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e149-132">-SubscriptionId</span></span>
<span data-ttu-id="2e149-133">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2e149-133">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2e149-134">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2e149-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2e149-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e149-135">-Confirm</span></span>
<span data-ttu-id="2e149-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e149-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e149-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e149-137">-WhatIf</span></span>
<span data-ttu-id="2e149-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e149-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e149-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e149-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e149-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e149-140">CommonParameters</span></span>
<span data-ttu-id="2e149-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e149-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e149-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2e149-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e149-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="2e149-143">INPUTS</span></span>

### <span data-ttu-id="2e149-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="2e149-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="2e149-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e149-145">OUTPUTS</span></span>

### <span data-ttu-id="2e149-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e149-146">System.Boolean</span></span>

## <span data-ttu-id="2e149-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="2e149-147">NOTES</span></span>

<span data-ttu-id="2e149-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2e149-148">ALIASES</span></span>

<span data-ttu-id="2e149-149">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="2e149-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2e149-150">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2e149-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2e149-151">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2e149-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2e149-152">INPUTOBJECT <ISpringCloudIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="2e149-152">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2e149-153">`[AppName <String>]`: nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="2e149-153">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="2e149-154">`[BindingName <String>]`: nome della risorsa di associazione.</span><span class="sxs-lookup"><span data-stu-id="2e149-154">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="2e149-155">`[CertificateName <String>]`: nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="2e149-155">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="2e149-156">`[DeploymentName <String>]`: nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2e149-156">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="2e149-157">`[DomainName <String>]`: nome della risorsa di dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2e149-157">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="2e149-158">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="2e149-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2e149-159">`[Location <String>]`: l'area geografica</span><span class="sxs-lookup"><span data-stu-id="2e149-159">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="2e149-160">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2e149-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="2e149-161">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="2e149-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="2e149-162">`[ServiceName <String>]`: nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="2e149-162">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="2e149-163">`[SubscriptionId <String>]`: recupera l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2e149-163">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="2e149-164">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2e149-164">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2e149-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e149-165">RELATED LINKS</span></span>

