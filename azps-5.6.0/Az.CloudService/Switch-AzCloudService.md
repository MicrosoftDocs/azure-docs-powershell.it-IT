---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/Switch-AzCloudService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
ms.openlocfilehash: b46ab9b8dee108f6d2126c199e5609d92452b95a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007213"
---
# <span data-ttu-id="3d561-101">Switch-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="3d561-101">Switch-AzCloudService</span></span>

## <span data-ttu-id="3d561-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d561-102">SYNOPSIS</span></span>
<span data-ttu-id="3d561-103">Scambia i VIP tra due servizi cloud (supporto esteso) di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3d561-103">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="3d561-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d561-104">SYNTAX</span></span>

### <span data-ttu-id="3d561-105">CloudServiceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3d561-105">CloudServiceName (Default)</span></span>
```
Switch-AzCloudService -CloudServiceName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Async] [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3d561-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="3d561-106">CloudService</span></span>
```
Switch-AzCloudService -CloudService <CloudService> [-SubscriptionId <String>] [-Async]
 [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3d561-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3d561-107">DESCRIPTION</span></span>
<span data-ttu-id="3d561-108">Scambia i VIP tra due servizi cloud (supporto esteso) di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3d561-108">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="3d561-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d561-109">EXAMPLES</span></span>

### <span data-ttu-id="3d561-110">Esempio 1: Cambiare servizio cloud usando il nome</span><span class="sxs-lookup"><span data-stu-id="3d561-110">Example 1: Switch cloud service using name</span></span>
```powershell
PS C:\> Switch-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="3d561-111">Il comando precedente richiama l'operazione vipswap nel servizio cloud con nome 'BService' ed eseguirà l'operazione quando l'utente conferma l'azione nella richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="3d561-111">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="3d561-112">"BService" con il suo servizio cloud scambiabile.</span><span class="sxs-lookup"><span data-stu-id="3d561-112">'BService' with be swapped with its swappable cloud service.</span></span>

### <span data-ttu-id="3d561-113">Esempio 2: Cambiare servizio cloud usando un oggetto servizio cloud</span><span class="sxs-lookup"><span data-stu-id="3d561-113">Example 2: Switch cloud service using cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Switch-AzCloudService -CloudService $cs

```

<span data-ttu-id="3d561-114">Il comando precedente richiama l'operazione vipswap nel servizio cloud con nome 'BService' ed eseguirà l'operazione quando l'utente conferma l'azione nella richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="3d561-114">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="3d561-115">"BService" con il suo servizio cloud scambiabile.</span><span class="sxs-lookup"><span data-stu-id="3d561-115">'BService' with be swapped with its swappable cloud service.</span></span>

## <span data-ttu-id="3d561-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d561-116">PARAMETERS</span></span>

### <span data-ttu-id="3d561-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d561-117">-AsJob</span></span>
<span data-ttu-id="3d561-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="3d561-118">Run the command as a job</span></span>

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

### <span data-ttu-id="3d561-119">-Async</span><span class="sxs-lookup"><span data-stu-id="3d561-119">-Async</span></span>


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

### <span data-ttu-id="3d561-120">-CloudService</span><span class="sxs-lookup"><span data-stu-id="3d561-120">-CloudService</span></span>
<span data-ttu-id="3d561-121">Per creare, vedere la sezione NOTE per le proprietà CLOUDSERVICE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3d561-121">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d561-122">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="3d561-122">-CloudServiceName</span></span>


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d561-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d561-123">-DefaultProfile</span></span>
<span data-ttu-id="3d561-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d561-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d561-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d561-125">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d561-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d561-126">-SubscriptionId</span></span>
<span data-ttu-id="3d561-127">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3d561-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3d561-128">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3d561-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3d561-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d561-129">-Confirm</span></span>
<span data-ttu-id="3d561-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d561-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d561-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d561-131">-WhatIf</span></span>
<span data-ttu-id="3d561-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d561-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d561-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d561-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d561-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d561-134">CommonParameters</span></span>
<span data-ttu-id="3d561-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d561-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d561-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3d561-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d561-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="3d561-137">INPUTS</span></span>

## <span data-ttu-id="3d561-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d561-138">OUTPUTS</span></span>

### <span data-ttu-id="3d561-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3d561-139">System.Boolean</span></span>

## <span data-ttu-id="3d561-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="3d561-140">NOTES</span></span>

<span data-ttu-id="3d561-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3d561-141">ALIASES</span></span>

<span data-ttu-id="3d561-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="3d561-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d561-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="3d561-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d561-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3d561-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d561-145">SERVIZIO <CloudService> CLOUD:</span><span class="sxs-lookup"><span data-stu-id="3d561-145">CLOUDSERVICE <CloudService>:</span></span> 
  - <span data-ttu-id="3d561-146">`Location <String>`: posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3d561-146">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="3d561-147">`[Configuration <String>]`: specifica la configurazione del servizio XML (con estensione cscfg) per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3d561-147">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="3d561-148">`[ConfigurationUrl <String>]`: specifica un URL che fa riferimento alla posizione della configurazione del servizio nel servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="3d561-148">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="3d561-149">L'URL del pacchetto del servizio può essere URI della firma di accesso condiviso da qualsiasi account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3d561-149">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="3d561-150">Si tratta di una proprietà di sola scrittura e non viene restituita nelle chiamate GET.</span><span class="sxs-lookup"><span data-stu-id="3d561-150">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="3d561-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: descrive un profilo dell'estensione del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3d561-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="3d561-152">`[Extension <IExtension[]>]`: elenco delle estensioni per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3d561-152">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="3d561-153">`[AutoUpgradeMinorVersion <Boolean?>]`: specificare in modo esplicito se la piattaforma può aggiornare automaticamente typeHandlerVersion alle versioni secondarie successive quando diventano disponibili.</span><span class="sxs-lookup"><span data-stu-id="3d561-153">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="3d561-154">`[ForceUpdateTag <String>]`: tag per forzare l'applicazione delle impostazioni pubbliche e protette fornite.</span><span class="sxs-lookup"><span data-stu-id="3d561-154">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="3d561-155">La modifica del valore del tag consente di eseguire di nuovo l'estensione senza modificare le impostazioni pubbliche o protette.</span><span class="sxs-lookup"><span data-stu-id="3d561-155">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="3d561-156">Se forceUpdateTag non viene modificato, gli aggiornamenti alle impostazioni pubbliche o protette verranno comunque applicati dal gestore.</span><span class="sxs-lookup"><span data-stu-id="3d561-156">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="3d561-157">Se né forceUpdateTag né le impostazioni pubbliche o protette vengono modificate, il flusso dell'estensione all'istanza del ruolo viene eseguito con lo stesso numero di sequenza e l'implementazione può essere eseguita di nuovo o meno</span><span class="sxs-lookup"><span data-stu-id="3d561-157">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="3d561-158">`[Name <String>]`: nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="3d561-158">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="3d561-159">`[ProtectedSetting <String>]`: impostazioni protette per l'estensione, crittografate prima dell'invio all'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="3d561-159">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="3d561-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="3d561-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="3d561-161">`[Publisher <String>]`: nome dell'autore del gestore estensioni.</span><span class="sxs-lookup"><span data-stu-id="3d561-161">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="3d561-162">`[RolesAppliedTo <String[]>]`: elenco facoltativo di ruoli per l'applicazione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="3d561-162">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="3d561-163">Se non si specifica la proprietà o si specifica "\*", l'estensione viene applicata a tutti i ruoli nel servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3d561-163">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="3d561-164">`[Setting <String>]`: impostazioni pubbliche per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="3d561-164">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="3d561-165">Per le estensioni JSON, si tratta delle impostazioni JSON per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="3d561-165">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="3d561-166">Per l'estensione XML, ad esempio RDP, si tratta dell'impostazione XML per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="3d561-166">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="3d561-167">`[SourceVaultId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="3d561-167">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="3d561-168">`[Type <String>]`: specifica il tipo dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="3d561-168">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="3d561-169">`[TypeHandlerVersion <String>]`: specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="3d561-169">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="3d561-170">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="3d561-170">Specifies the version of the extension.</span></span> <span data-ttu-id="3d561-171">Se questo elemento non viene specificato o come valore viene usato un asterisco (\*), viene usata la versione più recente dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="3d561-171">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="3d561-172">Se il valore viene specificato con un numero di versione principale e un asterisco come numero di versione secondaria (X.), viene selezionata l'ultima versione secondaria della versione principale specificata.</span><span class="sxs-lookup"><span data-stu-id="3d561-172">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="3d561-173">Se si specifica un numero di versione principale e un numero di versione secondaria (X.Y), viene selezionata la versione dell'estensione specifica.</span><span class="sxs-lookup"><span data-stu-id="3d561-173">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="3d561-174">Se si specifica una versione, viene eseguito un aggiornamento automatico sull'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="3d561-174">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="3d561-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: profilo di rete per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3d561-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="3d561-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: elenco di configurazioni di bilanciamento del carico per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3d561-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="3d561-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: elenco di indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="3d561-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="3d561-178">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="3d561-178">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="3d561-179">`[PrivateIPAddress <String>]`: l'indirizzo IP privato a cui fa riferimento il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3d561-179">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="3d561-180">`[PublicIPAddressId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="3d561-180">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="3d561-181">`[SubnetId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="3d561-181">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="3d561-182">`[Name <String>]`: nome risorsa</span><span class="sxs-lookup"><span data-stu-id="3d561-182">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="3d561-183">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="3d561-183">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="3d561-184">`[Id <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="3d561-184">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="3d561-185">`[OSProfile <ICloudServiceOSProfile>]`: descrive il profilo del sistema operativo per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3d561-185">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="3d561-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: specifica il set di certificati da installare nelle istanze del ruolo.</span><span class="sxs-lookup"><span data-stu-id="3d561-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="3d561-187">`[SourceVaultId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="3d561-187">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="3d561-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: elenco dei riferimenti a vault delle chiavi in SourceVault che contengono certificati.</span><span class="sxs-lookup"><span data-stu-id="3d561-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="3d561-189">`[CertificateUrl <String>]`: URL di un certificato che è stato caricato come segreto nel Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="3d561-189">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="3d561-190">`[PackageUrl <String>]`: specifica un URL che fa riferimento alla posizione del pacchetto del servizio nel servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="3d561-190">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="3d561-191">L'URL del pacchetto del servizio può essere URI della firma di accesso condiviso da qualsiasi account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3d561-191">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="3d561-192">Si tratta di una proprietà di sola scrittura e non viene restituita nelle chiamate GET.</span><span class="sxs-lookup"><span data-stu-id="3d561-192">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="3d561-193">`[RoleProfile <ICloudServiceRoleProfile>]`: descrive il profilo del ruolo per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3d561-193">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="3d561-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: elenco dei ruoli per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3d561-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="3d561-195">`[Name <String>]`: nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3d561-195">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="3d561-196">`[SkuCapacity <Int64?>]`: specifica il numero di istanze di ruoli nel servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3d561-196">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="3d561-197">`[SkuName <String>]`: il nome della SKU.</span><span class="sxs-lookup"><span data-stu-id="3d561-197">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="3d561-198">NOTA: se il nuovo SKU non è supportato nell'hardware in cui è attualmente in esecuzione il servizio cloud, è necessario eliminare e ricreare il servizio cloud o tornare alla SKU precedente.</span><span class="sxs-lookup"><span data-stu-id="3d561-198">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="3d561-199">`[SkuTier <String>]`: specifica il livello del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3d561-199">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="3d561-200">I valori possibili sono</span><span class="sxs-lookup"><span data-stu-id="3d561-200">Possible Values are</span></span> <br /><br /> <span data-ttu-id="3d561-201">**Standard**</span><span class="sxs-lookup"><span data-stu-id="3d561-201">**Standard**</span></span> <br /><br /> <span data-ttu-id="3d561-202">**Di base**</span><span class="sxs-lookup"><span data-stu-id="3d561-202">**Basic**</span></span>
  - <span data-ttu-id="3d561-203">`[StartCloudService <Boolean?>]`: (Facoltativo) Indica se avviare il servizio cloud immediatamente dopo la sua creazione.</span><span class="sxs-lookup"><span data-stu-id="3d561-203">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="3d561-204">Il valore predefinito è `true` .</span><span class="sxs-lookup"><span data-stu-id="3d561-204">The default value is `true`.</span></span>         <span data-ttu-id="3d561-205">Se false, il modello di servizio è ancora distribuito, ma il codice non viene eseguito immediatamente.</span><span class="sxs-lookup"><span data-stu-id="3d561-205">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="3d561-206">Il servizio è invece PoweredOff fino a quando non si chiama Start, in corrispondenza del quale verrà avviato il servizio.</span><span class="sxs-lookup"><span data-stu-id="3d561-206">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="3d561-207">Un servizio distribuito continua a sostenere addebiti, anche se con tecnologia poweredoff.</span><span class="sxs-lookup"><span data-stu-id="3d561-207">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="3d561-208">`[Tag <ICloudServiceTags>]`: tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="3d561-208">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="3d561-209">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3d561-209">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="3d561-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`: modalità di aggiornamento per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3d561-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="3d561-211">Le istanze del ruolo vengono allocate per aggiornare i domini durante la distribuzione del servizio.</span><span class="sxs-lookup"><span data-stu-id="3d561-211">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="3d561-212">Gli aggiornamenti possono essere avviati manualmente in ogni dominio di aggiornamento o avviati automaticamente in tutti i domini di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3d561-212">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="3d561-213">I valori possibili sono</span><span class="sxs-lookup"><span data-stu-id="3d561-213">Possible Values are</span></span> <br /><br /><span data-ttu-id="3d561-214">**Automatico**</span><span class="sxs-lookup"><span data-stu-id="3d561-214">**Auto**</span></span><br /><br /><span data-ttu-id="3d561-215">**Manuale**</span><span class="sxs-lookup"><span data-stu-id="3d561-215">**Manual**</span></span> <br /><br /><span data-ttu-id="3d561-216">**Simultaneo**</span><span class="sxs-lookup"><span data-stu-id="3d561-216">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="3d561-217">Se non viene specificato, il valore predefinito è Auto. Se impostato su Manuale, è necessario chiamare PUT UpdateDomain per applicare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3d561-217">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="3d561-218">Se impostato su Auto, l'aggiornamento viene applicato automaticamente a ogni dominio di aggiornamento in sequenza.</span><span class="sxs-lookup"><span data-stu-id="3d561-218">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="3d561-219">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d561-219">RELATED LINKS</span></span>

