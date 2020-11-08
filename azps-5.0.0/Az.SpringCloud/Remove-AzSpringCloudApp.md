---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: e363a7bedc891c736f06b60c093483010e6b261d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193185"
---
# <span data-ttu-id="ad9d6-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="ad9d6-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="ad9d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad9d6-102">SYNOPSIS</span></span>
<span data-ttu-id="ad9d6-103">Operazione per eliminare un'app.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-103">Operation to delete an App.</span></span>

## <span data-ttu-id="ad9d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad9d6-104">SYNTAX</span></span>

### <span data-ttu-id="ad9d6-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad9d6-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ad9d6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ad9d6-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ad9d6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad9d6-107">DESCRIPTION</span></span>
<span data-ttu-id="ad9d6-108">Operazione per eliminare un'app.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-108">Operation to delete an App.</span></span>

## <span data-ttu-id="ad9d6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad9d6-109">EXAMPLES</span></span>

### <span data-ttu-id="ad9d6-110">Esempio 1: rimuovere l'app Spring cloud per nome.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="ad9d6-111">Rimuovere l'app Spring cloud per nome.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="ad9d6-112">Esempio 2: rimuovere l'app Spring cloud da pipe.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="ad9d6-113">Rimuovi l'app Spring cloud da pipe.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="ad9d6-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad9d6-114">PARAMETERS</span></span>

### <span data-ttu-id="ad9d6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad9d6-115">-AsJob</span></span>
<span data-ttu-id="ad9d6-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="ad9d6-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ad9d6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad9d6-117">-DefaultProfile</span></span>
<span data-ttu-id="ad9d6-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad9d6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad9d6-119">-InputObject</span></span>
<span data-ttu-id="ad9d6-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ad9d6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad9d6-121">-Name</span></span>
<span data-ttu-id="ad9d6-122">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-122">The name of the App resource.</span></span>

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

### <span data-ttu-id="ad9d6-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="ad9d6-123">-NoWait</span></span>
<span data-ttu-id="ad9d6-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="ad9d6-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ad9d6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad9d6-125">-PassThru</span></span>
<span data-ttu-id="ad9d6-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="ad9d6-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ad9d6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad9d6-127">-ResourceGroupName</span></span>
<span data-ttu-id="ad9d6-128">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ad9d6-129">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ad9d6-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ad9d6-130">-ServiceName</span></span>
<span data-ttu-id="ad9d6-131">Nome della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-131">The name of the Service resource.</span></span>

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

### <span data-ttu-id="ad9d6-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad9d6-132">-SubscriptionId</span></span>
<span data-ttu-id="ad9d6-133">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-133">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ad9d6-134">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ad9d6-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ad9d6-135">-Confirm</span></span>
<span data-ttu-id="ad9d6-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad9d6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad9d6-137">-WhatIf</span></span>
<span data-ttu-id="ad9d6-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad9d6-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad9d6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad9d6-140">CommonParameters</span></span>
<span data-ttu-id="ad9d6-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad9d6-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad9d6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad9d6-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad9d6-143">INPUTS</span></span>

### <span data-ttu-id="ad9d6-144">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="ad9d6-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="ad9d6-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad9d6-145">OUTPUTS</span></span>

### <span data-ttu-id="ad9d6-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad9d6-146">System.Boolean</span></span>

## <span data-ttu-id="ad9d6-147">Note</span><span class="sxs-lookup"><span data-stu-id="ad9d6-147">NOTES</span></span>

<span data-ttu-id="ad9d6-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ad9d6-148">ALIASES</span></span>

<span data-ttu-id="ad9d6-149">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad9d6-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ad9d6-150">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ad9d6-151">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ad9d6-152">INPUTOBJECT <ISpringCloudIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ad9d6-152">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ad9d6-153">`[AppName <String>]`: Il nome della risorsa app.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-153">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="ad9d6-154">`[BindingName <String>]`: Nome della risorsa di binding.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-154">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="ad9d6-155">`[CertificateName <String>]`: Il nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-155">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="ad9d6-156">`[DeploymentName <String>]`: Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-156">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="ad9d6-157">`[DomainName <String>]`: Nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-157">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="ad9d6-158">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="ad9d6-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ad9d6-159">`[Location <String>]`: area geografica</span><span class="sxs-lookup"><span data-stu-id="ad9d6-159">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="ad9d6-160">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ad9d6-161">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ad9d6-162">`[ServiceName <String>]`: Nome della risorsa servizio.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-162">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="ad9d6-163">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-163">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="ad9d6-164">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ad9d6-164">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ad9d6-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad9d6-165">RELATED LINKS</span></span>

