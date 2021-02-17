---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 32e3bc6419ef94b177a06735654844d09ea04f3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192495"
---
# <span data-ttu-id="42873-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="42873-101">New-AzApiManagement</span></span>

## <span data-ttu-id="42873-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42873-102">SYNOPSIS</span></span>
<span data-ttu-id="42873-103">Crea una distribuzione di Gestione API.</span><span class="sxs-lookup"><span data-stu-id="42873-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="42873-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42873-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>]
 [-SslSetting <PsApiManagementSslSetting>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-EnableClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42873-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="42873-105">DESCRIPTION</span></span>
<span data-ttu-id="42873-106">Il cmdlet **New-AzApiManagement crea** una distribuzione di Gestione API in Gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="42873-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="42873-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42873-107">EXAMPLES</span></span>

### <span data-ttu-id="42873-108">Esempio 1: Creare un servizio di gestione API di livello sviluppatore</span><span class="sxs-lookup"><span data-stu-id="42873-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS D:\> New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi2" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"


PublicIPAddresses                     : {104.43.240.65}
PrivateIPAddresses                    :
Id                                    : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/ContosoGroup02/providers/Microsoft.ApiManagement/service/ContosoApi2
Name                                  : ContosoApi2
Location                              : Central US
Sku                                   : Developer
Capacity                              : 1
CreatedTimeUtc                        : 2/24/2020 10:34:12 PM
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://contosoapi2.azure-api.net
RuntimeRegionalUrl                    : https://contosoapi2-centralus-01.regional.azure-api.net
PortalUrl                             : https://contosoapi2.portal.azure-api.net
DeveloperPortalUrl                    : https://contosoapi2.developer.azure-api.net
ManagementApiUrl                      : https://contosoapi2.management.azure-api.net
ScmUrl                                : https://contosoapi2.scm.azure-api.net
PublisherEmail                        : admin@contoso.com
OrganizationName                      : Contoso
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {contosoapi2.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : ContosoGroup02
```

<span data-ttu-id="42873-109">Questo comando crea un servizio di gestione API di livello sviluppatore.</span><span class="sxs-lookup"><span data-stu-id="42873-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="42873-110">Il comando specifica l'organizzazione e l'indirizzo dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="42873-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="42873-111">Il comando non specifica il *parametro SKU.*</span><span class="sxs-lookup"><span data-stu-id="42873-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="42873-112">Di conseguenza, il cmdlet usa il valore predefinito developer.</span><span class="sxs-lookup"><span data-stu-id="42873-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="42873-113">Esempio 2: Creare un servizio di livello Standard con tre unità</span><span class="sxs-lookup"><span data-stu-id="42873-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="42873-114">Questo comando crea un servizio di gestione API di livello standard con tre unità.</span><span class="sxs-lookup"><span data-stu-id="42873-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="42873-115">Esempio 3: Creare un servizio di livello Consumo</span><span class="sxs-lookup"><span data-stu-id="42873-115">Example 3: Create a Consumption tier service</span></span>
```powershell
PS D:\github\azure-powershell> New-AzApiManagement -ResourceGroupName Api-Default-North-Europe -Name consumptionskuservice -Location 'West Europe' -Sku Consumption -Organization microsoft -AdminEmail contoso@contoso.com -SystemAssignedIdentity -EnableClientCertificate

PublicIPAddresses                     :
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-North-Europe/providers/Microsoft.ApiManagement/service/consumptionskuservice
Name                                  : consumptionskuservice
Location                              : West Europe
Sku                                   : Consumption
Capacity                              : 0
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://consumptionskuservice.azure-api.net
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {consumptionskuservice.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity
EnableClientCertificate               : True
ResourceGroupName                     : Api-Default-North-Europe
```

<span data-ttu-id="42873-116">Questo comando crea un servizio di gestione API di livello a consumo con certificato client abilitato nell'Europa occidentale.</span><span class="sxs-lookup"><span data-stu-id="42873-116">This command creates a consumption tier API Management service with Client Certificate enabled in west Europe.</span></span>

### <span data-ttu-id="42873-117">Esempio 4: Creare un servizio di gestione API per una rete virtuale esterna</span><span class="sxs-lookup"><span data-stu-id="42873-117">Example 4: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="42873-118">Questo comando crea un servizio di gestione API a livello superiore in una subnet di rete virtuale di Azure con un endpoint gateway per l'esterno e un'area master negli Stati Uniti occidentali.</span><span class="sxs-lookup"><span data-stu-id="42873-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="42873-119">Esempio 5: Creare un servizio di gestione API per una rete virtuale interna</span><span class="sxs-lookup"><span data-stu-id="42873-119">Example 5: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="42873-120">Questo comando crea un servizio di gestione API a livello superiore in una subnet di rete virtuale di Azure che ha un endpoint gateway per uso interno con un'area master negli Stati Uniti occidentali.</span><span class="sxs-lookup"><span data-stu-id="42873-120">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="42873-121">Esempio 6: Creare un servizio di gestione DELLE API e abilitare il protocollo TLS 1.0</span><span class="sxs-lookup"><span data-stu-id="42873-121">Example 6: Create an API Management service and Enable TLS 1.0 protocol</span></span>
```powershell
PS C:\> $enableTls=@{"Tls10" = "True"}
PS C:\> $sslSetting = New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls
PS C:\> New-AzApiManagement -ResourceGroupName Api-Default-CentralUS -Name "testtlspowershell" -Sku Standard -Location "CentralUS" -Organization "Microsoft" -AdminEmail "bar@contoso.com" -SslSetting $sslSetting

PublicIPAddresses                     : {23.99.140.18}
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-CentralUS/providers/Microsoft.ApiManagement/service/testtlspowershell
Name                                  : testtlspowershell
Location                              : Central US
Sku                                   : Standard
Capacity                              : 1
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://testtlspowershell.azure-api.net
RuntimeRegionalUrl                    : https://testtlspowershell-centralus-01.regional.azure-api.net
PortalUrl                             : https://testtlspowershell.portal.azure-api.net
ManagementApiUrl                      : https://testtlspowershell.management.azure-api.net
ScmUrl                                : https://testtlspowershell.scm.azure-api.net
PublisherEmail                        : bar@contoso.com
OrganizationName                      : Microsoft
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {testtlspowershell.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : Api-Default-CentralUS
```

<span data-ttu-id="42873-122">Questo comando crea un servizio di gestione api SKU standard e abilita TLS 1.0 nel client Frontend al gateway ApiManagement e al client Backend tra gateway ApiManagement e back-end.</span><span class="sxs-lookup"><span data-stu-id="42873-122">This command creates a Standard SKU Api Management service and Enable TLS 1.0 on Frontend client to ApiManagement Gateway and Backend client between ApiManagement Gateway and Backend.</span></span>

## <span data-ttu-id="42873-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42873-123">PARAMETERS</span></span>

### <span data-ttu-id="42873-124">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="42873-124">-AdditionalRegions</span></span>
<span data-ttu-id="42873-125">Altre aree di distribuzione di Gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="42873-125">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42873-126">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="42873-126">-AdminEmail</span></span>
<span data-ttu-id="42873-127">Specifica l'indirizzo di posta elettronica di origine per tutte le notifiche inviate dal sistema di gestione DELLE API.</span><span class="sxs-lookup"><span data-stu-id="42873-127">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42873-128">-Capacità</span><span class="sxs-lookup"><span data-stu-id="42873-128">-Capacity</span></span>
<span data-ttu-id="42873-129">Specifica la capacità di SKU del servizio di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="42873-129">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="42873-130">L'impostazione predefinita è 1 (1).</span><span class="sxs-lookup"><span data-stu-id="42873-130">The default is one (1).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42873-131">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="42873-131">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="42873-132">Configurazioni di nomi host personalizzati.</span><span class="sxs-lookup"><span data-stu-id="42873-132">Custom hostname configurations.</span></span> <span data-ttu-id="42873-133">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="42873-133">Default value is $null.</span></span> <span data-ttu-id="42873-134">Passando $null, viene impostato il nome host predefinito.</span><span class="sxs-lookup"><span data-stu-id="42873-134">Passing $null will set the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42873-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42873-135">-DefaultProfile</span></span>
<span data-ttu-id="42873-136">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42873-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42873-137">-EnableClientCertificate</span><span class="sxs-lookup"><span data-stu-id="42873-137">-EnableClientCertificate</span></span>
<span data-ttu-id="42873-138">Contrassegno da usare solo per il servizio ApiManagement di SKU di consumo.</span><span class="sxs-lookup"><span data-stu-id="42873-138">Flag only meant to be used for Consumption SKU ApiManagement Service.</span></span> <span data-ttu-id="42873-139">In questo modo viene applicato un certificato client da presentare a ogni richiesta al gateway.</span><span class="sxs-lookup"><span data-stu-id="42873-139">This enforces a client certificate to be presented on each request to the gateway.</span></span> <span data-ttu-id="42873-140">In questo modo è anche possibile autenticare il certificato nei criteri del gateway.</span><span class="sxs-lookup"><span data-stu-id="42873-140">This also enables the ability to authenticate the certificate in the policy on the gateway.</span></span>

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

### <span data-ttu-id="42873-141">-Location</span><span class="sxs-lookup"><span data-stu-id="42873-141">-Location</span></span>
<span data-ttu-id="42873-142">Specifica la posizione in cui creare il servizio di gestione api.</span><span class="sxs-lookup"><span data-stu-id="42873-142">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="42873-143">Per ottenere posizioni valide, usare il cmdlet Get-AzResourceProvider -ProviderManagement "Microsoft.ApiManagement" | dove {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object percorsi</span><span class="sxs-lookup"><span data-stu-id="42873-143">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42873-144">-Name</span><span class="sxs-lookup"><span data-stu-id="42873-144">-Name</span></span>
<span data-ttu-id="42873-145">Specifica un nome per la distribuzione di Gestione API.</span><span class="sxs-lookup"><span data-stu-id="42873-145">Specifies a name for the API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42873-146">-Organizzazione</span><span class="sxs-lookup"><span data-stu-id="42873-146">-Organization</span></span>
<span data-ttu-id="42873-147">Specifica il nome di un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="42873-147">Specifies the name of an organization.</span></span>
<span data-ttu-id="42873-148">Gestione API usa questo indirizzo nel portale di sviluppo nelle notifiche tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="42873-148">API Management uses this address in the developer portal in email notifications.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42873-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42873-149">-ResourceGroupName</span></span>
<span data-ttu-id="42873-150">Specifica il nome del gruppo di risorse in cui questo cmdlet crea una distribuzione di Gestione API.</span><span class="sxs-lookup"><span data-stu-id="42873-150">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42873-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="42873-151">-Sku</span></span>
<span data-ttu-id="42873-152">Specifica il livello del servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="42873-152">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="42873-153">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="42873-153">Valid values are:</span></span> 
- <span data-ttu-id="42873-154">Sviluppatore</span><span class="sxs-lookup"><span data-stu-id="42873-154">Developer</span></span> 
- <span data-ttu-id="42873-155">Standard</span><span class="sxs-lookup"><span data-stu-id="42873-155">Standard</span></span> 
- <span data-ttu-id="42873-156">Premium L'impostazione predefinita è Sviluppatore.</span><span class="sxs-lookup"><span data-stu-id="42873-156">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42873-157">-SslSetting</span><span class="sxs-lookup"><span data-stu-id="42873-157">-SslSetting</span></span>
<span data-ttu-id="42873-158">Impostazione Ssl del servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="42873-158">The Ssl Setting of the ApiManagement Service.</span></span> <span data-ttu-id="42873-159">Il valore predefinito è $null</span><span class="sxs-lookup"><span data-stu-id="42873-159">Default value is $null</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42873-160">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="42873-160">-SystemAssignedIdentity</span></span>
<span data-ttu-id="42873-161">Generare e assegnare un'identità di Azure Active Directory per questo server per l'uso con servizi di gestione delle chiavi come Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="42873-161">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="42873-162">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="42873-162">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="42873-163">Certificati emessi dalla CA interna per l'installazione nel servizio.</span><span class="sxs-lookup"><span data-stu-id="42873-163">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="42873-164">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="42873-164">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42873-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="42873-165">-Tag</span></span>
<span data-ttu-id="42873-166">Dizionario di tag.</span><span class="sxs-lookup"><span data-stu-id="42873-166">Tags dictionary.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42873-167">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="42873-167">-UserAssignedIdentity</span></span>
<span data-ttu-id="42873-168">Assegnare identità utente a questo server per l'uso con servizi di gestione delle chiavi come Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="42873-168">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42873-169">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="42873-169">-VirtualNetwork</span></span>
<span data-ttu-id="42873-170">Configurazione di rete virtuale dell'area di distribuzione principale di Gestione API Azure.</span><span class="sxs-lookup"><span data-stu-id="42873-170">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42873-171">-VpnType</span><span class="sxs-lookup"><span data-stu-id="42873-171">-VpnType</span></span>
<span data-ttu-id="42873-172">Tipo di rete virtuale della distribuzione ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="42873-172">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="42873-173">I valori validi sono</span><span class="sxs-lookup"><span data-stu-id="42873-173">Valid Values are</span></span> 
- <span data-ttu-id="42873-174">"Nessuno" (valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="42873-174">"None" (Default Value.</span></span> <span data-ttu-id="42873-175">ApiManagement non fa parte di alcuna rete virtuale")</span><span class="sxs-lookup"><span data-stu-id="42873-175">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="42873-176">"Esterno" (la distribuzione di ApiManagement viene impostata all'interno di una rete virtuale che ha un endpoint internet)</span><span class="sxs-lookup"><span data-stu-id="42873-176">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="42873-177">"Interno" (la distribuzione di ApiManagement viene impostata all'interno di una rete virtuale che ha un endpoint rivolto alla Intranet)</span><span class="sxs-lookup"><span data-stu-id="42873-177">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42873-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42873-178">CommonParameters</span></span>
<span data-ttu-id="42873-179">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42873-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42873-180">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="42873-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42873-181">INPUT</span><span class="sxs-lookup"><span data-stu-id="42873-181">INPUTS</span></span>

### <span data-ttu-id="42873-182">System.String</span><span class="sxs-lookup"><span data-stu-id="42873-182">System.String</span></span>

### <span data-ttu-id="42873-183">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="42873-183">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="42873-184">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="42873-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="42873-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="42873-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="42873-186">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="42873-186">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="42873-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span><span class="sxs-lookup"><span data-stu-id="42873-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="42873-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="42873-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="42873-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span><span class="sxs-lookup"><span data-stu-id="42873-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="42873-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42873-190">OUTPUTS</span></span>

### <span data-ttu-id="42873-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="42873-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="42873-192">NOTE</span><span class="sxs-lookup"><span data-stu-id="42873-192">NOTES</span></span>

## <span data-ttu-id="42873-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42873-193">RELATED LINKS</span></span>

[<span data-ttu-id="42873-194">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="42873-194">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="42873-195">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="42873-195">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="42873-196">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="42873-196">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="42873-197">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="42873-197">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="42873-198">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="42873-198">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


