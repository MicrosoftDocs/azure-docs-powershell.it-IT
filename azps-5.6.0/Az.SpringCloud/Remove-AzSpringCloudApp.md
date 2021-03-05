---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: c6dccbaa5e398d5d00b02a28cc8942b9e5264859
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977758"
---
# <span data-ttu-id="b1fee-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="b1fee-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="b1fee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1fee-102">SYNOPSIS</span></span>
<span data-ttu-id="b1fee-103">Operazione per l'eliminazione di un'app.</span><span class="sxs-lookup"><span data-stu-id="b1fee-103">Operation to delete an App.</span></span>

## <span data-ttu-id="b1fee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1fee-104">SYNTAX</span></span>

### <span data-ttu-id="b1fee-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1fee-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b1fee-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b1fee-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b1fee-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b1fee-107">DESCRIPTION</span></span>
<span data-ttu-id="b1fee-108">Operazione per l'eliminazione di un'app.</span><span class="sxs-lookup"><span data-stu-id="b1fee-108">Operation to delete an App.</span></span>

## <span data-ttu-id="b1fee-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1fee-109">EXAMPLES</span></span>

### <span data-ttu-id="b1fee-110">Esempio 1: Rimuovere l'app Spring Cloud in base al nome.</span><span class="sxs-lookup"><span data-stu-id="b1fee-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="b1fee-111">Rimuovi l'app Spring Cloud in base al nome.</span><span class="sxs-lookup"><span data-stu-id="b1fee-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="b1fee-112">Esempio 2: Rimuovere l'app Spring Cloud dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="b1fee-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="b1fee-113">Rimuovi l'app Cloud Spring dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="b1fee-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="b1fee-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1fee-114">PARAMETERS</span></span>

### <span data-ttu-id="b1fee-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1fee-115">-AsJob</span></span>
<span data-ttu-id="b1fee-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="b1fee-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b1fee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1fee-117">-DefaultProfile</span></span>
<span data-ttu-id="b1fee-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1fee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1fee-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1fee-119">-InputObject</span></span>
<span data-ttu-id="b1fee-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b1fee-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b1fee-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b1fee-121">-Name</span></span>
<span data-ttu-id="b1fee-122">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="b1fee-122">The name of the App resource.</span></span>

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

### <span data-ttu-id="b1fee-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b1fee-123">-NoWait</span></span>
<span data-ttu-id="b1fee-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="b1fee-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b1fee-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1fee-125">-PassThru</span></span>
<span data-ttu-id="b1fee-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="b1fee-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b1fee-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1fee-127">-ResourceGroupName</span></span>
<span data-ttu-id="b1fee-128">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b1fee-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b1fee-129">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="b1fee-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b1fee-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b1fee-130">-ServiceName</span></span>
<span data-ttu-id="b1fee-131">Nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="b1fee-131">The name of the Service resource.</span></span>

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

### <span data-ttu-id="b1fee-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1fee-132">-SubscriptionId</span></span>
<span data-ttu-id="b1fee-133">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b1fee-133">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b1fee-134">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b1fee-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b1fee-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1fee-135">-Confirm</span></span>
<span data-ttu-id="b1fee-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1fee-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1fee-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1fee-137">-WhatIf</span></span>
<span data-ttu-id="b1fee-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1fee-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1fee-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1fee-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1fee-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1fee-140">CommonParameters</span></span>
<span data-ttu-id="b1fee-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1fee-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1fee-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1fee-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1fee-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="b1fee-143">INPUTS</span></span>

### <span data-ttu-id="b1fee-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="b1fee-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="b1fee-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1fee-145">OUTPUTS</span></span>

### <span data-ttu-id="b1fee-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b1fee-146">System.Boolean</span></span>

## <span data-ttu-id="b1fee-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="b1fee-147">NOTES</span></span>

<span data-ttu-id="b1fee-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b1fee-148">ALIASES</span></span>

<span data-ttu-id="b1fee-149">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b1fee-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b1fee-150">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b1fee-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1fee-151">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b1fee-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b1fee-152">INPUTOBJECT <ISpringCloudIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b1fee-152">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b1fee-153">`[AppName <String>]`: nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="b1fee-153">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="b1fee-154">`[BindingName <String>]`: nome della risorsa di associazione.</span><span class="sxs-lookup"><span data-stu-id="b1fee-154">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="b1fee-155">`[CertificateName <String>]`: nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="b1fee-155">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="b1fee-156">`[DeploymentName <String>]`: nome della risorsa distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b1fee-156">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="b1fee-157">`[DomainName <String>]`: nome della risorsa di dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="b1fee-157">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="b1fee-158">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b1fee-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b1fee-159">`[Location <String>]`: l'area geografica</span><span class="sxs-lookup"><span data-stu-id="b1fee-159">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="b1fee-160">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b1fee-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b1fee-161">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="b1fee-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b1fee-162">`[ServiceName <String>]`: nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="b1fee-162">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="b1fee-163">`[SubscriptionId <String>]`: recupera l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b1fee-163">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="b1fee-164">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b1fee-164">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b1fee-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1fee-165">RELATED LINKS</span></span>

