---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 32e3bc6419ef94b177a06735654844d09ea04f3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199922"
---
# <span data-ttu-id="91bb9-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="91bb9-101">New-AzApiManagement</span></span>

## <span data-ttu-id="91bb9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91bb9-102">SYNOPSIS</span></span>
<span data-ttu-id="91bb9-103">Crea una distribuzione di gestione API.</span><span class="sxs-lookup"><span data-stu-id="91bb9-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="91bb9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91bb9-104">SYNTAX</span></span>

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

## <span data-ttu-id="91bb9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91bb9-105">DESCRIPTION</span></span>
<span data-ttu-id="91bb9-106">Il cmdlet **New-AzApiManagement** crea una distribuzione di gestione delle API in Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="91bb9-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="91bb9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91bb9-107">EXAMPLES</span></span>

### <span data-ttu-id="91bb9-108">Esempio 1: creare un servizio di gestione API Tier per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="91bb9-108">Example 1: Create a Developer tier API Management service</span></span>
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

<span data-ttu-id="91bb9-109">Questo comando crea un servizio di gestione delle API di livello per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="91bb9-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="91bb9-110">Il comando specifica l'organizzazione e l'indirizzo di amministratore.</span><span class="sxs-lookup"><span data-stu-id="91bb9-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="91bb9-111">Il comando non specifica il parametro *SKU* .</span><span class="sxs-lookup"><span data-stu-id="91bb9-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="91bb9-112">Il cmdlet usa quindi il valore predefinito di Developer.</span><span class="sxs-lookup"><span data-stu-id="91bb9-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="91bb9-113">Esempio 2: creare un servizio a livello standard con tre unità</span><span class="sxs-lookup"><span data-stu-id="91bb9-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="91bb9-114">Questo comando crea un servizio di gestione delle API di livello standard con tre unità.</span><span class="sxs-lookup"><span data-stu-id="91bb9-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="91bb9-115">Esempio 3: creare un servizio a livello di consumo</span><span class="sxs-lookup"><span data-stu-id="91bb9-115">Example 3: Create a Consumption tier service</span></span>
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

<span data-ttu-id="91bb9-116">Questo comando crea un servizio di gestione delle API di livello consumer con il certificato client abilitato in Europa occidentale.</span><span class="sxs-lookup"><span data-stu-id="91bb9-116">This command creates a consumption tier API Management service with Client Certificate enabled in west Europe.</span></span>

### <span data-ttu-id="91bb9-117">Esempio 4: creare un servizio di gestione delle API per una rete virtuale esterna</span><span class="sxs-lookup"><span data-stu-id="91bb9-117">Example 4: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="91bb9-118">Questo comando crea un servizio di gestione API di livello superiore in una subnet di rete virtuale di Azure con un endpoint gateway esterno con un'area master in West US.</span><span class="sxs-lookup"><span data-stu-id="91bb9-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="91bb9-119">Esempio 5: creare un servizio di gestione delle API per una rete virtuale interna</span><span class="sxs-lookup"><span data-stu-id="91bb9-119">Example 5: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="91bb9-120">Questo comando crea un servizio di gestione delle API di livello superiore in una subnet di rete virtuale di Azure con un endpoint gateway interno con un'area master in West US.</span><span class="sxs-lookup"><span data-stu-id="91bb9-120">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="91bb9-121">Esempio 6: creare un servizio di gestione delle API e abilitare il protocollo TLS 1,0</span><span class="sxs-lookup"><span data-stu-id="91bb9-121">Example 6: Create an API Management service and Enable TLS 1.0 protocol</span></span>
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

<span data-ttu-id="91bb9-122">Questo comando crea un servizio di gestione delle API SKU standard e consente a TLS 1,0 sul client frontend di ApiManagement gateway e client back-end tra gateway e backend di ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="91bb9-122">This command creates a Standard SKU Api Management service and Enable TLS 1.0 on Frontend client to ApiManagement Gateway and Backend client between ApiManagement Gateway and Backend.</span></span>

## <span data-ttu-id="91bb9-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91bb9-123">PARAMETERS</span></span>

### <span data-ttu-id="91bb9-124">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="91bb9-124">-AdditionalRegions</span></span>
<span data-ttu-id="91bb9-125">Aree di distribuzione aggiuntive della gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="91bb9-125">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="91bb9-126">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="91bb9-126">-AdminEmail</span></span>
<span data-ttu-id="91bb9-127">Specifica l'indirizzo di posta elettronica di origine per tutte le notifiche inviate dal sistema di gestione API.</span><span class="sxs-lookup"><span data-stu-id="91bb9-127">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="91bb9-128">-Capacità</span><span class="sxs-lookup"><span data-stu-id="91bb9-128">-Capacity</span></span>
<span data-ttu-id="91bb9-129">Specifica la capacità SKU del servizio di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="91bb9-129">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="91bb9-130">Il valore predefinito è uno (1).</span><span class="sxs-lookup"><span data-stu-id="91bb9-130">The default is one (1).</span></span>

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

### <span data-ttu-id="91bb9-131">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="91bb9-131">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="91bb9-132">Configurazioni hostname personalizzate.</span><span class="sxs-lookup"><span data-stu-id="91bb9-132">Custom hostname configurations.</span></span> <span data-ttu-id="91bb9-133">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="91bb9-133">Default value is $null.</span></span> <span data-ttu-id="91bb9-134">Passando $null verrà impostato il nome host predefinito.</span><span class="sxs-lookup"><span data-stu-id="91bb9-134">Passing $null will set the default hostname.</span></span>

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

### <span data-ttu-id="91bb9-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91bb9-135">-DefaultProfile</span></span>
<span data-ttu-id="91bb9-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91bb9-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91bb9-137">-EnableClientCertificate</span><span class="sxs-lookup"><span data-stu-id="91bb9-137">-EnableClientCertificate</span></span>
<span data-ttu-id="91bb9-138">Il contrassegno deve essere usato solo per il servizio ApiManagement SKU di consumo.</span><span class="sxs-lookup"><span data-stu-id="91bb9-138">Flag only meant to be used for Consumption SKU ApiManagement Service.</span></span> <span data-ttu-id="91bb9-139">In questo articolo viene applicato un certificato client per ogni richiesta al gateway.</span><span class="sxs-lookup"><span data-stu-id="91bb9-139">This enforces a client certificate to be presented on each request to the gateway.</span></span> <span data-ttu-id="91bb9-140">In questo modo è anche possibile eseguire l'autenticazione del certificato nei criteri del gateway.</span><span class="sxs-lookup"><span data-stu-id="91bb9-140">This also enables the ability to authenticate the certificate in the policy on the gateway.</span></span>

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

### <span data-ttu-id="91bb9-141">-Posizione</span><span class="sxs-lookup"><span data-stu-id="91bb9-141">-Location</span></span>
<span data-ttu-id="91bb9-142">Specifica il percorso per creare il servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="91bb9-142">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="91bb9-143">Per ottenere posizioni valide, usare il cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | dove {$ _. ResourceTypes [0]. ResourceTypeName-EQ "servizio"} | Posizioni Select-Object</span><span class="sxs-lookup"><span data-stu-id="91bb9-143">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="91bb9-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="91bb9-144">-Name</span></span>
<span data-ttu-id="91bb9-145">Specifica un nome per la distribuzione della gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="91bb9-145">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="91bb9-146">-Organizzazione</span><span class="sxs-lookup"><span data-stu-id="91bb9-146">-Organization</span></span>
<span data-ttu-id="91bb9-147">Specifica il nome di un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="91bb9-147">Specifies the name of an organization.</span></span>
<span data-ttu-id="91bb9-148">Gestione API usa questo indirizzo nel portale per sviluppatori nelle notifiche tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="91bb9-148">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="91bb9-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91bb9-149">-ResourceGroupName</span></span>
<span data-ttu-id="91bb9-150">Specifica il nome del gruppo di risorse in cui questo cmdlet crea una distribuzione di gestione API.</span><span class="sxs-lookup"><span data-stu-id="91bb9-150">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="91bb9-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="91bb9-151">-Sku</span></span>
<span data-ttu-id="91bb9-152">Specifica il livello del servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="91bb9-152">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="91bb9-153">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="91bb9-153">Valid values are:</span></span> 
- <span data-ttu-id="91bb9-154">Sviluppo</span><span class="sxs-lookup"><span data-stu-id="91bb9-154">Developer</span></span> 
- <span data-ttu-id="91bb9-155">Standard</span><span class="sxs-lookup"><span data-stu-id="91bb9-155">Standard</span></span> 
- <span data-ttu-id="91bb9-156">Premium l'impostazione predefinita è Developer.</span><span class="sxs-lookup"><span data-stu-id="91bb9-156">Premium The default is Developer.</span></span>

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

### <span data-ttu-id="91bb9-157">-SslSetting</span><span class="sxs-lookup"><span data-stu-id="91bb9-157">-SslSetting</span></span>
<span data-ttu-id="91bb9-158">L'impostazione SSL del servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="91bb9-158">The Ssl Setting of the ApiManagement Service.</span></span> <span data-ttu-id="91bb9-159">Il valore predefinito è $null</span><span class="sxs-lookup"><span data-stu-id="91bb9-159">Default value is $null</span></span>

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

### <span data-ttu-id="91bb9-160">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="91bb9-160">-SystemAssignedIdentity</span></span>
<span data-ttu-id="91bb9-161">Genera e assegna un'identità di Azure Active Directory per questo server per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="91bb9-161">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="91bb9-162">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="91bb9-162">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="91bb9-163">I certificati emessi da CA interna devono essere installati nel servizio.</span><span class="sxs-lookup"><span data-stu-id="91bb9-163">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="91bb9-164">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="91bb9-164">Default value is $null.</span></span>

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

### <span data-ttu-id="91bb9-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="91bb9-165">-Tag</span></span>
<span data-ttu-id="91bb9-166">Dizionario di tag.</span><span class="sxs-lookup"><span data-stu-id="91bb9-166">Tags dictionary.</span></span>

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

### <span data-ttu-id="91bb9-167">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="91bb9-167">-UserAssignedIdentity</span></span>
<span data-ttu-id="91bb9-168">Assegnare le identità utente a questo server per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="91bb9-168">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="91bb9-169">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="91bb9-169">-VirtualNetwork</span></span>
<span data-ttu-id="91bb9-170">Configurazione della rete virtuale dell'area di distribuzione di gestione API di Azure master.</span><span class="sxs-lookup"><span data-stu-id="91bb9-170">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="91bb9-171">-VpnType</span><span class="sxs-lookup"><span data-stu-id="91bb9-171">-VpnType</span></span>
<span data-ttu-id="91bb9-172">Tipo di rete virtuale della distribuzione di ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="91bb9-172">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="91bb9-173">I valori validi sono</span><span class="sxs-lookup"><span data-stu-id="91bb9-173">Valid Values are</span></span> 
- <span data-ttu-id="91bb9-174">"None" (valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="91bb9-174">"None" (Default Value.</span></span> <span data-ttu-id="91bb9-175">ApiManagement non fa parte di una rete virtuale ")</span><span class="sxs-lookup"><span data-stu-id="91bb9-175">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="91bb9-176">"Esterno" (la distribuzione di ApiManagement è configurato all'interno di una rete virtuale con un endpoint di fronte Internet)</span><span class="sxs-lookup"><span data-stu-id="91bb9-176">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="91bb9-177">"Internal" (la distribuzione di ApiManagement è configurato all'interno di una rete virtuale con endpoint di fronte alla Intranet)</span><span class="sxs-lookup"><span data-stu-id="91bb9-177">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="91bb9-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91bb9-178">CommonParameters</span></span>
<span data-ttu-id="91bb9-179">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91bb9-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91bb9-180">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91bb9-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91bb9-181">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91bb9-181">INPUTS</span></span>

### <span data-ttu-id="91bb9-182">System. String</span><span class="sxs-lookup"><span data-stu-id="91bb9-182">System.String</span></span>

### <span data-ttu-id="91bb9-183">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="91bb9-183">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="91bb9-184">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="91bb9-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="91bb9-185">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="91bb9-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="91bb9-186">System. Collections. Generic. Dictionary ' 2 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e], [System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="91bb9-186">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="91bb9-187">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion []</span><span class="sxs-lookup"><span data-stu-id="91bb9-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="91bb9-188">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCustomHostNameConfiguration []</span><span class="sxs-lookup"><span data-stu-id="91bb9-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="91bb9-189">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSystemCertificate []</span><span class="sxs-lookup"><span data-stu-id="91bb9-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="91bb9-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91bb9-190">OUTPUTS</span></span>

### <span data-ttu-id="91bb9-191">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="91bb9-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="91bb9-192">Note</span><span class="sxs-lookup"><span data-stu-id="91bb9-192">NOTES</span></span>

## <span data-ttu-id="91bb9-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91bb9-193">RELATED LINKS</span></span>

[<span data-ttu-id="91bb9-194">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="91bb9-194">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="91bb9-195">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="91bb9-195">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="91bb9-196">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="91bb9-196">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="91bb9-197">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="91bb9-197">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="91bb9-198">Ripristinare-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="91bb9-198">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


