---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: a331e083075d7ed5fa3f148bc405226d85ddc960
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010254"
---
# <span data-ttu-id="8e418-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="8e418-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="8e418-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e418-102">SYNOPSIS</span></span>
<span data-ttu-id="8e418-103">Creare un nuovo servizio o aggiornare un servizio in uscita.</span><span class="sxs-lookup"><span data-stu-id="8e418-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="8e418-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e418-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8e418-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8e418-105">DESCRIPTION</span></span>
<span data-ttu-id="8e418-106">Creare un nuovo servizio o aggiornare un servizio in uscita.</span><span class="sxs-lookup"><span data-stu-id="8e418-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="8e418-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e418-107">EXAMPLES</span></span>

### <span data-ttu-id="8e418-108">Esempio 1: Creare un servizio cloud primaverile.</span><span class="sxs-lookup"><span data-stu-id="8e418-108">Example 1: Create a spring cloud service.</span></span>
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

<span data-ttu-id="8e418-109">Creare un servizio cloud primaverile.</span><span class="sxs-lookup"><span data-stu-id="8e418-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="8e418-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e418-110">PARAMETERS</span></span>

### <span data-ttu-id="8e418-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e418-111">-AsJob</span></span>
<span data-ttu-id="8e418-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="8e418-112">Run the command as a job</span></span>

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

### <span data-ttu-id="8e418-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e418-113">-DefaultProfile</span></span>
<span data-ttu-id="8e418-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e418-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e418-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="8e418-115">-GitPropertyUri</span></span>
<span data-ttu-id="8e418-116">URI del repository</span><span class="sxs-lookup"><span data-stu-id="8e418-116">URI of the repository</span></span>

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

### <span data-ttu-id="8e418-117">-Location</span><span class="sxs-lookup"><span data-stu-id="8e418-117">-Location</span></span>
<span data-ttu-id="8e418-118">Posizione GEO della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8e418-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="8e418-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8e418-119">-Name</span></span>
<span data-ttu-id="8e418-120">Nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="8e418-120">The name of the Service resource.</span></span>

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

### <span data-ttu-id="8e418-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8e418-121">-NoWait</span></span>
<span data-ttu-id="8e418-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="8e418-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8e418-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e418-123">-ResourceGroupName</span></span>
<span data-ttu-id="8e418-124">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="8e418-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8e418-125">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="8e418-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8e418-126">-SKUName</span><span class="sxs-lookup"><span data-stu-id="8e418-126">-SkuName</span></span>
<span data-ttu-id="8e418-127">Nome della SKU</span><span class="sxs-lookup"><span data-stu-id="8e418-127">Name of the Sku</span></span>

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

### <span data-ttu-id="8e418-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="8e418-128">-SkuTier</span></span>
<span data-ttu-id="8e418-129">Livello della SKU</span><span class="sxs-lookup"><span data-stu-id="8e418-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="8e418-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e418-130">-SubscriptionId</span></span>
<span data-ttu-id="8e418-131">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8e418-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8e418-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="8e418-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8e418-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="8e418-133">-Tag</span></span>
<span data-ttu-id="8e418-134">Tag del servizio, ovvero un elenco di coppie di valori chiave che descrivono la risorsa.</span><span class="sxs-lookup"><span data-stu-id="8e418-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="8e418-135">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="8e418-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="8e418-136">Chiave di informazioni dettagliate sull'applicazione di destinazione</span><span class="sxs-lookup"><span data-stu-id="8e418-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="8e418-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="8e418-137">-TraceEnabled</span></span>
<span data-ttu-id="8e418-138">Indica se abilitare la funzionalità di traccia</span><span class="sxs-lookup"><span data-stu-id="8e418-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="8e418-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e418-139">-Confirm</span></span>
<span data-ttu-id="8e418-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e418-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e418-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e418-141">-WhatIf</span></span>
<span data-ttu-id="8e418-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e418-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e418-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e418-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e418-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e418-144">CommonParameters</span></span>
<span data-ttu-id="8e418-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e418-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e418-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8e418-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e418-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="8e418-147">INPUTS</span></span>

## <span data-ttu-id="8e418-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e418-148">OUTPUTS</span></span>

### <span data-ttu-id="8e418-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="8e418-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="8e418-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="8e418-150">NOTES</span></span>

<span data-ttu-id="8e418-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8e418-151">ALIASES</span></span>

## <span data-ttu-id="8e418-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e418-152">RELATED LINKS</span></span>

