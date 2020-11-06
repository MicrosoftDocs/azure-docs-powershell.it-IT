---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: 62400acbb9fb70f05772bd9749e39e3d7d62cc62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515832"
---
# <span data-ttu-id="746fe-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="746fe-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="746fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="746fe-102">SYNOPSIS</span></span>
<span data-ttu-id="746fe-103">Aggiorna la distribuzione di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="746fe-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="746fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="746fe-104">SYNTAX</span></span>

### <span data-ttu-id="746fe-105">UpdateSpecificService (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="746fe-105">UpdateSpecificService (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="746fe-106">UpdateFromPsApiManagementInstance</span><span class="sxs-lookup"><span data-stu-id="746fe-106">UpdateFromPsApiManagementInstance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="746fe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="746fe-107">DESCRIPTION</span></span>
<span data-ttu-id="746fe-108">Il cmdlet **Update-AzureRmApiManagementDeployment** aggiorna le distribuzioni correnti di un servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="746fe-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="746fe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="746fe-109">EXAMPLES</span></span>

### <span data-ttu-id="746fe-110">Esempio 1: aggiornare una distribuzione di un'istanza di ApiManagement</span><span class="sxs-lookup"><span data-stu-id="746fe-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="746fe-111">Questo comando Aggiorna la distribuzione di un'istanza di gestione delle API in uno standard di capacità di tre unità.</span><span class="sxs-lookup"><span data-stu-id="746fe-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="746fe-112">Esempio 2: ottenere un'istanza di ApiManagement e ridimensionarla</span><span class="sxs-lookup"><span data-stu-id="746fe-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="746fe-113">Questo esempio ottiene un'istanza di gestione delle API, la bilancia in cinque unità Premium e quindi aggiunge altre tre unità all'area Premium.</span><span class="sxs-lookup"><span data-stu-id="746fe-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="746fe-114">Esempio 3: aggiornamento della distribuzione (VNET esterno)</span><span class="sxs-lookup"><span data-stu-id="746fe-114">Example 3: Update deployment (external VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="746fe-115">Questo comando aggiorna una distribuzione di gestione delle API esistente e si unisce a un *VpnType* esterno.</span><span class="sxs-lookup"><span data-stu-id="746fe-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="746fe-116">Esempio 4: aggiornamento della distribuzione (VNET interno)</span><span class="sxs-lookup"><span data-stu-id="746fe-116">Example 4: Update deployment (internal VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="746fe-117">Questo comando aggiorna una distribuzione di gestione delle API esistente e si unisce a un *VpnType* interno.</span><span class="sxs-lookup"><span data-stu-id="746fe-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="746fe-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="746fe-118">PARAMETERS</span></span>

### <span data-ttu-id="746fe-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="746fe-119">-AdditionalRegions</span></span>
<span data-ttu-id="746fe-120">Specifica aree di distribuzione aggiuntive della gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="746fe-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: UpdateSpecificService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="746fe-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="746fe-121">-ApiManagement</span></span>
<span data-ttu-id="746fe-122">Specifica l'istanza di **PsApiManagement** da cui ottenere la configurazione di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="746fe-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="746fe-123">Usa questo parametro se l'istanza contiene già tutte le modifiche necessarie.</span><span class="sxs-lookup"><span data-stu-id="746fe-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: UpdateFromPsApiManagementInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="746fe-124">-Capacità</span><span class="sxs-lookup"><span data-stu-id="746fe-124">-Capacity</span></span>
<span data-ttu-id="746fe-125">Specifica la capacità SKU dell'area di distribuzione di gestione API di Azure master.</span><span class="sxs-lookup"><span data-stu-id="746fe-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: Int32
Parameter Sets: UpdateSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="746fe-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="746fe-126">-DefaultProfile</span></span>
<span data-ttu-id="746fe-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="746fe-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="746fe-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="746fe-128">-Location</span></span>
<span data-ttu-id="746fe-129">Specifica la posizione dell'area di distribuzione della gestione delle API master.</span><span class="sxs-lookup"><span data-stu-id="746fe-129">Specifies the location of the master API Management deployment region.</span></span>

<span data-ttu-id="746fe-130">Per ottenere posizioni valide, usare il cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | dove {$ _. ResourceTypes [0]. ResourceTypeName-EQ "servizio"} | Posizioni Select-Object</span><span class="sxs-lookup"><span data-stu-id="746fe-130">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: UpdateSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="746fe-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="746fe-131">-Name</span></span>
<span data-ttu-id="746fe-132">Specifica il nome della gestione delle API che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="746fe-132">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: UpdateSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="746fe-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="746fe-133">-PassThru</span></span>
<span data-ttu-id="746fe-134">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="746fe-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="746fe-135">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="746fe-135">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="746fe-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="746fe-136">-ResourceGroupName</span></span>
<span data-ttu-id="746fe-137">Specifica il nome del gruppo di risorse in cui è presente la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="746fe-137">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: String
Parameter Sets: UpdateSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="746fe-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="746fe-138">-Sku</span></span>
<span data-ttu-id="746fe-139">Specifica il livello dell'area di distribuzione di gestione API di Azure master.</span><span class="sxs-lookup"><span data-stu-id="746fe-139">Specifies the tier of the master Azure API Management deployment region.</span></span>

<span data-ttu-id="746fe-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="746fe-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="746fe-141">Sviluppo</span><span class="sxs-lookup"><span data-stu-id="746fe-141">Developer</span></span>
- <span data-ttu-id="746fe-142">Standard</span><span class="sxs-lookup"><span data-stu-id="746fe-142">Standard</span></span>
- <span data-ttu-id="746fe-143">Premium</span><span class="sxs-lookup"><span data-stu-id="746fe-143">Premium</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: UpdateSpecificService
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="746fe-144">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="746fe-144">-VirtualNetwork</span></span>
<span data-ttu-id="746fe-145">Specifica la configurazione della rete virtuale dell'area di distribuzione di gestione API di Azure master.</span><span class="sxs-lookup"><span data-stu-id="746fe-145">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: UpdateSpecificService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="746fe-146">-VpnType</span><span class="sxs-lookup"><span data-stu-id="746fe-146">-VpnType</span></span>
<span data-ttu-id="746fe-147">Specifica il tipo di rete virtuale della distribuzione della gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="746fe-147">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="746fe-148">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="746fe-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="746fe-149">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="746fe-149">None.</span></span>
<span data-ttu-id="746fe-150">La distribuzione della gestione delle API non fa parte di una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="746fe-150">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="746fe-151">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="746fe-151">This is the default value.</span></span> 
- <span data-ttu-id="746fe-152">Esterno.</span><span class="sxs-lookup"><span data-stu-id="746fe-152">External.</span></span>
<span data-ttu-id="746fe-153">La distribuzione della gestione delle API ha un indirizzo virtuale con rivestimento esterno.</span><span class="sxs-lookup"><span data-stu-id="746fe-153">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="746fe-154">Interno.</span><span class="sxs-lookup"><span data-stu-id="746fe-154">Internal.</span></span>
<span data-ttu-id="746fe-155">La distribuzione della gestione delle API include un indirizzo virtuale di Intranet.</span><span class="sxs-lookup"><span data-stu-id="746fe-155">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: PsApiManagementVpnType
Parameter Sets: UpdateSpecificService
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="746fe-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="746fe-156">CommonParameters</span></span>
<span data-ttu-id="746fe-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="746fe-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="746fe-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="746fe-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="746fe-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="746fe-159">INPUTS</span></span>

### <span data-ttu-id="746fe-160">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="746fe-160">PsApiManagement</span></span>
<span data-ttu-id="746fe-161">Il parametro ' ApiManagement ' accetta il valore di tipo ' PsApiManagement ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="746fe-161">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="746fe-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="746fe-162">OUTPUTS</span></span>

### <span data-ttu-id="746fe-163">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="746fe-163">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="746fe-164">Note</span><span class="sxs-lookup"><span data-stu-id="746fe-164">NOTES</span></span>

## <span data-ttu-id="746fe-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="746fe-165">RELATED LINKS</span></span>

[<span data-ttu-id="746fe-166">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="746fe-166">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


