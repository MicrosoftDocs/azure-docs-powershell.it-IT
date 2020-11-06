---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: ebf95d8e809731bdca2f288bc09054fd14353686
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521116"
---
# <span data-ttu-id="b6790-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6790-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="b6790-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6790-102">SYNOPSIS</span></span>
<span data-ttu-id="b6790-103">Crea una distribuzione di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b6790-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6790-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6790-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6790-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6790-105">DESCRIPTION</span></span>
<span data-ttu-id="b6790-106">Il cmdlet **New-AzureRmApiManagement** crea una distribuzione di gestione delle API in Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="b6790-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="b6790-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6790-107">EXAMPLES</span></span>

### <span data-ttu-id="b6790-108">Esempio 1: creare un servizio di gestione API Tier per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="b6790-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="b6790-109">Questo comando crea un servizio di gestione delle API di livello per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="b6790-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="b6790-110">Il comando specifica l'organizzazione e l'indirizzo di amministratore.</span><span class="sxs-lookup"><span data-stu-id="b6790-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="b6790-111">Il comando non specifica il parametro *SKU* .</span><span class="sxs-lookup"><span data-stu-id="b6790-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="b6790-112">Il cmdlet usa quindi il valore predefinito di Developer.</span><span class="sxs-lookup"><span data-stu-id="b6790-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="b6790-113">Esempio 2: creare un servizio a livello standard con tre unità</span><span class="sxs-lookup"><span data-stu-id="b6790-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="b6790-114">Questo comando crea un servizio di gestione delle API di livello standard con tre unità.</span><span class="sxs-lookup"><span data-stu-id="b6790-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="b6790-115">Esempio 3: creare un servizio di gestione delle API per una rete virtuale esterna</span><span class="sxs-lookup"><span data-stu-id="b6790-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="b6790-116">Questo comando crea un servizio di gestione API di livello superiore in una subnet di rete virtuale di Azure con un endpoint gateway esterno con un'area master in West US.</span><span class="sxs-lookup"><span data-stu-id="b6790-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="b6790-117">Esempio 4: creare un servizio di gestione delle API per una rete virtuale interna</span><span class="sxs-lookup"><span data-stu-id="b6790-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="b6790-118">Questo comando crea un servizio di gestione delle API di livello superiore in una subnet di rete virtuale di Azure con un endpoint gateway interno con un'area master in West US.</span><span class="sxs-lookup"><span data-stu-id="b6790-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="b6790-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6790-119">PARAMETERS</span></span>

### <span data-ttu-id="b6790-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="b6790-120">-AdditionalRegions</span></span>
<span data-ttu-id="b6790-121">Aree di distribuzione aggiuntive della gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6790-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6790-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="b6790-122">-AdminEmail</span></span>
<span data-ttu-id="b6790-123">Specifica l'indirizzo di posta elettronica di origine per tutte le notifiche inviate dal sistema di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b6790-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6790-124">-Capacità</span><span class="sxs-lookup"><span data-stu-id="b6790-124">-Capacity</span></span>
<span data-ttu-id="b6790-125">Specifica la capacità SKU del servizio di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6790-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="b6790-126">Il valore predefinito è uno (1).</span><span class="sxs-lookup"><span data-stu-id="b6790-126">The default is one (1).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6790-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6790-127">-DefaultProfile</span></span>
<span data-ttu-id="b6790-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6790-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6790-129">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b6790-129">-Location</span></span>
<span data-ttu-id="b6790-130">Specifica il percorso per creare il servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="b6790-130">Specifies the location to create the Api Management service.</span></span>

<span data-ttu-id="b6790-131">Per ottenere posizioni valide, usare il cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | dove {$ _. ResourceTypes [0]. ResourceTypeName-EQ "servizio"} | Posizioni Select-Object</span><span class="sxs-lookup"><span data-stu-id="b6790-131">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6790-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6790-132">-Name</span></span>
<span data-ttu-id="b6790-133">Specifica un nome per la distribuzione della gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="b6790-133">Specifies a name for the API Management deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6790-134">-Organizzazione</span><span class="sxs-lookup"><span data-stu-id="b6790-134">-Organization</span></span>
<span data-ttu-id="b6790-135">Specifica il nome di un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b6790-135">Specifies the name of an organization.</span></span>
<span data-ttu-id="b6790-136">Gestione API usa questo indirizzo nel portale per sviluppatori nelle notifiche tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b6790-136">API Management uses this address in the developer portal in email notifications.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6790-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6790-137">-ResourceGroupName</span></span>
<span data-ttu-id="b6790-138">Specifica il nome del gruppo di risorse in cui questo cmdlet crea una distribuzione di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b6790-138">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6790-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="b6790-139">-Sku</span></span>
<span data-ttu-id="b6790-140">Specifica il livello del servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="b6790-140">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="b6790-141">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b6790-141">Valid values are:</span></span> 

- <span data-ttu-id="b6790-142">Sviluppo</span><span class="sxs-lookup"><span data-stu-id="b6790-142">Developer</span></span> 
- <span data-ttu-id="b6790-143">Standard</span><span class="sxs-lookup"><span data-stu-id="b6790-143">Standard</span></span> 
- <span data-ttu-id="b6790-144">Premium</span><span class="sxs-lookup"><span data-stu-id="b6790-144">Premium</span></span> 

<span data-ttu-id="b6790-145">Il valore predefinito è Developer.</span><span class="sxs-lookup"><span data-stu-id="b6790-145">The default is Developer.</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6790-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6790-146">-Tag</span></span>
<span data-ttu-id="b6790-147">Dizionario di tag.</span><span class="sxs-lookup"><span data-stu-id="b6790-147">Tags dictionary.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6790-148">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b6790-148">-VirtualNetwork</span></span>
<span data-ttu-id="b6790-149">Configurazione della rete virtuale dell'area di distribuzione di gestione API di Azure master.</span><span class="sxs-lookup"><span data-stu-id="b6790-149">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6790-150">-VpnType</span><span class="sxs-lookup"><span data-stu-id="b6790-150">-VpnType</span></span>
<span data-ttu-id="b6790-151">Tipo di rete virtuale della distribuzione di ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b6790-151">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="b6790-152">I valori validi sono</span><span class="sxs-lookup"><span data-stu-id="b6790-152">Valid Values are</span></span> 
- <span data-ttu-id="b6790-153">"None" (valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b6790-153">"None" (Default Value.</span></span> <span data-ttu-id="b6790-154">ApiManagement non fa parte di una rete virtuale ")</span><span class="sxs-lookup"><span data-stu-id="b6790-154">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="b6790-155">"Esterno" (la distribuzione di ApiManagement è configurato all'interno di una rete virtuale con un endpoint di fronte Internet)</span><span class="sxs-lookup"><span data-stu-id="b6790-155">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="b6790-156">"Internal" (la distribuzione di ApiManagement è configurato all'interno di una rete virtuale con endpoint di fronte alla Intranet)</span><span class="sxs-lookup"><span data-stu-id="b6790-156">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6790-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6790-157">CommonParameters</span></span>
<span data-ttu-id="b6790-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6790-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6790-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6790-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6790-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6790-160">INPUTS</span></span>

### <span data-ttu-id="b6790-161">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b6790-161">None</span></span>
<span data-ttu-id="b6790-162">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b6790-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b6790-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6790-163">OUTPUTS</span></span>

### <span data-ttu-id="b6790-164">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6790-164">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b6790-165">Note</span><span class="sxs-lookup"><span data-stu-id="b6790-165">NOTES</span></span>

## <span data-ttu-id="b6790-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6790-166">RELATED LINKS</span></span>

[<span data-ttu-id="b6790-167">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6790-167">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="b6790-168">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6790-168">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="b6790-169">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6790-169">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="b6790-170">Ripristinare-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6790-170">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


