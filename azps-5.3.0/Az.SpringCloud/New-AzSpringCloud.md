---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: d5b8d521c72b553143f75b0911cb9b933b0795e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476687"
---
# <span data-ttu-id="e53e3-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="e53e3-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="e53e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e53e3-102">SYNOPSIS</span></span>
<span data-ttu-id="e53e3-103">Creare un nuovo servizio o aggiornare un servizio in uscita.</span><span class="sxs-lookup"><span data-stu-id="e53e3-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="e53e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e53e3-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e53e3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e53e3-105">DESCRIPTION</span></span>
<span data-ttu-id="e53e3-106">Creare un nuovo servizio o aggiornare un servizio in uscita.</span><span class="sxs-lookup"><span data-stu-id="e53e3-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="e53e3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e53e3-107">EXAMPLES</span></span>

### <span data-ttu-id="e53e3-108">Esempio 1: creare un servizio cloud primaverile.</span><span class="sxs-lookup"><span data-stu-id="e53e3-108">Example 1: Create a spring cloud service.</span></span>
```powershell
PS C:\> New-AzSpringCloud -ResourceGroupName spring-cloud-rp -name spring-cloud-service -Location eastus

ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="e53e3-109">Creare un servizio cloud primaverile.</span><span class="sxs-lookup"><span data-stu-id="e53e3-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="e53e3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e53e3-110">PARAMETERS</span></span>

### <span data-ttu-id="e53e3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e53e3-111">-AsJob</span></span>
<span data-ttu-id="e53e3-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="e53e3-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e53e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e53e3-113">-DefaultProfile</span></span>
<span data-ttu-id="e53e3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e53e3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e53e3-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="e53e3-115">-GitPropertyUri</span></span>
<span data-ttu-id="e53e3-116">URI del repository</span><span class="sxs-lookup"><span data-stu-id="e53e3-116">URI of the repository</span></span>

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

### <span data-ttu-id="e53e3-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e53e3-117">-Location</span></span>
<span data-ttu-id="e53e3-118">Posizione GEO della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e53e3-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="e53e3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e53e3-119">-Name</span></span>
<span data-ttu-id="e53e3-120">Nome della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="e53e3-120">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e53e3-121">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="e53e3-121">-NoWait</span></span>
<span data-ttu-id="e53e3-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="e53e3-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e53e3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e53e3-123">-ResourceGroupName</span></span>
<span data-ttu-id="e53e3-124">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e53e3-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e53e3-125">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="e53e3-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e53e3-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e53e3-126">-SkuName</span></span>
<span data-ttu-id="e53e3-127">Nome dell'USK</span><span class="sxs-lookup"><span data-stu-id="e53e3-127">Name of the Sku</span></span>

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

### <span data-ttu-id="e53e3-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e53e3-128">-SkuTier</span></span>
<span data-ttu-id="e53e3-129">Livello dell'USK</span><span class="sxs-lookup"><span data-stu-id="e53e3-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="e53e3-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e53e3-130">-SubscriptionId</span></span>
<span data-ttu-id="e53e3-131">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e53e3-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e53e3-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e53e3-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e53e3-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="e53e3-133">-Tag</span></span>
<span data-ttu-id="e53e3-134">Tag del servizio che è un elenco di coppie di valori chiave che descrivono la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e53e3-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e53e3-135">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="e53e3-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="e53e3-136">Chiave di strumentazione Insight Application di destinazione</span><span class="sxs-lookup"><span data-stu-id="e53e3-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="e53e3-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="e53e3-137">-TraceEnabled</span></span>
<span data-ttu-id="e53e3-138">Indica se abilitare la funzionalità di traccia</span><span class="sxs-lookup"><span data-stu-id="e53e3-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="e53e3-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e53e3-139">-Confirm</span></span>
<span data-ttu-id="e53e3-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e53e3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e53e3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e53e3-141">-WhatIf</span></span>
<span data-ttu-id="e53e3-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e53e3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e53e3-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e53e3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e53e3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e53e3-144">CommonParameters</span></span>
<span data-ttu-id="e53e3-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e53e3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e53e3-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e53e3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e53e3-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e53e3-147">INPUTS</span></span>

## <span data-ttu-id="e53e3-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e53e3-148">OUTPUTS</span></span>

### <span data-ttu-id="e53e3-149">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20200701. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="e53e3-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="e53e3-150">Note</span><span class="sxs-lookup"><span data-stu-id="e53e3-150">NOTES</span></span>

<span data-ttu-id="e53e3-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e53e3-151">ALIASES</span></span>

## <span data-ttu-id="e53e3-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e53e3-152">RELATED LINKS</span></span>

