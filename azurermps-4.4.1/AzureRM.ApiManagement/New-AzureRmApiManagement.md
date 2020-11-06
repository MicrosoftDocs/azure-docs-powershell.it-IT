---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: 82e09e146999ce0bd320ba398ab2f196f1115688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517240"
---
# <span data-ttu-id="b66fd-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b66fd-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="b66fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b66fd-102">SYNOPSIS</span></span>
<span data-ttu-id="b66fd-103">Crea una distribuzione di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b66fd-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b66fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b66fd-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b66fd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b66fd-105">DESCRIPTION</span></span>
<span data-ttu-id="b66fd-106">Il cmdlet **New-AzureRmApiManagement** crea una distribuzione di gestione delle API in Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="b66fd-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="b66fd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b66fd-107">EXAMPLES</span></span>

### <span data-ttu-id="b66fd-108">Esempio 1: creare un servizio di gestione API Tier per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="b66fd-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="b66fd-109">Questo comando crea un servizio di gestione delle API di livello per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="b66fd-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="b66fd-110">Il comando specifica l'organizzazione e l'indirizzo di amministratore.</span><span class="sxs-lookup"><span data-stu-id="b66fd-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="b66fd-111">Il comando non specifica il parametro *SKU* .</span><span class="sxs-lookup"><span data-stu-id="b66fd-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="b66fd-112">Il cmdlet usa quindi il valore predefinito di Developer.</span><span class="sxs-lookup"><span data-stu-id="b66fd-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="b66fd-113">Esempio 2: creare un servizio a livello standard con tre unità</span><span class="sxs-lookup"><span data-stu-id="b66fd-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="b66fd-114">Questo comando crea un servizio di gestione delle API di livello standard con tre unità.</span><span class="sxs-lookup"><span data-stu-id="b66fd-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="b66fd-115">Esempio 3: creare un servizio di gestione delle API per una rete virtuale esterna</span><span class="sxs-lookup"><span data-stu-id="b66fd-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="b66fd-116">Questo comando crea un servizio di gestione API di livello superiore in una subnet di rete virtuale di Azure con un endpoint gateway esterno con un'area master in West US.</span><span class="sxs-lookup"><span data-stu-id="b66fd-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="b66fd-117">Esempio 4: creare un servizio di gestione delle API per una rete virtuale interna</span><span class="sxs-lookup"><span data-stu-id="b66fd-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="b66fd-118">Questo comando crea un servizio di gestione delle API di livello superiore in una subnet di rete virtuale di Azure con un endpoint gateway interno con un'area master in West US.</span><span class="sxs-lookup"><span data-stu-id="b66fd-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="b66fd-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b66fd-119">PARAMETERS</span></span>

### <span data-ttu-id="b66fd-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="b66fd-120">-AdditionalRegions</span></span>
<span data-ttu-id="b66fd-121">Aree di distribuzione aggiuntive della gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="b66fd-121">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="b66fd-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="b66fd-122">-AdminEmail</span></span>
<span data-ttu-id="b66fd-123">Specifica l'indirizzo di posta elettronica di origine per tutte le notifiche inviate dal sistema di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b66fd-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="b66fd-124">-Capacità</span><span class="sxs-lookup"><span data-stu-id="b66fd-124">-Capacity</span></span>
<span data-ttu-id="b66fd-125">Specifica la capacità SKU del servizio di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="b66fd-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="b66fd-126">Il valore predefinito è uno (1).</span><span class="sxs-lookup"><span data-stu-id="b66fd-126">The default is one (1).</span></span>

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

### <span data-ttu-id="b66fd-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b66fd-127">-Location</span></span>
<span data-ttu-id="b66fd-128">Specifica la posizione in cui questo cmdlet crea una distribuzione di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b66fd-128">Specifies the location in which this cmdlet creates an API Management deployment.</span></span>
<span data-ttu-id="b66fd-129">Per ottenere posizioni valide, usare i cmdlet Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="b66fd-129">To obtain valid locations, use the Get-AzureLocation cmdlets.</span></span>

<span data-ttu-id="b66fd-130">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b66fd-130">Valid values are:</span></span> 

- <span data-ttu-id="b66fd-131">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="b66fd-131">North Central US</span></span>
- <span data-ttu-id="b66fd-132">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="b66fd-132">South Central US</span></span>
- <span data-ttu-id="b66fd-133">Stati Uniti centrali</span><span class="sxs-lookup"><span data-stu-id="b66fd-133">Central US</span></span>
- <span data-ttu-id="b66fd-134">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="b66fd-134">West Europe</span></span>
- <span data-ttu-id="b66fd-135">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="b66fd-135">North Europe</span></span>
- <span data-ttu-id="b66fd-136">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="b66fd-136">West US</span></span>
- <span data-ttu-id="b66fd-137">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="b66fd-137">East US</span></span>
- <span data-ttu-id="b66fd-138">Stati Uniti Est 2</span><span class="sxs-lookup"><span data-stu-id="b66fd-138">East US 2</span></span>
- <span data-ttu-id="b66fd-139">Giappone est</span><span class="sxs-lookup"><span data-stu-id="b66fd-139">Japan East</span></span>
- <span data-ttu-id="b66fd-140">Giappone ovest</span><span class="sxs-lookup"><span data-stu-id="b66fd-140">Japan West</span></span>
- <span data-ttu-id="b66fd-141">Brasile sud</span><span class="sxs-lookup"><span data-stu-id="b66fd-141">Brazil South</span></span>
- <span data-ttu-id="b66fd-142">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="b66fd-142">Southeast Asia</span></span>
- <span data-ttu-id="b66fd-143">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="b66fd-143">East Asia</span></span>
- <span data-ttu-id="b66fd-144">Australia Est</span><span class="sxs-lookup"><span data-stu-id="b66fd-144">Australia East</span></span>
- <span data-ttu-id="b66fd-145">Australia sud-est</span><span class="sxs-lookup"><span data-stu-id="b66fd-145">Australia Southeast</span></span>

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

### <span data-ttu-id="b66fd-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="b66fd-146">-Name</span></span>
<span data-ttu-id="b66fd-147">Specifica un nome per la distribuzione della gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="b66fd-147">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="b66fd-148">-Organizzazione</span><span class="sxs-lookup"><span data-stu-id="b66fd-148">-Organization</span></span>
<span data-ttu-id="b66fd-149">Specifica il nome di un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b66fd-149">Specifies the name of an organization.</span></span>
<span data-ttu-id="b66fd-150">Gestione API usa questo indirizzo nel portale per sviluppatori nelle notifiche tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b66fd-150">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="b66fd-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b66fd-151">-ResourceGroupName</span></span>
<span data-ttu-id="b66fd-152">Specifica il nome del gruppo di risorse in cui questo cmdlet crea una distribuzione di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b66fd-152">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="b66fd-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="b66fd-153">-Sku</span></span>
<span data-ttu-id="b66fd-154">Specifica il livello del servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="b66fd-154">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="b66fd-155">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b66fd-155">Valid values are:</span></span> 

- <span data-ttu-id="b66fd-156">Sviluppo</span><span class="sxs-lookup"><span data-stu-id="b66fd-156">Developer</span></span> 
- <span data-ttu-id="b66fd-157">Standard</span><span class="sxs-lookup"><span data-stu-id="b66fd-157">Standard</span></span> 
- <span data-ttu-id="b66fd-158">Premium</span><span class="sxs-lookup"><span data-stu-id="b66fd-158">Premium</span></span> 

<span data-ttu-id="b66fd-159">Il valore predefinito è Developer.</span><span class="sxs-lookup"><span data-stu-id="b66fd-159">The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b66fd-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="b66fd-160">-Tags</span></span>
<span data-ttu-id="b66fd-161">Specifica un dizionario di tag.</span><span class="sxs-lookup"><span data-stu-id="b66fd-161">Specifies a dictionary of tags.</span></span>

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

### <span data-ttu-id="b66fd-162">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b66fd-162">-VirtualNetwork</span></span>
<span data-ttu-id="b66fd-163">Configurazione della rete virtuale dell'area di distribuzione di gestione API di Azure master.</span><span class="sxs-lookup"><span data-stu-id="b66fd-163">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="b66fd-164">-VpnType</span><span class="sxs-lookup"><span data-stu-id="b66fd-164">-VpnType</span></span>
<span data-ttu-id="b66fd-165">Tipo di rete virtuale della distribuzione di ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b66fd-165">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="b66fd-166">I valori validi sono</span><span class="sxs-lookup"><span data-stu-id="b66fd-166">Valid Values are</span></span> 
- <span data-ttu-id="b66fd-167">"None" (valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b66fd-167">"None" (Default Value.</span></span> <span data-ttu-id="b66fd-168">ApiManagement non fa parte di una rete virtuale ")</span><span class="sxs-lookup"><span data-stu-id="b66fd-168">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="b66fd-169">"Esterno" (la distribuzione di ApiManagement è configurato all'interno di una rete virtuale con un endpoint di fronte Internet)</span><span class="sxs-lookup"><span data-stu-id="b66fd-169">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="b66fd-170">"Internal" (la distribuzione di ApiManagement è configurato all'interno di una rete virtuale con endpoint di fronte alla Intranet)</span><span class="sxs-lookup"><span data-stu-id="b66fd-170">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="b66fd-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b66fd-171">-DefaultProfile</span></span>
<span data-ttu-id="b66fd-172">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b66fd-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b66fd-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b66fd-173">CommonParameters</span></span>
<span data-ttu-id="b66fd-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b66fd-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b66fd-175">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b66fd-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b66fd-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b66fd-176">INPUTS</span></span>

## <span data-ttu-id="b66fd-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b66fd-177">OUTPUTS</span></span>

### <span data-ttu-id="b66fd-178">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b66fd-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b66fd-179">Note</span><span class="sxs-lookup"><span data-stu-id="b66fd-179">NOTES</span></span>

## <span data-ttu-id="b66fd-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b66fd-180">RELATED LINKS</span></span>

[<span data-ttu-id="b66fd-181">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b66fd-181">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="b66fd-182">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b66fd-182">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="b66fd-183">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b66fd-183">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="b66fd-184">Ripristinare-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b66fd-184">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


