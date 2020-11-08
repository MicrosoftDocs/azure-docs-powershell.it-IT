---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/restart-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Restart-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Restart-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 859ea1febad82dbb09e88debe3f825feab18b1c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193180"
---
# <span data-ttu-id="fc673-101">Restart-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="fc673-101">Restart-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="fc673-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc673-102">SYNOPSIS</span></span>
<span data-ttu-id="fc673-103">Riavviare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="fc673-103">Restart the deployment.</span></span>

## <span data-ttu-id="fc673-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc673-104">SYNTAX</span></span>

### <span data-ttu-id="fc673-105">Restart (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fc673-105">Restart (Default)</span></span>
```
Restart-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fc673-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fc673-106">RestartViaIdentity</span></span>
```
Restart-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fc673-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc673-107">DESCRIPTION</span></span>
<span data-ttu-id="fc673-108">Riavviare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="fc673-108">Restart the deployment.</span></span>

## <span data-ttu-id="fc673-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc673-109">EXAMPLES</span></span>

### <span data-ttu-id="fc673-110">Esempio 1: riavviare il servizio cloud primaverile in base al nome.</span><span class="sxs-lookup"><span data-stu-id="fc673-110">Example 1: Restart Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Restart-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="fc673-111">Riavviare il servizio cloud primaverile per nome.</span><span class="sxs-lookup"><span data-stu-id="fc673-111">Restart Spring Cloud Service by name.</span></span>

### <span data-ttu-id="fc673-112">Esempio 2: riavviare il servizio cloud primaverile da pipe.</span><span class="sxs-lookup"><span data-stu-id="fc673-112">Example 2: Restart Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Restart-AzSpringCloud
```

<span data-ttu-id="fc673-113">Riavviare il servizio cloud primaverile da pipe.</span><span class="sxs-lookup"><span data-stu-id="fc673-113">Restart Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="fc673-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc673-114">PARAMETERS</span></span>

### <span data-ttu-id="fc673-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="fc673-115">-AppName</span></span>
<span data-ttu-id="fc673-116">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="fc673-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc673-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc673-117">-AsJob</span></span>
<span data-ttu-id="fc673-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="fc673-118">Run the command as a job</span></span>

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

### <span data-ttu-id="fc673-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc673-119">-DefaultProfile</span></span>
<span data-ttu-id="fc673-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc673-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc673-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc673-121">-InputObject</span></span>
<span data-ttu-id="fc673-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="fc673-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc673-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc673-123">-Name</span></span>
<span data-ttu-id="fc673-124">Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="fc673-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc673-125">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="fc673-125">-NoWait</span></span>
<span data-ttu-id="fc673-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="fc673-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fc673-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc673-127">-PassThru</span></span>
<span data-ttu-id="fc673-128">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="fc673-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fc673-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc673-129">-ResourceGroupName</span></span>
<span data-ttu-id="fc673-130">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc673-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fc673-131">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="fc673-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc673-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fc673-132">-ServiceName</span></span>
<span data-ttu-id="fc673-133">Nome della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="fc673-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc673-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc673-134">-SubscriptionId</span></span>
<span data-ttu-id="fc673-135">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fc673-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fc673-136">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="fc673-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc673-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fc673-137">-Confirm</span></span>
<span data-ttu-id="fc673-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc673-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc673-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc673-139">-WhatIf</span></span>
<span data-ttu-id="fc673-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc673-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc673-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc673-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc673-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc673-142">CommonParameters</span></span>
<span data-ttu-id="fc673-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc673-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc673-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc673-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc673-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc673-145">INPUTS</span></span>

### <span data-ttu-id="fc673-146">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="fc673-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="fc673-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc673-147">OUTPUTS</span></span>

### <span data-ttu-id="fc673-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc673-148">System.Boolean</span></span>

## <span data-ttu-id="fc673-149">Note</span><span class="sxs-lookup"><span data-stu-id="fc673-149">NOTES</span></span>

<span data-ttu-id="fc673-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fc673-150">ALIASES</span></span>

<span data-ttu-id="fc673-151">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc673-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fc673-152">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="fc673-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fc673-153">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fc673-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fc673-154">INPUTOBJECT <ISpringCloudIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="fc673-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fc673-155">`[AppName <String>]`: Il nome della risorsa app.</span><span class="sxs-lookup"><span data-stu-id="fc673-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="fc673-156">`[BindingName <String>]`: Nome della risorsa di binding.</span><span class="sxs-lookup"><span data-stu-id="fc673-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="fc673-157">`[CertificateName <String>]`: Il nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="fc673-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="fc673-158">`[DeploymentName <String>]`: Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="fc673-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="fc673-159">`[DomainName <String>]`: Nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="fc673-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="fc673-160">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="fc673-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fc673-161">`[Location <String>]`: area geografica</span><span class="sxs-lookup"><span data-stu-id="fc673-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="fc673-162">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc673-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="fc673-163">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="fc673-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="fc673-164">`[ServiceName <String>]`: Nome della risorsa servizio.</span><span class="sxs-lookup"><span data-stu-id="fc673-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="fc673-165">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fc673-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="fc673-166">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="fc673-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="fc673-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc673-167">RELATED LINKS</span></span>
