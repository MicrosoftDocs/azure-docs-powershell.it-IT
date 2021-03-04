---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-AzCloudServicePublicIPAddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
ms.openlocfilehash: d875ad9af0ebe864f9d396fed44961a5d48f38c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975949"
---
# <span data-ttu-id="aeab1-101">Get-AzCloudServicePublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="aeab1-101">Get-AzCloudServicePublicIPAddress</span></span>

## <span data-ttu-id="aeab1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeab1-102">SYNOPSIS</span></span>
<span data-ttu-id="aeab1-103">Ottenere l'indirizzo IP pubblico di un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-103">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="aeab1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aeab1-104">SYNTAX</span></span>

### <span data-ttu-id="aeab1-105">CloudServiceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aeab1-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [<CommonParameters>]
```

### <span data-ttu-id="aeab1-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="aeab1-106">CloudService</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudService <CloudService> [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="aeab1-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aeab1-107">DESCRIPTION</span></span>
<span data-ttu-id="aeab1-108">Ottenere l'indirizzo IP pubblico di un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-108">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="aeab1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aeab1-109">EXAMPLES</span></span>

### <span data-ttu-id="aeab1-110">Esempio 1: Ottenere gli indirizzi IP pubblici a livello di istanza per un nome di servizio cloud specificato.</span><span class="sxs-lookup"><span data-stu-id="aeab1-110">Example 1: Get instance level public IP addresses for a given cloud service name.</span></span>
```powershell
PS C:\> Get-AzCloudServicePublicIPAddress -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="aeab1-111">Ottiene gli indirizzi IP pubblici a livello di istanza per un determinato nome di servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-111">Gets the instance level public IP addresses for a given cloud service name.</span></span>

### <span data-ttu-id="aeab1-112">Esempio 2: Ottenere indirizzi IP pubblici a livello di istanza per un determinato oggetto servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-112">Example 2: Get instance level public IP addresses for a given cloud service object.</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServicePublicIPAddress -CloudService $cs

```

<span data-ttu-id="aeab1-113">Ottiene gli indirizzi IP pubblici a livello di istanza per un determinato oggetto servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-113">Gets the instance level public IP addresses for a given cloud service object.</span></span>

## <span data-ttu-id="aeab1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aeab1-114">PARAMETERS</span></span>

### <span data-ttu-id="aeab1-115">-CloudService</span><span class="sxs-lookup"><span data-stu-id="aeab1-115">-CloudService</span></span>
<span data-ttu-id="aeab1-116">Istanza di CloudService.</span><span class="sxs-lookup"><span data-stu-id="aeab1-116">CloudService instance.</span></span>
<span data-ttu-id="aeab1-117">Per creare, vedere la sezione NOTE per le proprietà CLOUDSERVICE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="aeab1-117">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

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

### <span data-ttu-id="aeab1-118">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="aeab1-118">-CloudServiceName</span></span>
<span data-ttu-id="aeab1-119">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="aeab1-119">CloudServiceName.</span></span>

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

### <span data-ttu-id="aeab1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeab1-120">-ResourceGroupName</span></span>
<span data-ttu-id="aeab1-121">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="aeab1-121">ResourceGroupName.</span></span>

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

### <span data-ttu-id="aeab1-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aeab1-122">-SubscriptionId</span></span>
<span data-ttu-id="aeab1-123">Abbonamento.</span><span class="sxs-lookup"><span data-stu-id="aeab1-123">Subscription.</span></span>

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

### <span data-ttu-id="aeab1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeab1-124">CommonParameters</span></span>
<span data-ttu-id="aeab1-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeab1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeab1-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aeab1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeab1-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="aeab1-127">INPUTS</span></span>

## <span data-ttu-id="aeab1-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aeab1-128">OUTPUTS</span></span>

## <span data-ttu-id="aeab1-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="aeab1-129">NOTES</span></span>

<span data-ttu-id="aeab1-130">ALIAS</span><span class="sxs-lookup"><span data-stu-id="aeab1-130">ALIASES</span></span>

<span data-ttu-id="aeab1-131">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="aeab1-131">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aeab1-132">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="aeab1-132">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aeab1-133">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aeab1-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aeab1-134"><CloudService>CLOUDSERVICE: istanza di CloudService.</span><span class="sxs-lookup"><span data-stu-id="aeab1-134">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="aeab1-135">`Location <String>`: posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="aeab1-135">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="aeab1-136">`[Configuration <String>]`: specifica la configurazione del servizio XML (con estensione cscfg) per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-136">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="aeab1-137">`[ConfigurationUrl <String>]`: specifica un URL che fa riferimento alla posizione della configurazione del servizio nel servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="aeab1-137">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="aeab1-138">L'URL del pacchetto del servizio può essere UN URI della firma di accesso condiviso da qualsiasi account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aeab1-138">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="aeab1-139">Si tratta di una proprietà di sola scrittura e non viene restituita nelle chiamate GET.</span><span class="sxs-lookup"><span data-stu-id="aeab1-139">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="aeab1-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: descrive un profilo dell'estensione del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="aeab1-141">`[Extension <IExtension[]>]`: elenco di estensioni per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-141">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="aeab1-142">`[AutoUpgradeMinorVersion <Boolean?>]`: specificare in modo esplicito se la piattaforma può aggiornare automaticamente typeHandlerVersion alle versioni secondarie successive quando diventano disponibili.</span><span class="sxs-lookup"><span data-stu-id="aeab1-142">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="aeab1-143">`[ForceUpdateTag <String>]`: tag per forzare l'applicazione delle impostazioni pubbliche e protette fornite.</span><span class="sxs-lookup"><span data-stu-id="aeab1-143">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="aeab1-144">La modifica del valore del tag consente di eseguire di nuovo l'estensione senza modificare le impostazioni pubbliche o protette.</span><span class="sxs-lookup"><span data-stu-id="aeab1-144">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="aeab1-145">Se forceUpdateTag non viene modificato, gli aggiornamenti alle impostazioni pubbliche o protette verranno comunque applicati dal gestore.</span><span class="sxs-lookup"><span data-stu-id="aeab1-145">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="aeab1-146">Se né forceUpdateTag né le impostazioni pubbliche o protette vengono modificate, il flusso dell'estensione all'istanza del ruolo viene eseguito con lo stesso numero di sequenza e l'implementazione può essere eseguita di nuovo o meno</span><span class="sxs-lookup"><span data-stu-id="aeab1-146">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="aeab1-147">`[Name <String>]`: nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="aeab1-147">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="aeab1-148">`[ProtectedSetting <String>]`: impostazioni protette per l'estensione, crittografate prima dell'invio all'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="aeab1-148">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="aeab1-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="aeab1-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="aeab1-150">`[Publisher <String>]`: nome dell'autore del gestore estensioni.</span><span class="sxs-lookup"><span data-stu-id="aeab1-150">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="aeab1-151">`[RolesAppliedTo <String[]>]`: elenco facoltativo di ruoli per l'applicazione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="aeab1-151">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="aeab1-152">Se non si specifica la proprietà o si specifica "\*", l'estensione viene applicata a tutti i ruoli nel servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-152">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="aeab1-153">`[Setting <String>]`: impostazioni pubbliche per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="aeab1-153">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="aeab1-154">Per le estensioni JSON, si tratta delle impostazioni JSON per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="aeab1-154">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="aeab1-155">Per l'estensione XML, ad esempio RDP, questa è l'impostazione XML per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="aeab1-155">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="aeab1-156">`[SourceVaultId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="aeab1-156">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="aeab1-157">`[Type <String>]`: specifica il tipo dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="aeab1-157">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="aeab1-158">`[TypeHandlerVersion <String>]`: specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="aeab1-158">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="aeab1-159">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="aeab1-159">Specifies the version of the extension.</span></span> <span data-ttu-id="aeab1-160">Se questo elemento non viene specificato o come valore viene usato un asterisco (\*), viene usata la versione più recente dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="aeab1-160">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="aeab1-161">Se il valore viene specificato con un numero di versione principale e un asterisco come numero di versione secondaria (X.), viene selezionata l'ultima versione secondaria della versione principale specificata.</span><span class="sxs-lookup"><span data-stu-id="aeab1-161">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="aeab1-162">Se si specifica un numero di versione principale e un numero di versione secondaria (X.Y), viene selezionata la versione dell'estensione specifica.</span><span class="sxs-lookup"><span data-stu-id="aeab1-162">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="aeab1-163">Se si specifica una versione, viene eseguito un aggiornamento automatico sull'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="aeab1-163">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="aeab1-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`: profilo di rete per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="aeab1-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: elenco di configurazioni di bilanciamento del carico per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="aeab1-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: elenco di indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="aeab1-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="aeab1-167">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="aeab1-167">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="aeab1-168">`[PrivateIPAddress <String>]`: l'indirizzo IP privato a cui fa riferimento il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-168">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="aeab1-169">`[PublicIPAddressId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="aeab1-169">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="aeab1-170">`[SubnetId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="aeab1-170">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="aeab1-171">`[Name <String>]`: nome risorsa</span><span class="sxs-lookup"><span data-stu-id="aeab1-171">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="aeab1-172">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="aeab1-172">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="aeab1-173">`[Id <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="aeab1-173">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="aeab1-174">`[OSProfile <ICloudServiceOSProfile>]`: descrive il profilo del sistema operativo per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-174">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="aeab1-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`: specifica il set di certificati da installare nelle istanze del ruolo.</span><span class="sxs-lookup"><span data-stu-id="aeab1-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="aeab1-176">`[SourceVaultId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="aeab1-176">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="aeab1-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: elenco dei riferimenti a vault delle chiavi in SourceVault che contengono certificati.</span><span class="sxs-lookup"><span data-stu-id="aeab1-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="aeab1-178">`[CertificateUrl <String>]`: URL di un certificato che è stato caricato come segreto nel Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="aeab1-178">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="aeab1-179">`[PackageUrl <String>]`: specifica un URL che fa riferimento alla posizione del pacchetto del servizio nel servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="aeab1-179">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="aeab1-180">L'URL del pacchetto del servizio può essere UN URI della firma di accesso condiviso da qualsiasi account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aeab1-180">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="aeab1-181">Si tratta di una proprietà di sola scrittura e non viene restituita nelle chiamate GET.</span><span class="sxs-lookup"><span data-stu-id="aeab1-181">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="aeab1-182">`[RoleProfile <ICloudServiceRoleProfile>]`: descrive il profilo del ruolo per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-182">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="aeab1-183">`[Role <ICloudServiceRoleProfileProperties[]>]`: elenco dei ruoli per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-183">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="aeab1-184">`[Name <String>]`: nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="aeab1-184">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="aeab1-185">`[SkuCapacity <Int64?>]`: specifica il numero di istanze di ruoli nel servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-185">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="aeab1-186">`[SkuName <String>]`: nome della SKU.</span><span class="sxs-lookup"><span data-stu-id="aeab1-186">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="aeab1-187">NOTA: se il nuovo SKU non è supportato nell'hardware in cui è attualmente in uso il servizio cloud, è necessario eliminare e ricreare il servizio cloud o tornare alla SKU precedente.</span><span class="sxs-lookup"><span data-stu-id="aeab1-187">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="aeab1-188">`[SkuTier <String>]`: specifica il livello del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-188">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="aeab1-189">I valori possibili sono</span><span class="sxs-lookup"><span data-stu-id="aeab1-189">Possible Values are</span></span> <br /><br /> <span data-ttu-id="aeab1-190">**Standard**</span><span class="sxs-lookup"><span data-stu-id="aeab1-190">**Standard**</span></span> <br /><br /> <span data-ttu-id="aeab1-191">**Di base**</span><span class="sxs-lookup"><span data-stu-id="aeab1-191">**Basic**</span></span>
  - <span data-ttu-id="aeab1-192">`[StartCloudService <Boolean?>]`: (Facoltativo) Indica se avviare il servizio cloud immediatamente dopo la sua creazione.</span><span class="sxs-lookup"><span data-stu-id="aeab1-192">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="aeab1-193">Il valore predefinito è `true` .</span><span class="sxs-lookup"><span data-stu-id="aeab1-193">The default value is `true`.</span></span>         <span data-ttu-id="aeab1-194">Se false, il modello di servizio è ancora distribuito, ma il codice non viene eseguito immediatamente.</span><span class="sxs-lookup"><span data-stu-id="aeab1-194">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="aeab1-195">Il servizio è invece PoweredOff fino a quando non si chiama Start, in corrispondenza del quale verrà avviato il servizio.</span><span class="sxs-lookup"><span data-stu-id="aeab1-195">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="aeab1-196">Un servizio distribuito continua a sostenere addebiti, anche se con tecnologia poweredoff.</span><span class="sxs-lookup"><span data-stu-id="aeab1-196">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="aeab1-197">`[Tag <ICloudServiceTags>]`: tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="aeab1-197">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="aeab1-198">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aeab1-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="aeab1-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`: modalità di aggiornamento per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="aeab1-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="aeab1-200">Le istanze del ruolo vengono allocate per aggiornare i domini durante la distribuzione del servizio.</span><span class="sxs-lookup"><span data-stu-id="aeab1-200">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="aeab1-201">Gli aggiornamenti possono essere avviati manualmente in ogni dominio di aggiornamento o avviati automaticamente in tutti i domini di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="aeab1-201">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="aeab1-202">I valori possibili sono</span><span class="sxs-lookup"><span data-stu-id="aeab1-202">Possible Values are</span></span> <br /><br /><span data-ttu-id="aeab1-203">**Automatico**</span><span class="sxs-lookup"><span data-stu-id="aeab1-203">**Auto**</span></span><br /><br /><span data-ttu-id="aeab1-204">**Manuale**</span><span class="sxs-lookup"><span data-stu-id="aeab1-204">**Manual**</span></span> <br /><br /><span data-ttu-id="aeab1-205">**Simultaneo**</span><span class="sxs-lookup"><span data-stu-id="aeab1-205">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="aeab1-206">Se non viene specificato, il valore predefinito è Auto. Se impostato su Manuale, è necessario chiamare PUT UpdateDomain per applicare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="aeab1-206">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="aeab1-207">Se impostato su Auto, l'aggiornamento viene applicato automaticamente a ogni dominio di aggiornamento in sequenza.</span><span class="sxs-lookup"><span data-stu-id="aeab1-207">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="aeab1-208">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aeab1-208">RELATED LINKS</span></span>

