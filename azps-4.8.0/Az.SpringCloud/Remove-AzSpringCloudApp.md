---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: ace761bfd329c756baa27d1bff6300f2e030f377
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191886"
---
# <span data-ttu-id="39875-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="39875-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="39875-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39875-102">SYNOPSIS</span></span>
<span data-ttu-id="39875-103">Operazione per eliminare un'app.</span><span class="sxs-lookup"><span data-stu-id="39875-103">Operation to delete an App.</span></span>

## <span data-ttu-id="39875-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39875-104">SYNTAX</span></span>

### <span data-ttu-id="39875-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39875-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="39875-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="39875-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="39875-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39875-107">DESCRIPTION</span></span>
<span data-ttu-id="39875-108">Operazione per eliminare un'app.</span><span class="sxs-lookup"><span data-stu-id="39875-108">Operation to delete an App.</span></span>

## <span data-ttu-id="39875-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39875-109">EXAMPLES</span></span>

### <span data-ttu-id="39875-110">Esempio 1: rimuovere l'app Spring cloud per nome.</span><span class="sxs-lookup"><span data-stu-id="39875-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="39875-111">Rimuovere l'app Spring cloud per nome.</span><span class="sxs-lookup"><span data-stu-id="39875-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="39875-112">Esempio 2: rimuovere l'app Spring cloud da pipe.</span><span class="sxs-lookup"><span data-stu-id="39875-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="39875-113">Rimuovi l'app Spring cloud da pipe.</span><span class="sxs-lookup"><span data-stu-id="39875-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="39875-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39875-114">PARAMETERS</span></span>

### <span data-ttu-id="39875-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39875-115">-DefaultProfile</span></span>
<span data-ttu-id="39875-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39875-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39875-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39875-117">-InputObject</span></span>
<span data-ttu-id="39875-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="39875-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="39875-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="39875-119">-Name</span></span>
<span data-ttu-id="39875-120">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="39875-120">The name of the App resource.</span></span>

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

### <span data-ttu-id="39875-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39875-121">-PassThru</span></span>
<span data-ttu-id="39875-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="39875-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="39875-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39875-123">-ResourceGroupName</span></span>
<span data-ttu-id="39875-124">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="39875-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="39875-125">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="39875-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="39875-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="39875-126">-ServiceName</span></span>
<span data-ttu-id="39875-127">Nome della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="39875-127">The name of the Service resource.</span></span>

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

### <span data-ttu-id="39875-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39875-128">-SubscriptionId</span></span>
<span data-ttu-id="39875-129">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="39875-129">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="39875-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="39875-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="39875-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="39875-131">-Confirm</span></span>
<span data-ttu-id="39875-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39875-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39875-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39875-133">-WhatIf</span></span>
<span data-ttu-id="39875-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39875-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39875-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39875-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39875-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39875-136">CommonParameters</span></span>
<span data-ttu-id="39875-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39875-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39875-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39875-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39875-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39875-139">INPUTS</span></span>

### <span data-ttu-id="39875-140">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="39875-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="39875-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39875-141">OUTPUTS</span></span>

### <span data-ttu-id="39875-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39875-142">System.Boolean</span></span>

## <span data-ttu-id="39875-143">Note</span><span class="sxs-lookup"><span data-stu-id="39875-143">NOTES</span></span>

<span data-ttu-id="39875-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="39875-144">ALIASES</span></span>

<span data-ttu-id="39875-145">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39875-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="39875-146">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="39875-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39875-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="39875-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="39875-148">INPUTOBJECT <ISpringCloudIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="39875-148">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="39875-149">`[AppName <String>]`: Il nome della risorsa app.</span><span class="sxs-lookup"><span data-stu-id="39875-149">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="39875-150">`[BindingName <String>]`: Nome della risorsa di binding.</span><span class="sxs-lookup"><span data-stu-id="39875-150">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="39875-151">`[CertificateName <String>]`: Il nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="39875-151">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="39875-152">`[DeploymentName <String>]`: Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="39875-152">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="39875-153">`[DomainName <String>]`: Nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="39875-153">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="39875-154">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="39875-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="39875-155">`[Location <String>]`: area geografica</span><span class="sxs-lookup"><span data-stu-id="39875-155">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="39875-156">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="39875-156">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="39875-157">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="39875-157">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="39875-158">`[ServiceName <String>]`: Nome della risorsa servizio.</span><span class="sxs-lookup"><span data-stu-id="39875-158">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="39875-159">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="39875-159">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="39875-160">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="39875-160">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="39875-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39875-161">RELATED LINKS</span></span>

