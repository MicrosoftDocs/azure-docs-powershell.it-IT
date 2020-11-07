---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 489df2abd46f3ec198422991c2627804f6dc140b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676038"
---
# <span data-ttu-id="ced5e-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced5e-101">New-AzApiManagement</span></span>

## <span data-ttu-id="ced5e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ced5e-102">SYNOPSIS</span></span>
<span data-ttu-id="ced5e-103">Crea una distribuzione di gestione API.</span><span class="sxs-lookup"><span data-stu-id="ced5e-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="ced5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ced5e-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>]
 [-SslSetting <PsApiManagementSslSetting>] [-AssignIdentity] [-EnableClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ced5e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ced5e-105">DESCRIPTION</span></span>
<span data-ttu-id="ced5e-106">Il cmdlet **New-AzApiManagement** crea una distribuzione di gestione delle API in Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="ced5e-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="ced5e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ced5e-107">EXAMPLES</span></span>

### <span data-ttu-id="ced5e-108">Esempio 1: creare un servizio di gestione API Tier per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="ced5e-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="ced5e-109">Questo comando crea un servizio di gestione delle API di livello per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="ced5e-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="ced5e-110">Il comando specifica l'organizzazione e l'indirizzo di amministratore.</span><span class="sxs-lookup"><span data-stu-id="ced5e-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="ced5e-111">Il comando non specifica il parametro *SKU* .</span><span class="sxs-lookup"><span data-stu-id="ced5e-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="ced5e-112">Il cmdlet usa quindi il valore predefinito di Developer.</span><span class="sxs-lookup"><span data-stu-id="ced5e-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="ced5e-113">Esempio 2: creare un servizio a livello standard con tre unità</span><span class="sxs-lookup"><span data-stu-id="ced5e-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="ced5e-114">Questo comando crea un servizio di gestione delle API di livello standard con tre unità.</span><span class="sxs-lookup"><span data-stu-id="ced5e-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="ced5e-115">Esempio 3: creare un servizio a livello di consumo</span><span class="sxs-lookup"><span data-stu-id="ced5e-115">Example 3: Create a Consumption tier service</span></span>
```powershell
PS D:\github\azure-powershell> New-AzApiManagement -ResourceGroupName Api-Default-North-Europe -Name consumptionskuservice -Location 'West Europe' -Sku Consumption -Organization microsoft -AdminEmail contoso@contoso.com -AssignIdentity -EnableClientCertificate

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

<span data-ttu-id="ced5e-116">Questo comando crea un servizio di gestione delle API di livello consumer con il certificato client abilitato in Europa occidentale.</span><span class="sxs-lookup"><span data-stu-id="ced5e-116">This command creates a consumption tier API Management service with Client Certificate enabled in west Europe.</span></span>

### <span data-ttu-id="ced5e-117">Esempio 4: creare un servizio di gestione delle API per una rete virtuale esterna</span><span class="sxs-lookup"><span data-stu-id="ced5e-117">Example 4: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="ced5e-118">Questo comando crea un servizio di gestione API di livello superiore in una subnet di rete virtuale di Azure con un endpoint gateway esterno con un'area master in West US.</span><span class="sxs-lookup"><span data-stu-id="ced5e-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="ced5e-119">Esempio 5: creare un servizio di gestione delle API per una rete virtuale interna</span><span class="sxs-lookup"><span data-stu-id="ced5e-119">Example 5: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="ced5e-120">Questo comando crea un servizio di gestione delle API di livello superiore in una subnet di rete virtuale di Azure con un endpoint gateway interno con un'area master in West US.</span><span class="sxs-lookup"><span data-stu-id="ced5e-120">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="ced5e-121">Esempio 6: creare un servizio di gestione delle API e abilitare il protocollo TLS 1,0</span><span class="sxs-lookup"><span data-stu-id="ced5e-121">Example 6: Create an API Management service and Enable TLS 1.0 protocol</span></span>
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

<span data-ttu-id="ced5e-122">Questo comando crea un servizio di gestione delle API SKU standard e consente a TLS 1,0 sul client frontend di ApiManagement gateway e client back-end tra gateway e backend di ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ced5e-122">This command creates a Standard SKU Api Management service and Enable TLS 1.0 on Frontend client to ApiManagement Gateway and Backend client between ApiManagement Gateway and Backend.</span></span>

## <span data-ttu-id="ced5e-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ced5e-123">PARAMETERS</span></span>

### <span data-ttu-id="ced5e-124">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="ced5e-124">-AdditionalRegions</span></span>
<span data-ttu-id="ced5e-125">Aree di distribuzione aggiuntive della gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="ced5e-125">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="ced5e-126">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="ced5e-126">-AdminEmail</span></span>
<span data-ttu-id="ced5e-127">Specifica l'indirizzo di posta elettronica di origine per tutte le notifiche inviate dal sistema di gestione API.</span><span class="sxs-lookup"><span data-stu-id="ced5e-127">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="ced5e-128">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ced5e-128">-AssignIdentity</span></span>
<span data-ttu-id="ced5e-129">Genera e assegna un'identità di Azure Active Directory per questo server per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="ced5e-129">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ced5e-130">-Capacità</span><span class="sxs-lookup"><span data-stu-id="ced5e-130">-Capacity</span></span>
<span data-ttu-id="ced5e-131">Specifica la capacità SKU del servizio di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="ced5e-131">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="ced5e-132">Il valore predefinito è uno (1).</span><span class="sxs-lookup"><span data-stu-id="ced5e-132">The default is one (1).</span></span>

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

### <span data-ttu-id="ced5e-133">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced5e-133">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="ced5e-134">Configurazioni hostname personalizzate.</span><span class="sxs-lookup"><span data-stu-id="ced5e-134">Custom hostname configurations.</span></span> <span data-ttu-id="ced5e-135">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="ced5e-135">Default value is $null.</span></span> <span data-ttu-id="ced5e-136">Passando $null verrà impostato il nome host predefinito.</span><span class="sxs-lookup"><span data-stu-id="ced5e-136">Passing $null will set the default hostname.</span></span>

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

### <span data-ttu-id="ced5e-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced5e-137">-DefaultProfile</span></span>
<span data-ttu-id="ced5e-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ced5e-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ced5e-139">-EnableClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ced5e-139">-EnableClientCertificate</span></span>
<span data-ttu-id="ced5e-140">Il contrassegno deve essere usato solo per il servizio ApiManagement SKU di consumo.</span><span class="sxs-lookup"><span data-stu-id="ced5e-140">Flag only meant to be used for Consumption SKU ApiManagement Service.</span></span> <span data-ttu-id="ced5e-141">In questo articolo viene applicato un certificato client per ogni richiesta al gateway.</span><span class="sxs-lookup"><span data-stu-id="ced5e-141">This enforces a client certificate to be presented on each request to the gateway.</span></span> <span data-ttu-id="ced5e-142">In questo modo è anche possibile eseguire l'autenticazione del certificato nei criteri del gateway.</span><span class="sxs-lookup"><span data-stu-id="ced5e-142">This also enables the ability to authenticate the certificate in the policy on the gateway.</span></span>

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

### <span data-ttu-id="ced5e-143">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ced5e-143">-Location</span></span>
<span data-ttu-id="ced5e-144">Specifica il percorso per creare il servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="ced5e-144">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="ced5e-145">Per ottenere posizioni valide, usare il cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | dove {$ _. ResourceTypes [0]. ResourceTypeName-EQ "servizio"} | Posizioni Select-Object</span><span class="sxs-lookup"><span data-stu-id="ced5e-145">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="ced5e-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="ced5e-146">-Name</span></span>
<span data-ttu-id="ced5e-147">Specifica un nome per la distribuzione della gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="ced5e-147">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="ced5e-148">-Organizzazione</span><span class="sxs-lookup"><span data-stu-id="ced5e-148">-Organization</span></span>
<span data-ttu-id="ced5e-149">Specifica il nome di un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="ced5e-149">Specifies the name of an organization.</span></span>
<span data-ttu-id="ced5e-150">Gestione API usa questo indirizzo nel portale per sviluppatori nelle notifiche tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="ced5e-150">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="ced5e-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ced5e-151">-ResourceGroupName</span></span>
<span data-ttu-id="ced5e-152">Specifica il nome del gruppo di risorse in cui questo cmdlet crea una distribuzione di gestione API.</span><span class="sxs-lookup"><span data-stu-id="ced5e-152">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="ced5e-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="ced5e-153">-Sku</span></span>
<span data-ttu-id="ced5e-154">Specifica il livello del servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="ced5e-154">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="ced5e-155">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="ced5e-155">Valid values are:</span></span> 
- <span data-ttu-id="ced5e-156">Sviluppo</span><span class="sxs-lookup"><span data-stu-id="ced5e-156">Developer</span></span> 
- <span data-ttu-id="ced5e-157">Standard</span><span class="sxs-lookup"><span data-stu-id="ced5e-157">Standard</span></span> 
- <span data-ttu-id="ced5e-158">Premium l'impostazione predefinita è Developer.</span><span class="sxs-lookup"><span data-stu-id="ced5e-158">Premium The default is Developer.</span></span>

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

### <span data-ttu-id="ced5e-159">-SslSetting</span><span class="sxs-lookup"><span data-stu-id="ced5e-159">-SslSetting</span></span>
<span data-ttu-id="ced5e-160">L'impostazione SSL del servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ced5e-160">The Ssl Setting of the ApiManagement Service.</span></span> <span data-ttu-id="ced5e-161">Il valore predefinito è $null</span><span class="sxs-lookup"><span data-stu-id="ced5e-161">Default value is $null</span></span>

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

### <span data-ttu-id="ced5e-162">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced5e-162">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="ced5e-163">I certificati emessi da CA interna devono essere installati nel servizio.</span><span class="sxs-lookup"><span data-stu-id="ced5e-163">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="ced5e-164">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="ced5e-164">Default value is $null.</span></span>

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

### <span data-ttu-id="ced5e-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="ced5e-165">-Tag</span></span>
<span data-ttu-id="ced5e-166">Dizionario di tag.</span><span class="sxs-lookup"><span data-stu-id="ced5e-166">Tags dictionary.</span></span>

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

### <span data-ttu-id="ced5e-167">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ced5e-167">-VirtualNetwork</span></span>
<span data-ttu-id="ced5e-168">Configurazione della rete virtuale dell'area di distribuzione di gestione API di Azure master.</span><span class="sxs-lookup"><span data-stu-id="ced5e-168">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="ced5e-169">-VpnType</span><span class="sxs-lookup"><span data-stu-id="ced5e-169">-VpnType</span></span>
<span data-ttu-id="ced5e-170">Tipo di rete virtuale della distribuzione di ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ced5e-170">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="ced5e-171">I valori validi sono</span><span class="sxs-lookup"><span data-stu-id="ced5e-171">Valid Values are</span></span> 
- <span data-ttu-id="ced5e-172">"None" (valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ced5e-172">"None" (Default Value.</span></span> <span data-ttu-id="ced5e-173">ApiManagement non fa parte di una rete virtuale ")</span><span class="sxs-lookup"><span data-stu-id="ced5e-173">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="ced5e-174">"Esterno" (la distribuzione di ApiManagement è configurato all'interno di una rete virtuale con un endpoint di fronte Internet)</span><span class="sxs-lookup"><span data-stu-id="ced5e-174">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="ced5e-175">"Internal" (la distribuzione di ApiManagement è configurato all'interno di una rete virtuale con endpoint di fronte alla Intranet)</span><span class="sxs-lookup"><span data-stu-id="ced5e-175">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="ced5e-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced5e-176">CommonParameters</span></span>
<span data-ttu-id="ced5e-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ced5e-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced5e-178">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ced5e-178">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced5e-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ced5e-179">INPUTS</span></span>

### <span data-ttu-id="ced5e-180">System. String</span><span class="sxs-lookup"><span data-stu-id="ced5e-180">System.String</span></span>

### <span data-ttu-id="ced5e-181">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ced5e-181">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ced5e-182">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ced5e-182">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ced5e-183">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ced5e-183">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="ced5e-184">System. Collections. Generic. Dictionary ' 2 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e], [System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ced5e-184">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ced5e-185">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion []</span><span class="sxs-lookup"><span data-stu-id="ced5e-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="ced5e-186">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCustomHostNameConfiguration []</span><span class="sxs-lookup"><span data-stu-id="ced5e-186">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="ced5e-187">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSystemCertificate []</span><span class="sxs-lookup"><span data-stu-id="ced5e-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="ced5e-188">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ced5e-188">OUTPUTS</span></span>

### <span data-ttu-id="ced5e-189">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced5e-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ced5e-190">Note</span><span class="sxs-lookup"><span data-stu-id="ced5e-190">NOTES</span></span>

## <span data-ttu-id="ced5e-191">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ced5e-191">RELATED LINKS</span></span>

[<span data-ttu-id="ced5e-192">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced5e-192">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="ced5e-193">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced5e-193">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="ced5e-194">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced5e-194">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="ced5e-195">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced5e-195">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="ced5e-196">Ripristinare-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced5e-196">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


