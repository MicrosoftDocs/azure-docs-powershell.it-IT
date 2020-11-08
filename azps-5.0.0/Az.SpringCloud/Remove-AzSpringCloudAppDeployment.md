---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 25b7b5c93f769982364a0df8f14f5fbe2f804fa2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193184"
---
# <span data-ttu-id="2311a-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="2311a-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="2311a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2311a-102">SYNOPSIS</span></span>
<span data-ttu-id="2311a-103">Operazione per eliminare una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2311a-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="2311a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2311a-104">SYNTAX</span></span>

### <span data-ttu-id="2311a-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2311a-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2311a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2311a-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2311a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2311a-107">DESCRIPTION</span></span>
<span data-ttu-id="2311a-108">Operazione per eliminare una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2311a-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="2311a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2311a-109">EXAMPLES</span></span>

### <span data-ttu-id="2311a-110">Esempio 1: rimuovere la distribuzione del cloud Spring per nome.</span><span class="sxs-lookup"><span data-stu-id="2311a-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="2311a-111">Rimuovere la distribuzione del cloud Spring per nome.</span><span class="sxs-lookup"><span data-stu-id="2311a-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="2311a-112">Esempio 2: rimuovere la distribuzione del cloud Spring da pipe.</span><span class="sxs-lookup"><span data-stu-id="2311a-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="2311a-113">Rimuovere la distribuzione del cloud Spring da pipe.</span><span class="sxs-lookup"><span data-stu-id="2311a-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="2311a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2311a-114">PARAMETERS</span></span>

### <span data-ttu-id="2311a-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="2311a-115">-AppName</span></span>
<span data-ttu-id="2311a-116">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="2311a-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="2311a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2311a-117">-AsJob</span></span>
<span data-ttu-id="2311a-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="2311a-118">Run the command as a job</span></span>

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

### <span data-ttu-id="2311a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2311a-119">-DefaultProfile</span></span>
<span data-ttu-id="2311a-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2311a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2311a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2311a-121">-InputObject</span></span>
<span data-ttu-id="2311a-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2311a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2311a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2311a-123">-Name</span></span>
<span data-ttu-id="2311a-124">Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2311a-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="2311a-125">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="2311a-125">-NoWait</span></span>
<span data-ttu-id="2311a-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="2311a-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2311a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2311a-127">-PassThru</span></span>
<span data-ttu-id="2311a-128">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="2311a-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2311a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2311a-129">-ResourceGroupName</span></span>
<span data-ttu-id="2311a-130">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2311a-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2311a-131">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="2311a-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2311a-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2311a-132">-ServiceName</span></span>
<span data-ttu-id="2311a-133">Nome della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="2311a-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="2311a-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2311a-134">-SubscriptionId</span></span>
<span data-ttu-id="2311a-135">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2311a-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2311a-136">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2311a-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2311a-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2311a-137">-Confirm</span></span>
<span data-ttu-id="2311a-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2311a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2311a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2311a-139">-WhatIf</span></span>
<span data-ttu-id="2311a-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2311a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2311a-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2311a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2311a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2311a-142">CommonParameters</span></span>
<span data-ttu-id="2311a-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2311a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2311a-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2311a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2311a-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2311a-145">INPUTS</span></span>

### <span data-ttu-id="2311a-146">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="2311a-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="2311a-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2311a-147">OUTPUTS</span></span>

### <span data-ttu-id="2311a-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2311a-148">System.Boolean</span></span>

## <span data-ttu-id="2311a-149">Note</span><span class="sxs-lookup"><span data-stu-id="2311a-149">NOTES</span></span>

<span data-ttu-id="2311a-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2311a-150">ALIASES</span></span>

<span data-ttu-id="2311a-151">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2311a-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2311a-152">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2311a-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2311a-153">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2311a-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2311a-154">INPUTOBJECT <ISpringCloudIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="2311a-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2311a-155">`[AppName <String>]`: Il nome della risorsa app.</span><span class="sxs-lookup"><span data-stu-id="2311a-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="2311a-156">`[BindingName <String>]`: Nome della risorsa di binding.</span><span class="sxs-lookup"><span data-stu-id="2311a-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="2311a-157">`[CertificateName <String>]`: Il nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="2311a-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="2311a-158">`[DeploymentName <String>]`: Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2311a-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="2311a-159">`[DomainName <String>]`: Nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2311a-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="2311a-160">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="2311a-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2311a-161">`[Location <String>]`: area geografica</span><span class="sxs-lookup"><span data-stu-id="2311a-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="2311a-162">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2311a-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="2311a-163">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="2311a-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="2311a-164">`[ServiceName <String>]`: Nome della risorsa servizio.</span><span class="sxs-lookup"><span data-stu-id="2311a-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="2311a-165">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2311a-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="2311a-166">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2311a-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2311a-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2311a-167">RELATED LINKS</span></span>

