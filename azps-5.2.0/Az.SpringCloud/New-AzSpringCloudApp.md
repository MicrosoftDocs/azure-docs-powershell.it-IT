---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
ms.openlocfilehash: c8f723a66ee388244f2aab9ab556ea315f44e72c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341764"
---
# <span data-ttu-id="c4184-101">New-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="c4184-101">New-AzSpringCloudApp</span></span>

## <span data-ttu-id="c4184-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4184-102">SYNOPSIS</span></span>
<span data-ttu-id="c4184-103">Creare una nuova app o aggiornare un'app in uscita.</span><span class="sxs-lookup"><span data-stu-id="c4184-103">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="c4184-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4184-104">SYNTAX</span></span>

```
New-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c4184-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4184-105">DESCRIPTION</span></span>
<span data-ttu-id="c4184-106">Creare una nuova app o aggiornare un'app in uscita.</span><span class="sxs-lookup"><span data-stu-id="c4184-106">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="c4184-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4184-107">EXAMPLES</span></span>

### <span data-ttu-id="c4184-108">Esempio 1: creare un'app Cloud primaverile.</span><span class="sxs-lookup"><span data-stu-id="c4184-108">Example 1: Create a spring cloud app.</span></span>
```powershell
PS C:\> New-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
ActiveDeploymentName    :
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="c4184-109">Creare un'app Cloud primaverile.</span><span class="sxs-lookup"><span data-stu-id="c4184-109">Create a spring cloud app.</span></span>

## <span data-ttu-id="c4184-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4184-110">PARAMETERS</span></span>

### <span data-ttu-id="c4184-111">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="c4184-111">-ActiveDeploymentName</span></span>
<span data-ttu-id="c4184-112">Nome della distribuzione attiva dell'app</span><span class="sxs-lookup"><span data-stu-id="c4184-112">Name of the active deployment of the App</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4184-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4184-113">-AsJob</span></span>
<span data-ttu-id="c4184-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="c4184-114">Run the command as a job</span></span>

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

### <span data-ttu-id="c4184-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4184-115">-DefaultProfile</span></span>
<span data-ttu-id="c4184-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4184-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4184-117">-FQDN</span><span class="sxs-lookup"><span data-stu-id="c4184-117">-Fqdn</span></span>
<span data-ttu-id="c4184-118">Nome DNS completo.</span><span class="sxs-lookup"><span data-stu-id="c4184-118">Fully qualified dns Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4184-119">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c4184-119">-HttpsOnly</span></span>
<span data-ttu-id="c4184-120">Indica se è consentito solo HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c4184-120">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="c4184-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c4184-121">-Location</span></span>
<span data-ttu-id="c4184-122">La posizione GEO dell'applicazione, sempre la stessa con la relativa risorsa padre</span><span class="sxs-lookup"><span data-stu-id="c4184-122">The GEO location of the application, always the same with its parent resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4184-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4184-123">-Name</span></span>
<span data-ttu-id="c4184-124">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="c4184-124">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4184-125">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="c4184-125">-NoWait</span></span>
<span data-ttu-id="c4184-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="c4184-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c4184-127">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="c4184-127">-PersistentDiskMountPath</span></span>
<span data-ttu-id="c4184-128">Montare il percorso del disco persistente</span><span class="sxs-lookup"><span data-stu-id="c4184-128">Mount path of the persistent disk</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4184-129">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="c4184-129">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="c4184-130">Dimensioni del disco persistente in GB</span><span class="sxs-lookup"><span data-stu-id="c4184-130">Size of the persistent disk in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4184-131">-Pubblico</span><span class="sxs-lookup"><span data-stu-id="c4184-131">-Public</span></span>
<span data-ttu-id="c4184-132">Indica se l'app espone endpoint pubblico</span><span class="sxs-lookup"><span data-stu-id="c4184-132">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="c4184-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4184-133">-ResourceGroupName</span></span>
<span data-ttu-id="c4184-134">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c4184-134">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c4184-135">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="c4184-135">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4184-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c4184-136">-ServiceName</span></span>
<span data-ttu-id="c4184-137">Nome della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="c4184-137">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4184-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4184-138">-SubscriptionId</span></span>
<span data-ttu-id="c4184-139">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c4184-139">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c4184-140">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c4184-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4184-141">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="c4184-141">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="c4184-142">Montare il percorso del disco temporaneo</span><span class="sxs-lookup"><span data-stu-id="c4184-142">Mount path of the temporary disk</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4184-143">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="c4184-143">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="c4184-144">Dimensioni del disco temporaneo in GB</span><span class="sxs-lookup"><span data-stu-id="c4184-144">Size of the temporary disk in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4184-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c4184-145">-Confirm</span></span>
<span data-ttu-id="c4184-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4184-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4184-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4184-147">-WhatIf</span></span>
<span data-ttu-id="c4184-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4184-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4184-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4184-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4184-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4184-150">CommonParameters</span></span>
<span data-ttu-id="c4184-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4184-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4184-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4184-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4184-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4184-153">INPUTS</span></span>

## <span data-ttu-id="c4184-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4184-154">OUTPUTS</span></span>

### <span data-ttu-id="c4184-155">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20200701. IAppResource</span><span class="sxs-lookup"><span data-stu-id="c4184-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="c4184-156">Note</span><span class="sxs-lookup"><span data-stu-id="c4184-156">NOTES</span></span>

<span data-ttu-id="c4184-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c4184-157">ALIASES</span></span>

## <span data-ttu-id="c4184-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4184-158">RELATED LINKS</span></span>

