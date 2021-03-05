---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-AzCloudServiceNetworkInterfaces
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
ms.openlocfilehash: ae6bb602e90fd86334a28a804deed2be429347ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008109"
---
# <span data-ttu-id="ecbc6-101">Get-AzCloudServiceNetworkInterfaces</span><span class="sxs-lookup"><span data-stu-id="ecbc6-101">Get-AzCloudServiceNetworkInterfaces</span></span>

## <span data-ttu-id="ecbc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecbc6-102">SYNOPSIS</span></span>
<span data-ttu-id="ecbc6-103">Ottenere le interfacce di rete di un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-103">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="ecbc6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecbc6-104">SYNTAX</span></span>

### <span data-ttu-id="ecbc6-105">CloudServiceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ecbc6-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-RoleInstanceName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ecbc6-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="ecbc6-106">CloudService</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudService <CloudService> [-SubscriptionId <String>]
 [-RoleInstanceName <String>] [<CommonParameters>]
```

## <span data-ttu-id="ecbc6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ecbc6-107">DESCRIPTION</span></span>
<span data-ttu-id="ecbc6-108">Ottenere le interfacce di rete di un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-108">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="ecbc6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecbc6-109">EXAMPLES</span></span>

### <span data-ttu-id="ecbc6-110">Esempio 1: Ottenere le interfacce di rete con il nome di un servizio cloud</span><span class="sxs-lookup"><span data-stu-id="ecbc6-110">Example 1: Get network interfaces by a cloud service name</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="ecbc6-111">Ottiene tutte le interfacce di rete per un dato nome di servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-111">Gets all the network interfaces for a given cloud service name.</span></span>

### <span data-ttu-id="ecbc6-112">Esempio 2: Ottenere le interfacce di rete da un oggetto servizio cloud</span><span class="sxs-lookup"><span data-stu-id="ecbc6-112">Example 2: Get network interfaces by a cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs

```

<span data-ttu-id="ecbc6-113">Ottiene tutte le interfacce di rete per un determinato oggetto servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-113">Gets all the network interfaces for a given cloud service object.</span></span>

### <span data-ttu-id="ecbc6-114">Esempio 3: Ottenere le interfacce di rete da un oggetto servizio cloud e dal nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-114">Example 3: Get network interfaces by a cloud service object and role instance name.</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs -RoleInstanceName WebRole1_IN_0

```

<span data-ttu-id="ecbc6-115">Ottiene tutte le interfacce di rete per un determinato oggetto servizio cloud e il nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-115">Gets all the network interfaces for a given cloud service object and role instance name.</span></span>

## <span data-ttu-id="ecbc6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecbc6-116">PARAMETERS</span></span>

### <span data-ttu-id="ecbc6-117">-CloudService</span><span class="sxs-lookup"><span data-stu-id="ecbc6-117">-CloudService</span></span>
<span data-ttu-id="ecbc6-118">Istanza di CloudService.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-118">CloudService instance.</span></span>
<span data-ttu-id="ecbc6-119">Per creare, vedere la sezione NOTE per le proprietà CLOUDSERVICE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-119">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ecbc6-120">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="ecbc6-120">-CloudServiceName</span></span>
<span data-ttu-id="ecbc6-121">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-121">CloudServiceName.</span></span>

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

### <span data-ttu-id="ecbc6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecbc6-122">-ResourceGroupName</span></span>
<span data-ttu-id="ecbc6-123">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-123">ResourceGroupName.</span></span>

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

### <span data-ttu-id="ecbc6-124">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="ecbc6-124">-RoleInstanceName</span></span>
<span data-ttu-id="ecbc6-125">RoleInstanceName.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-125">RoleInstanceName.</span></span>

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

### <span data-ttu-id="ecbc6-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ecbc6-126">-SubscriptionId</span></span>
<span data-ttu-id="ecbc6-127">Abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-127">Subscription.</span></span>

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

### <span data-ttu-id="ecbc6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecbc6-128">CommonParameters</span></span>
<span data-ttu-id="ecbc6-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecbc6-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecbc6-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="ecbc6-131">INPUTS</span></span>

## <span data-ttu-id="ecbc6-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecbc6-132">OUTPUTS</span></span>

## <span data-ttu-id="ecbc6-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="ecbc6-133">NOTES</span></span>

<span data-ttu-id="ecbc6-134">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ecbc6-134">ALIASES</span></span>

<span data-ttu-id="ecbc6-135">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="ecbc6-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ecbc6-136">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ecbc6-137">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ecbc6-138"><CloudService>CLOUDSERVICE: istanza di CloudService.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-138">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="ecbc6-139">`Location <String>`: posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-139">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="ecbc6-140">`[Configuration <String>]`: specifica la configurazione del servizio XML (con estensione cscfg) per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-140">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="ecbc6-141">`[ConfigurationUrl <String>]`: specifica un URL che fa riferimento alla posizione della configurazione del servizio nel servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-141">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="ecbc6-142">L'URL del pacchetto del servizio può essere UN URI della firma di accesso condiviso da qualsiasi account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-142">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="ecbc6-143">Si tratta di una proprietà di sola scrittura e non viene restituita nelle chiamate GET.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-143">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="ecbc6-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: descrive un profilo di estensione del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="ecbc6-145">`[Extension <IExtension[]>]`: elenco delle estensioni per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-145">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="ecbc6-146">`[AutoUpgradeMinorVersion <Boolean?>]`: specificare in modo esplicito se la piattaforma può aggiornare automaticamente typeHandlerVersion alle versioni secondarie successive quando diventano disponibili.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-146">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="ecbc6-147">`[ForceUpdateTag <String>]`: tag per forzare l'applicazione delle impostazioni pubbliche e protette fornite.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-147">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="ecbc6-148">La modifica del valore del tag consente di eseguire di nuovo l'estensione senza modificare le impostazioni pubbliche o protette.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-148">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="ecbc6-149">Se forceUpdateTag non viene modificato, gli aggiornamenti alle impostazioni pubbliche o protette verranno comunque applicati dal gestore.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-149">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="ecbc6-150">Se né forceUpdateTag né le impostazioni pubbliche o protette vengono modificate, il flusso dell'estensione all'istanza del ruolo viene eseguito con lo stesso numero di sequenza e l'implementazione può essere eseguita di nuovo o meno</span><span class="sxs-lookup"><span data-stu-id="ecbc6-150">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="ecbc6-151">`[Name <String>]`: nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-151">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="ecbc6-152">`[ProtectedSetting <String>]`: impostazioni protette per l'estensione, crittografate prima dell'invio all'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-152">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="ecbc6-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="ecbc6-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="ecbc6-154">`[Publisher <String>]`: nome dell'autore del gestore estensioni.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-154">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="ecbc6-155">`[RolesAppliedTo <String[]>]`: elenco facoltativo di ruoli per applicare questa estensione.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-155">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="ecbc6-156">Se non si specifica la proprietà o si specifica "\*", l'estensione viene applicata a tutti i ruoli nel servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-156">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="ecbc6-157">`[Setting <String>]`: impostazioni pubbliche per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-157">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="ecbc6-158">Per le estensioni JSON, si tratta delle impostazioni JSON per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-158">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="ecbc6-159">Per l'estensione XML, ad esempio RDP, questa è l'impostazione XML per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-159">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="ecbc6-160">`[SourceVaultId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="ecbc6-160">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="ecbc6-161">`[Type <String>]`: specifica il tipo dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-161">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="ecbc6-162">`[TypeHandlerVersion <String>]`: specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-162">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="ecbc6-163">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-163">Specifies the version of the extension.</span></span> <span data-ttu-id="ecbc6-164">Se questo elemento non viene specificato o come valore viene usato un asterisco (\*), viene usata la versione più recente dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-164">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="ecbc6-165">Se il valore viene specificato con un numero di versione principale e un asterisco come numero di versione secondaria (X.), viene selezionata l'ultima versione secondaria della versione principale specificata.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-165">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="ecbc6-166">Se si specifica un numero di versione principale e un numero di versione secondaria (X.Y), viene selezionata la versione dell'estensione specifica.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-166">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="ecbc6-167">Se si specifica una versione, viene eseguito un aggiornamento automatico sull'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-167">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="ecbc6-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`: profilo di rete per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="ecbc6-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: elenco di configurazioni di bilanciamento del carico per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="ecbc6-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: elenco di indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="ecbc6-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="ecbc6-171">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="ecbc6-171">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="ecbc6-172">`[PrivateIPAddress <String>]`: l'indirizzo IP privato a cui fa riferimento il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-172">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="ecbc6-173">`[PublicIPAddressId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="ecbc6-173">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="ecbc6-174">`[SubnetId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="ecbc6-174">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="ecbc6-175">`[Name <String>]`: nome risorsa</span><span class="sxs-lookup"><span data-stu-id="ecbc6-175">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="ecbc6-176">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="ecbc6-176">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="ecbc6-177">`[Id <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="ecbc6-177">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="ecbc6-178">`[OSProfile <ICloudServiceOSProfile>]`: descrive il profilo del sistema operativo per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-178">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="ecbc6-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`: specifica il set di certificati da installare nelle istanze del ruolo.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="ecbc6-180">`[SourceVaultId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="ecbc6-180">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="ecbc6-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: elenco dei riferimenti a vault chiave in SourceVault che contengono certificati.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="ecbc6-182">`[CertificateUrl <String>]`: URL di un certificato che è stato caricato come segreto nel Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-182">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="ecbc6-183">`[PackageUrl <String>]`: specifica un URL che fa riferimento alla posizione del pacchetto del servizio nel servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-183">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="ecbc6-184">L'URL del pacchetto del servizio può essere UN URI della firma di accesso condiviso da qualsiasi account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-184">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="ecbc6-185">Si tratta di una proprietà di sola scrittura e non viene restituita nelle chiamate GET.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-185">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="ecbc6-186">`[RoleProfile <ICloudServiceRoleProfile>]`: descrive il profilo del ruolo per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-186">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="ecbc6-187">`[Role <ICloudServiceRoleProfileProperties[]>]`: elenco dei ruoli per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-187">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="ecbc6-188">`[Name <String>]`: nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-188">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="ecbc6-189">`[SkuCapacity <Int64?>]`: specifica il numero di istanze di ruoli nel servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-189">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="ecbc6-190">`[SkuName <String>]`: nome della SKU.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-190">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="ecbc6-191">NOTA: se il nuovo SKU non è supportato nell'hardware in cui è attualmente in uso il servizio cloud, è necessario eliminare e ricreare il servizio cloud o tornare alla SKU precedente.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-191">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="ecbc6-192">`[SkuTier <String>]`: specifica il livello del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-192">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="ecbc6-193">I valori possibili sono</span><span class="sxs-lookup"><span data-stu-id="ecbc6-193">Possible Values are</span></span> <br /><br /> <span data-ttu-id="ecbc6-194">**Standard**</span><span class="sxs-lookup"><span data-stu-id="ecbc6-194">**Standard**</span></span> <br /><br /> <span data-ttu-id="ecbc6-195">**Di base**</span><span class="sxs-lookup"><span data-stu-id="ecbc6-195">**Basic**</span></span>
  - <span data-ttu-id="ecbc6-196">`[StartCloudService <Boolean?>]`: (Facoltativo) Indica se avviare il servizio cloud immediatamente dopo la sua creazione.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-196">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="ecbc6-197">Il valore predefinito è `true` .</span><span class="sxs-lookup"><span data-stu-id="ecbc6-197">The default value is `true`.</span></span>         <span data-ttu-id="ecbc6-198">Se false, il modello di servizio è ancora distribuito, ma il codice non viene eseguito immediatamente.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-198">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="ecbc6-199">Il servizio è invece PoweredOff fino a quando non si chiama Start, in corrispondenza del quale verrà avviato il servizio.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-199">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="ecbc6-200">Un servizio distribuito continua a sostenere addebiti, anche se con tecnologia poweredoff.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-200">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="ecbc6-201">`[Tag <ICloudServiceTags>]`: tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-201">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="ecbc6-202">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-202">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ecbc6-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`: modalità di aggiornamento per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="ecbc6-204">Le istanze del ruolo vengono allocate per aggiornare i domini durante la distribuzione del servizio.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-204">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="ecbc6-205">Gli aggiornamenti possono essere avviati manualmente in ogni dominio di aggiornamento o avviati automaticamente in tutti i domini di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-205">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="ecbc6-206">I valori possibili sono</span><span class="sxs-lookup"><span data-stu-id="ecbc6-206">Possible Values are</span></span> <br /><br /><span data-ttu-id="ecbc6-207">**Automatico**</span><span class="sxs-lookup"><span data-stu-id="ecbc6-207">**Auto**</span></span><br /><br /><span data-ttu-id="ecbc6-208">**Manuale**</span><span class="sxs-lookup"><span data-stu-id="ecbc6-208">**Manual**</span></span> <br /><br /><span data-ttu-id="ecbc6-209">**Simultaneo**</span><span class="sxs-lookup"><span data-stu-id="ecbc6-209">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="ecbc6-210">Se non viene specificato, il valore predefinito è Auto. Se impostato su Manuale, è necessario chiamare PUT UpdateDomain per applicare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-210">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="ecbc6-211">Se impostato su Auto, l'aggiornamento viene applicato automaticamente a ogni dominio di aggiornamento in sequenza.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-211">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="ecbc6-212">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecbc6-212">RELATED LINKS</span></span>

