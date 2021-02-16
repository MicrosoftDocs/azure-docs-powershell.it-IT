---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/new-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
ms.openlocfilehash: 24e90ebae59c9d9a4449c57270b7ca69f9b05b88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199438"
---
# <span data-ttu-id="b2e5b-101">New-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="b2e5b-101">New-AzCloudService</span></span>

## <span data-ttu-id="b2e5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2e5b-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e5b-103">Creare o aggiornare un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-103">Create or update a cloud service.</span></span>
<span data-ttu-id="b2e5b-104">Tenere presente che alcune proprietà possono essere impostate solo durante la creazione di servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="b2e5b-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2e5b-105">SYNTAX</span></span>

```
New-AzCloudService -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Configuration <String>] [-ConfigurationUrl <String>] [-ExtensionProfile <ICloudServiceExtensionProfile>]
 [-NetworkProfile <ICloudServiceNetworkProfile>] [-OSProfile <ICloudServiceOSProfile>] [-PackageUrl <String>]
 [-RoleProfile <ICloudServiceRoleProfile>] [-StartCloudService] [-Tag <Hashtable>]
 [-UpgradeMode <CloudServiceUpgradeMode>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b2e5b-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b2e5b-106">DESCRIPTION</span></span>
<span data-ttu-id="b2e5b-107">Creare o aggiornare un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-107">Create or update a cloud service.</span></span>
<span data-ttu-id="b2e5b-108">Tenere presente che alcune proprietà possono essere impostate solo durante la creazione del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="b2e5b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2e5b-109">EXAMPLES</span></span>

### <span data-ttu-id="b2e5b-110">Esempio 1: Creare un nuovo servizio cloud con un singolo ruolo</span><span class="sxs-lookup"><span data-stu-id="b2e5b-110">Example 1: Create new cloud service with single role</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile
```

<span data-ttu-id="b2e5b-111">Sopra il set di comandi viene creato un servizio cloud con un singolo ruolo</span><span class="sxs-lookup"><span data-stu-id="b2e5b-111">Above set of commands creates a cloud service with single role</span></span>

### <span data-ttu-id="b2e5b-112">Esempio 2: Creare un nuovo servizio cloud con ruolo singolo ed estensione RDP</span><span class="sxs-lookup"><span data-stu-id="b2e5b-112">Example 2: Create new cloud service with single role and RDP extension</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosoOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
PS C:\> $extensionProfile = @{extension = @($extension)}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile
```

<span data-ttu-id="b2e5b-113">Il set di comandi precedente crea un servizio cloud con un ruolo singolo e l'estensione RDP</span><span class="sxs-lookup"><span data-stu-id="b2e5b-113">Above set of commands creates a cloud service with single role and RDP extension</span></span>

### <span data-ttu-id="b2e5b-114">Esempio 3: Creare un nuovo servizio cloud con un ruolo singolo e un certificato dal vault chiave</span><span class="sxs-lookup"><span data-stu-id="b2e5b-114">Example 3: Create new cloud service with single role and certificate from key vault</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create OS profile object
$keyVault = Get-AzKeyVault -ResourceGroupName ContosOrg -VaultName ContosKeyVault
$certificate=Get-AzKeyVaultCertificate -VaultName ContosKeyVault -Name ContosCert
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
$osProfile = @{secret = @($secretGroup)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -OSProfile $osProfile
```

<span data-ttu-id="b2e5b-115">Sopra il set di comandi crea un servizio cloud con un ruolo singolo e un certificato dal vault chiave.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-115">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

### <span data-ttu-id="b2e5b-116">Esempio 4: Creare un nuovo servizio cloud con più ruoli ed estensioni</span><span class="sxs-lookup"><span data-stu-id="b2e5b-116">Example 4: Create new cloud service with multiple roles and extensions</span></span>
```powershell
# Create role profile object
PS C:\> $role1 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $role2 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoBackend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role1, $role2)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'

# Create Geneva extension object
PS C:\> $genevaExtension = New-AzCloudServiceExtensionObject -Name GenevaExtension -Publisher Microsoft.Azure.Geneva -Type GenevaMonitoringPaaS -TypeHandlerVersion "2.14.0.2"
PS C:\> $extensionProfile = @{extension = @($rdpExtension, $genevaExtension)}

# Add tags
$tag=@{"Owner" = "Contoso"}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile                           `
                  -Tag $tag
```

<span data-ttu-id="b2e5b-117">Sopra il set di comandi crea un servizio cloud con un ruolo singolo e un certificato dal vault chiave.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-117">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

## <span data-ttu-id="b2e5b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2e5b-118">PARAMETERS</span></span>

### <span data-ttu-id="b2e5b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2e5b-119">-AsJob</span></span>
<span data-ttu-id="b2e5b-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="b2e5b-120">Run the command as a job</span></span>

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

### <span data-ttu-id="b2e5b-121">-Configuration</span><span class="sxs-lookup"><span data-stu-id="b2e5b-121">-Configuration</span></span>
<span data-ttu-id="b2e5b-122">Specifica la configurazione del servizio XML (con estensione cscfg) per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-122">Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>

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

### <span data-ttu-id="b2e5b-123">-ConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="b2e5b-123">-ConfigurationUrl</span></span>
<span data-ttu-id="b2e5b-124">Specifica un URL che fa riferimento alla posizione della configurazione del servizio nel servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-124">Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span>
<span data-ttu-id="b2e5b-125">L'URL del pacchetto del servizio può essere UN URI della firma di accesso condiviso da qualsiasi account di archiviazione. Si tratta di una proprietà di sola scrittura e non viene restituita nelle chiamate GET.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-125">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

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

### <span data-ttu-id="b2e5b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e5b-126">-DefaultProfile</span></span>
<span data-ttu-id="b2e5b-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2e5b-128">-ExtensionProfile</span><span class="sxs-lookup"><span data-stu-id="b2e5b-128">-ExtensionProfile</span></span>
<span data-ttu-id="b2e5b-129">Descrive un profilo di estensione del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-129">Describes a cloud service extension profile.</span></span>
<span data-ttu-id="b2e5b-130">Per creare, vedere la sezione NOTE per le proprietà EXTENSIONPROFILE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-130">To construct, see NOTES section for EXTENSIONPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceExtensionProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e5b-131">-Location</span><span class="sxs-lookup"><span data-stu-id="b2e5b-131">-Location</span></span>
<span data-ttu-id="b2e5b-132">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-132">Resource location.</span></span>

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

### <span data-ttu-id="b2e5b-133">-Name</span><span class="sxs-lookup"><span data-stu-id="b2e5b-133">-Name</span></span>
<span data-ttu-id="b2e5b-134">Nome del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-134">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e5b-135">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b2e5b-135">-NetworkProfile</span></span>
<span data-ttu-id="b2e5b-136">Profilo di rete per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-136">Network Profile for the cloud service.</span></span>
<span data-ttu-id="b2e5b-137">Per creare, vedere la sezione NOTE per le proprietà NETWORKPROFILE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-137">To construct, see NOTES section for NETWORKPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceNetworkProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e5b-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b2e5b-138">-NoWait</span></span>
<span data-ttu-id="b2e5b-139">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="b2e5b-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b2e5b-140">-OSProfile</span><span class="sxs-lookup"><span data-stu-id="b2e5b-140">-OSProfile</span></span>
<span data-ttu-id="b2e5b-141">Descrive il profilo del sistema operativo per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-141">Describes the OS profile for the cloud service.</span></span>
<span data-ttu-id="b2e5b-142">Per creare, vedere la sezione NOTE per le proprietà OSPROFILE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-142">To construct, see NOTES section for OSPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e5b-143">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="b2e5b-143">-PackageUrl</span></span>
<span data-ttu-id="b2e5b-144">Specifica un URL che fa riferimento alla posizione del pacchetto del servizio nel servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-144">Specifies a URL that refers to the location of the service package in the Blob service.</span></span>
<span data-ttu-id="b2e5b-145">L'URL del pacchetto del servizio può essere UN URI della firma di accesso condiviso da qualsiasi account di archiviazione. Si tratta di una proprietà di sola scrittura e non viene restituita nelle chiamate GET.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-145">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

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

### <span data-ttu-id="b2e5b-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e5b-146">-ResourceGroupName</span></span>
<span data-ttu-id="b2e5b-147">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-147">Name of the resource group.</span></span>

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

### <span data-ttu-id="b2e5b-148">-RoleProfile</span><span class="sxs-lookup"><span data-stu-id="b2e5b-148">-RoleProfile</span></span>
<span data-ttu-id="b2e5b-149">Descrive il profilo del ruolo per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-149">Describes the role profile for the cloud service.</span></span>
<span data-ttu-id="b2e5b-150">Per creare, vedere la sezione NOTE per le proprietà ROLEPROFILE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-150">To construct, see NOTES section for ROLEPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceRoleProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e5b-151">-StartCloudService</span><span class="sxs-lookup"><span data-stu-id="b2e5b-151">-StartCloudService</span></span>
<span data-ttu-id="b2e5b-152">(Facoltativo) Indica se avviare il servizio cloud immediatamente dopo la sua creazione.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-152">(Optional) Indicates whether to start the cloud service immediately after it is created.</span></span>
<span data-ttu-id="b2e5b-153">Il valore predefinito è `true` . Se false, il modello di servizio è ancora distribuito, ma il codice non viene eseguito immediatamente.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-153">The default value is `true`.If false, the service model is still deployed, but the code is not run immediately.</span></span>
<span data-ttu-id="b2e5b-154">Il servizio è invece PoweredOff fino a quando non si chiama Start, in corrispondenza del quale verrà avviato il servizio.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-154">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span>
<span data-ttu-id="b2e5b-155">Un servizio distribuito continua a sostenere addebiti, anche se con tecnologia poweredoff.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-155">A deployed service still incurs charges, even if it is poweredoff.</span></span>

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

### <span data-ttu-id="b2e5b-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b2e5b-156">-SubscriptionId</span></span>
<span data-ttu-id="b2e5b-157">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b2e5b-158">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-158">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b2e5b-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2e5b-159">-Tag</span></span>
<span data-ttu-id="b2e5b-160">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-160">Resource tags.</span></span>

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

### <span data-ttu-id="b2e5b-161">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="b2e5b-161">-UpgradeMode</span></span>
<span data-ttu-id="b2e5b-162">Modalità di aggiornamento per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-162">Update mode for the cloud service.</span></span>
<span data-ttu-id="b2e5b-163">Le istanze del ruolo vengono allocate per aggiornare i domini durante la distribuzione del servizio.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-163">Role instances are allocated to update domains when the service is deployed.</span></span>
<span data-ttu-id="b2e5b-164">Gli aggiornamenti possono essere avviati manualmente in ogni dominio di aggiornamento o avviati automaticamente in tutti i domini di aggiornamento. I valori possibili \<br /\> \<br /\> **sono** \<br /\> \<br /\> **manuali e** \<br /\> \<br /\> **simultanei se** non sono \<br /\> \<br /\> specificati, il valore predefinito è Auto. Se impostato su Manuale, è necessario chiamare PUT UpdateDomain per applicare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-164">Updates can be initiated manually in each update domain or initiated automatically in all update domains.Possible Values are \<br /\>\<br /\>**Auto**\<br /\>\<br /\>**Manual** \<br /\>\<br /\>**Simultaneous**\<br /\>\<br /\>If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span>
<span data-ttu-id="b2e5b-165">Se impostato su Auto, l'aggiornamento viene applicato automaticamente a ogni dominio di aggiornamento in sequenza.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-165">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.CloudServiceUpgradeMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e5b-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2e5b-166">-Confirm</span></span>
<span data-ttu-id="b2e5b-167">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2e5b-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2e5b-168">-WhatIf</span></span>
<span data-ttu-id="b2e5b-169">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2e5b-170">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2e5b-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e5b-171">CommonParameters</span></span>
<span data-ttu-id="b2e5b-172">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e5b-173">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e5b-174">INPUT</span><span class="sxs-lookup"><span data-stu-id="b2e5b-174">INPUTS</span></span>

## <span data-ttu-id="b2e5b-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2e5b-175">OUTPUTS</span></span>

### <span data-ttu-id="b2e5b-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="b2e5b-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="b2e5b-177">NOTE</span><span class="sxs-lookup"><span data-stu-id="b2e5b-177">NOTES</span></span>

<span data-ttu-id="b2e5b-178">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b2e5b-178">ALIASES</span></span>

<span data-ttu-id="b2e5b-179">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b2e5b-179">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b2e5b-180">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-180">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b2e5b-181">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-181">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b2e5b-182"><ICloudServiceExtensionProfile>EXTENSIONPROFILE: descrive un profilo dell'estensione del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-182">EXTENSIONPROFILE <ICloudServiceExtensionProfile>: Describes a cloud service extension profile.</span></span>
  - <span data-ttu-id="b2e5b-183">`[Extension <IExtension[]>]`: elenco delle estensioni per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-183">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
    - <span data-ttu-id="b2e5b-184">`[AutoUpgradeMinorVersion <Boolean?>]`: specificare in modo esplicito se la piattaforma può aggiornare automaticamente typeHandlerVersion alle versioni secondarie successive quando diventano disponibili.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
    - <span data-ttu-id="b2e5b-185">`[ForceUpdateTag <String>]`: tag per forzare l'applicazione delle impostazioni pubbliche e protette fornite.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-185">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="b2e5b-186">La modifica del valore del tag consente di eseguire di nuovo l'estensione senza modificare le impostazioni pubbliche o protette.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-186">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="b2e5b-187">Se forceUpdateTag non viene modificato, gli aggiornamenti alle impostazioni pubbliche o protette verranno comunque applicati dal gestore.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-187">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="b2e5b-188">Se né forceUpdateTag né le impostazioni pubbliche o protette vengono modificate, il flusso dell'estensione all'istanza del ruolo viene eseguito con lo stesso numero di sequenza e l'implementazione può essere eseguita di nuovo o meno</span><span class="sxs-lookup"><span data-stu-id="b2e5b-188">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
    - <span data-ttu-id="b2e5b-189">`[Name <String>]`: nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-189">`[Name <String>]`: The name of the extension.</span></span>
    - <span data-ttu-id="b2e5b-190">`[ProtectedSetting <String>]`: impostazioni protette per l'estensione, crittografate prima dell'invio all'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-190">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
    - <span data-ttu-id="b2e5b-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b2e5b-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
    - <span data-ttu-id="b2e5b-192">`[Publisher <String>]`: nome dell'autore del gestore estensioni.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-192">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
    - <span data-ttu-id="b2e5b-193">`[RolesAppliedTo <String[]>]`: elenco facoltativo di ruoli per l'applicazione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-193">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="b2e5b-194">Se non si specifica la proprietà o si specifica "\*", l'estensione viene applicata a tutti i ruoli nel servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-194">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
    - <span data-ttu-id="b2e5b-195">`[Setting <String>]`: impostazioni pubbliche per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-195">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="b2e5b-196">Per le estensioni JSON, si tratta delle impostazioni JSON per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-196">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="b2e5b-197">Per l'estensione XML, ad esempio RDP, si tratta dell'impostazione XML per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-197">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
    - <span data-ttu-id="b2e5b-198">`[SourceVaultId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="b2e5b-198">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="b2e5b-199">`[Type <String>]`: specifica il tipo dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-199">`[Type <String>]`: Specifies the type of the extension.</span></span>
    - <span data-ttu-id="b2e5b-200">`[TypeHandlerVersion <String>]`: specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-200">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="b2e5b-201">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-201">Specifies the version of the extension.</span></span> <span data-ttu-id="b2e5b-202">Se questo elemento non viene specificato o come valore viene usato un asterisco (\*), viene usata la versione più recente dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-202">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="b2e5b-203">Se il valore viene specificato con un numero di versione principale e un asterisco come numero di versione secondaria (X.), viene selezionata l'ultima versione secondaria della versione principale specificata.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-203">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="b2e5b-204">Se si specifica un numero di versione principale e un numero di versione secondaria (X.Y), viene selezionata la versione dell'estensione specifica.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-204">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="b2e5b-205">Se si specifica una versione, viene eseguito un aggiornamento automatico sull'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-205">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>

<span data-ttu-id="b2e5b-206"><ICloudServiceNetworkProfile>NETWORKPROFILE: profilo di rete per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-206">NETWORKPROFILE <ICloudServiceNetworkProfile>: Network Profile for the cloud service.</span></span>
  - <span data-ttu-id="b2e5b-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: elenco di configurazioni di bilanciamento del carico per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
    - <span data-ttu-id="b2e5b-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: elenco di indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="b2e5b-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
      - <span data-ttu-id="b2e5b-209">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b2e5b-209">`[Name <String>]`:</span></span> 
      - <span data-ttu-id="b2e5b-210">`[PrivateIPAddress <String>]`: l'indirizzo IP privato a cui fa riferimento il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-210">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
      - <span data-ttu-id="b2e5b-211">`[PublicIPAddressId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="b2e5b-211">`[PublicIPAddressId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="b2e5b-212">`[SubnetId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="b2e5b-212">`[SubnetId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="b2e5b-213">`[Name <String>]`: nome risorsa</span><span class="sxs-lookup"><span data-stu-id="b2e5b-213">`[Name <String>]`: Resource Name</span></span>
  - <span data-ttu-id="b2e5b-214">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="b2e5b-214">`[SwappableCloudService <ISubResource>]`:</span></span> 
    - <span data-ttu-id="b2e5b-215">`[Id <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="b2e5b-215">`[Id <String>]`: Resource Id</span></span>

<span data-ttu-id="b2e5b-216">OSPROFILE: <ICloudServiceOSProfile> descrive il profilo del sistema operativo per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-216">OSPROFILE <ICloudServiceOSProfile>: Describes the OS profile for the cloud service.</span></span>
  - <span data-ttu-id="b2e5b-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: specifica il set di certificati da installare nelle istanze del ruolo.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
    - <span data-ttu-id="b2e5b-218">`[SourceVaultId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="b2e5b-218">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="b2e5b-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: elenco dei riferimenti a vault chiave in SourceVault che contengono certificati.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
      - <span data-ttu-id="b2e5b-220">`[CertificateUrl <String>]`: URL di un certificato che è stato caricato come segreto nel Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-220">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

<span data-ttu-id="b2e5b-221"><ICloudServiceRoleProfile>ROLEPROFILE: descrive il profilo del ruolo per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-221">ROLEPROFILE <ICloudServiceRoleProfile>: Describes the role profile for the cloud service.</span></span>
  - <span data-ttu-id="b2e5b-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: elenco dei ruoli per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
    - <span data-ttu-id="b2e5b-223">`[Name <String>]`: nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-223">`[Name <String>]`: Resource name.</span></span>
    - <span data-ttu-id="b2e5b-224">`[SkuCapacity <Int64?>]`: specifica il numero di istanze di ruoli nel servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-224">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
    - <span data-ttu-id="b2e5b-225">`[SkuName <String>]`: nome della SKU.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-225">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="b2e5b-226">NOTA: se il nuovo SKU non è supportato nell'hardware in cui è attualmente in esecuzione il servizio cloud, è necessario eliminare e ricreare il servizio cloud o tornare alla SKU precedente.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-226">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
    - <span data-ttu-id="b2e5b-227">`[SkuTier <String>]`: specifica il livello del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-227">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="b2e5b-228">I valori possibili sono</span><span class="sxs-lookup"><span data-stu-id="b2e5b-228">Possible Values are</span></span> <br /><br /> <span data-ttu-id="b2e5b-229">**Standard**</span><span class="sxs-lookup"><span data-stu-id="b2e5b-229">**Standard**</span></span> <br /><br /> <span data-ttu-id="b2e5b-230">**Di base**</span><span class="sxs-lookup"><span data-stu-id="b2e5b-230">**Basic**</span></span>

## <span data-ttu-id="b2e5b-231">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2e5b-231">RELATED LINKS</span></span>

