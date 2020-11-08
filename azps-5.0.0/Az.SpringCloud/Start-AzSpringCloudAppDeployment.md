---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/start-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 7cab91bf5c7e95258f17a73da4e2b177e30444c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193178"
---
# <span data-ttu-id="2950c-101">Start-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="2950c-101">Start-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="2950c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2950c-102">SYNOPSIS</span></span>
<span data-ttu-id="2950c-103">Avviare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2950c-103">Start the deployment.</span></span>

## <span data-ttu-id="2950c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2950c-104">SYNTAX</span></span>

### <span data-ttu-id="2950c-105">Inizio (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2950c-105">Start (Default)</span></span>
```
Start-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2950c-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2950c-106">StartViaIdentity</span></span>
```
Start-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2950c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2950c-107">DESCRIPTION</span></span>
<span data-ttu-id="2950c-108">Avviare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2950c-108">Start the deployment.</span></span>

## <span data-ttu-id="2950c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2950c-109">EXAMPLES</span></span>

### <span data-ttu-id="2950c-110">Esempio 1: avviare il servizio cloud primaverile in base al nome.</span><span class="sxs-lookup"><span data-stu-id="2950c-110">Example 1: Start Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Start-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="2950c-111">Avviare il servizio cloud primaverile in base al nome.</span><span class="sxs-lookup"><span data-stu-id="2950c-111">Start Spring Cloud Service by name.</span></span>

### <span data-ttu-id="2950c-112">Esempio 2: avviare il servizio cloud primaverile da pipe.</span><span class="sxs-lookup"><span data-stu-id="2950c-112">Example 2: Start Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Start-AzSpringCloud
```

<span data-ttu-id="2950c-113">Avviare il servizio cloud primaverile da pipe.</span><span class="sxs-lookup"><span data-stu-id="2950c-113">Start Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="2950c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2950c-114">PARAMETERS</span></span>

### <span data-ttu-id="2950c-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="2950c-115">-AppName</span></span>
<span data-ttu-id="2950c-116">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="2950c-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="2950c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2950c-117">-AsJob</span></span>
<span data-ttu-id="2950c-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="2950c-118">Run the command as a job</span></span>

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

### <span data-ttu-id="2950c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2950c-119">-DefaultProfile</span></span>
<span data-ttu-id="2950c-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2950c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2950c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2950c-121">-InputObject</span></span>
<span data-ttu-id="2950c-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2950c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2950c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2950c-123">-Name</span></span>
<span data-ttu-id="2950c-124">Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2950c-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="2950c-125">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="2950c-125">-NoWait</span></span>
<span data-ttu-id="2950c-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="2950c-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2950c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2950c-127">-PassThru</span></span>
<span data-ttu-id="2950c-128">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="2950c-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2950c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2950c-129">-ResourceGroupName</span></span>
<span data-ttu-id="2950c-130">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2950c-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2950c-131">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="2950c-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2950c-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2950c-132">-ServiceName</span></span>
<span data-ttu-id="2950c-133">Nome della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="2950c-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="2950c-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2950c-134">-SubscriptionId</span></span>
<span data-ttu-id="2950c-135">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2950c-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2950c-136">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2950c-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2950c-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2950c-137">-Confirm</span></span>
<span data-ttu-id="2950c-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2950c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2950c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2950c-139">-WhatIf</span></span>
<span data-ttu-id="2950c-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2950c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2950c-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2950c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2950c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2950c-142">CommonParameters</span></span>
<span data-ttu-id="2950c-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2950c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2950c-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2950c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2950c-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2950c-145">INPUTS</span></span>

### <span data-ttu-id="2950c-146">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="2950c-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="2950c-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2950c-147">OUTPUTS</span></span>

### <span data-ttu-id="2950c-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2950c-148">System.Boolean</span></span>

## <span data-ttu-id="2950c-149">Note</span><span class="sxs-lookup"><span data-stu-id="2950c-149">NOTES</span></span>

<span data-ttu-id="2950c-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2950c-150">ALIASES</span></span>

<span data-ttu-id="2950c-151">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2950c-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2950c-152">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2950c-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2950c-153">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2950c-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2950c-154">INPUTOBJECT <ISpringCloudIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="2950c-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2950c-155">`[AppName <String>]`: Il nome della risorsa app.</span><span class="sxs-lookup"><span data-stu-id="2950c-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="2950c-156">`[BindingName <String>]`: Nome della risorsa di binding.</span><span class="sxs-lookup"><span data-stu-id="2950c-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="2950c-157">`[CertificateName <String>]`: Il nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="2950c-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="2950c-158">`[DeploymentName <String>]`: Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2950c-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="2950c-159">`[DomainName <String>]`: Nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2950c-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="2950c-160">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="2950c-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2950c-161">`[Location <String>]`: area geografica</span><span class="sxs-lookup"><span data-stu-id="2950c-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="2950c-162">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2950c-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="2950c-163">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="2950c-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="2950c-164">`[ServiceName <String>]`: Nome della risorsa servizio.</span><span class="sxs-lookup"><span data-stu-id="2950c-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="2950c-165">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2950c-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="2950c-166">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2950c-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2950c-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2950c-167">RELATED LINKS</span></span>

