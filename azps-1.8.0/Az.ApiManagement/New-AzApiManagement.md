---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 43393995fcc370e2b3ff2b20586ab696c39d059b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673614"
---
# <span data-ttu-id="b8d85-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b8d85-101">New-AzApiManagement</span></span>

## <span data-ttu-id="b8d85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b8d85-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d85-103">Crea una distribuzione di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b8d85-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="b8d85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8d85-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8d85-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8d85-105">DESCRIPTION</span></span>
<span data-ttu-id="b8d85-106">Il cmdlet **New-AzApiManagement** crea una distribuzione di gestione delle API in Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="b8d85-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="b8d85-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8d85-107">EXAMPLES</span></span>

### <span data-ttu-id="b8d85-108">Esempio 1: creare un servizio di gestione API Tier per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="b8d85-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="b8d85-109">Questo comando crea un servizio di gestione delle API di livello per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="b8d85-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="b8d85-110">Il comando specifica l'organizzazione e l'indirizzo di amministratore.</span><span class="sxs-lookup"><span data-stu-id="b8d85-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="b8d85-111">Il comando non specifica il parametro *SKU* .</span><span class="sxs-lookup"><span data-stu-id="b8d85-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="b8d85-112">Il cmdlet usa quindi il valore predefinito di Developer.</span><span class="sxs-lookup"><span data-stu-id="b8d85-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="b8d85-113">Esempio 2: creare un servizio a livello standard con tre unità</span><span class="sxs-lookup"><span data-stu-id="b8d85-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="b8d85-114">Questo comando crea un servizio di gestione delle API di livello standard con tre unità.</span><span class="sxs-lookup"><span data-stu-id="b8d85-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="b8d85-115">Esempio 3: creare un servizio di gestione delle API per una rete virtuale esterna</span><span class="sxs-lookup"><span data-stu-id="b8d85-115">Example 3: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="b8d85-116">Questo comando crea un servizio di gestione API di livello superiore in una subnet di rete virtuale di Azure con un endpoint gateway esterno con un'area master in West US.</span><span class="sxs-lookup"><span data-stu-id="b8d85-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="b8d85-117">Esempio 4: creare un servizio di gestione delle API per una rete virtuale interna</span><span class="sxs-lookup"><span data-stu-id="b8d85-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="b8d85-118">Questo comando crea un servizio di gestione delle API di livello superiore in una subnet di rete virtuale di Azure con un endpoint gateway interno con un'area master in West US.</span><span class="sxs-lookup"><span data-stu-id="b8d85-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="b8d85-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b8d85-119">PARAMETERS</span></span>

### <span data-ttu-id="b8d85-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="b8d85-120">-AdditionalRegions</span></span>
<span data-ttu-id="b8d85-121">Aree di distribuzione aggiuntive della gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d85-121">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="b8d85-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="b8d85-122">-AdminEmail</span></span>
<span data-ttu-id="b8d85-123">Specifica l'indirizzo di posta elettronica di origine per tutte le notifiche inviate dal sistema di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b8d85-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="b8d85-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b8d85-124">-AssignIdentity</span></span>
<span data-ttu-id="b8d85-125">Genera e assegna un'identità di Azure Active Directory per questo server per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="b8d85-125">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="b8d85-126">-Capacità</span><span class="sxs-lookup"><span data-stu-id="b8d85-126">-Capacity</span></span>
<span data-ttu-id="b8d85-127">Specifica la capacità SKU del servizio di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d85-127">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="b8d85-128">Il valore predefinito è uno (1).</span><span class="sxs-lookup"><span data-stu-id="b8d85-128">The default is one (1).</span></span>

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

### <span data-ttu-id="b8d85-129">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8d85-129">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="b8d85-130">Configurazioni hostname personalizzate.</span><span class="sxs-lookup"><span data-stu-id="b8d85-130">Custom hostname configurations.</span></span> <span data-ttu-id="b8d85-131">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="b8d85-131">Default value is $null.</span></span> <span data-ttu-id="b8d85-132">Passando $null verrà impostato il nome host predefinito.</span><span class="sxs-lookup"><span data-stu-id="b8d85-132">Passing $null will set the default hostname.</span></span>

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

### <span data-ttu-id="b8d85-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d85-133">-DefaultProfile</span></span>
<span data-ttu-id="b8d85-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d85-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8d85-135">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b8d85-135">-Location</span></span>
<span data-ttu-id="b8d85-136">Specifica il percorso per creare il servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="b8d85-136">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="b8d85-137">Per ottenere posizioni valide, usare il cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | dove {$ _. ResourceTypes [0]. ResourceTypeName-EQ "servizio"} | Posizioni Select-Object</span><span class="sxs-lookup"><span data-stu-id="b8d85-137">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="b8d85-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8d85-138">-Name</span></span>
<span data-ttu-id="b8d85-139">Specifica un nome per la distribuzione della gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="b8d85-139">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="b8d85-140">-Organizzazione</span><span class="sxs-lookup"><span data-stu-id="b8d85-140">-Organization</span></span>
<span data-ttu-id="b8d85-141">Specifica il nome di un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b8d85-141">Specifies the name of an organization.</span></span>
<span data-ttu-id="b8d85-142">Gestione API usa questo indirizzo nel portale per sviluppatori nelle notifiche tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b8d85-142">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="b8d85-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8d85-143">-ResourceGroupName</span></span>
<span data-ttu-id="b8d85-144">Specifica il nome del gruppo di risorse in cui questo cmdlet crea una distribuzione di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b8d85-144">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="b8d85-145">-SKU</span><span class="sxs-lookup"><span data-stu-id="b8d85-145">-Sku</span></span>
<span data-ttu-id="b8d85-146">Specifica il livello del servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="b8d85-146">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="b8d85-147">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b8d85-147">Valid values are:</span></span> 
- <span data-ttu-id="b8d85-148">Sviluppo</span><span class="sxs-lookup"><span data-stu-id="b8d85-148">Developer</span></span> 
- <span data-ttu-id="b8d85-149">Standard</span><span class="sxs-lookup"><span data-stu-id="b8d85-149">Standard</span></span> 
- <span data-ttu-id="b8d85-150">Premium l'impostazione predefinita è Developer.</span><span class="sxs-lookup"><span data-stu-id="b8d85-150">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d85-151">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8d85-151">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="b8d85-152">I certificati emessi da CA interna devono essere installati nel servizio.</span><span class="sxs-lookup"><span data-stu-id="b8d85-152">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="b8d85-153">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="b8d85-153">Default value is $null.</span></span>

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

### <span data-ttu-id="b8d85-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="b8d85-154">-Tag</span></span>
<span data-ttu-id="b8d85-155">Dizionario di tag.</span><span class="sxs-lookup"><span data-stu-id="b8d85-155">Tags dictionary.</span></span>

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

### <span data-ttu-id="b8d85-156">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b8d85-156">-VirtualNetwork</span></span>
<span data-ttu-id="b8d85-157">Configurazione della rete virtuale dell'area di distribuzione di gestione API di Azure master.</span><span class="sxs-lookup"><span data-stu-id="b8d85-157">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="b8d85-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="b8d85-158">-VpnType</span></span>
<span data-ttu-id="b8d85-159">Tipo di rete virtuale della distribuzione di ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b8d85-159">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="b8d85-160">I valori validi sono</span><span class="sxs-lookup"><span data-stu-id="b8d85-160">Valid Values are</span></span> 
- <span data-ttu-id="b8d85-161">"None" (valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b8d85-161">"None" (Default Value.</span></span> <span data-ttu-id="b8d85-162">ApiManagement non fa parte di una rete virtuale ")</span><span class="sxs-lookup"><span data-stu-id="b8d85-162">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="b8d85-163">"Esterno" (la distribuzione di ApiManagement è configurato all'interno di una rete virtuale con un endpoint di fronte Internet)</span><span class="sxs-lookup"><span data-stu-id="b8d85-163">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="b8d85-164">"Internal" (la distribuzione di ApiManagement è configurato all'interno di una rete virtuale con endpoint di fronte alla Intranet)</span><span class="sxs-lookup"><span data-stu-id="b8d85-164">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="b8d85-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d85-165">CommonParameters</span></span>
<span data-ttu-id="b8d85-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8d85-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d85-167">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8d85-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d85-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b8d85-168">INPUTS</span></span>

### <span data-ttu-id="b8d85-169">System. String</span><span class="sxs-lookup"><span data-stu-id="b8d85-169">System.String</span></span>

### <span data-ttu-id="b8d85-170">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b8d85-170">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="b8d85-171">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b8d85-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b8d85-172">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b8d85-172">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="b8d85-173">System. Collections. Generic. Dictionary ' 2 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e], [System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b8d85-173">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b8d85-174">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion []</span><span class="sxs-lookup"><span data-stu-id="b8d85-174">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="b8d85-175">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCustomHostNameConfiguration []</span><span class="sxs-lookup"><span data-stu-id="b8d85-175">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="b8d85-176">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSystemCertificate []</span><span class="sxs-lookup"><span data-stu-id="b8d85-176">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="b8d85-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8d85-177">OUTPUTS</span></span>

### <span data-ttu-id="b8d85-178">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b8d85-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b8d85-179">Note</span><span class="sxs-lookup"><span data-stu-id="b8d85-179">NOTES</span></span>

## <span data-ttu-id="b8d85-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8d85-180">RELATED LINKS</span></span>

[<span data-ttu-id="b8d85-181">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b8d85-181">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="b8d85-182">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b8d85-182">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="b8d85-183">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b8d85-183">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="b8d85-184">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b8d85-184">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="b8d85-185">Ripristinare-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b8d85-185">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


