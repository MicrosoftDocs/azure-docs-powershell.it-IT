---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: e4170dbe2a1ac4ed8ad39bdb7a5db6d7174555e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508779"
---
# <span data-ttu-id="69c04-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="69c04-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="69c04-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69c04-102">SYNOPSIS</span></span>
<span data-ttu-id="69c04-103">Aggiorna la distribuzione di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="69c04-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69c04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69c04-104">SYNTAX</span></span>

### <span data-ttu-id="69c04-105">Servizio di gestione API specifico (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="69c04-105">Specific API Management service (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69c04-106">Aggiornamento dall'istanza di PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="69c04-106">Update from PsApiManagement instance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69c04-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69c04-107">DESCRIPTION</span></span>
<span data-ttu-id="69c04-108">Il cmdlet **Update-AzureRmApiManagementDeployment** aggiorna le distribuzioni correnti di un servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="69c04-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="69c04-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69c04-109">EXAMPLES</span></span>

### <span data-ttu-id="69c04-110">Esempio 1: aggiornare una distribuzione di un'istanza di ApiManagement</span><span class="sxs-lookup"><span data-stu-id="69c04-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="69c04-111">Questo comando Aggiorna la distribuzione di un'istanza di gestione delle API in uno standard di capacità di tre unità.</span><span class="sxs-lookup"><span data-stu-id="69c04-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="69c04-112">Esempio 2: ottenere un'istanza di ApiManagement e ridimensionarla</span><span class="sxs-lookup"><span data-stu-id="69c04-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="69c04-113">Questo esempio ottiene un'istanza di gestione delle API, la bilancia in cinque unità Premium e quindi aggiunge altre tre unità all'area Premium.</span><span class="sxs-lookup"><span data-stu-id="69c04-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="69c04-114">Esempio 3: aggiornamento della distribuzione (VNET esterno)</span><span class="sxs-lookup"><span data-stu-id="69c04-114">Example 3: Update deployment (external VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="69c04-115">Questo comando aggiorna una distribuzione di gestione delle API esistente e si unisce a un *VpnType* esterno.</span><span class="sxs-lookup"><span data-stu-id="69c04-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="69c04-116">Esempio 4: aggiornamento della distribuzione (VNET interno)</span><span class="sxs-lookup"><span data-stu-id="69c04-116">Example 4: Update deployment (internal VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="69c04-117">Questo comando aggiorna una distribuzione di gestione delle API esistente e si unisce a un *VpnType* interno.</span><span class="sxs-lookup"><span data-stu-id="69c04-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="69c04-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69c04-118">PARAMETERS</span></span>

### <span data-ttu-id="69c04-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="69c04-119">-AdditionalRegions</span></span>
<span data-ttu-id="69c04-120">Specifica aree di distribuzione aggiuntive della gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="69c04-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c04-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="69c04-121">-ApiManagement</span></span>
<span data-ttu-id="69c04-122">Specifica l'istanza di **PsApiManagement** da cui ottenere la configurazione di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="69c04-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="69c04-123">Usa questo parametro se l'istanza contiene già tutte le modifiche necessarie.</span><span class="sxs-lookup"><span data-stu-id="69c04-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: Update from PsApiManagement instance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69c04-124">-Capacità</span><span class="sxs-lookup"><span data-stu-id="69c04-124">-Capacity</span></span>
<span data-ttu-id="69c04-125">Specifica la capacità SKU dell'area di distribuzione di gestione API di Azure master.</span><span class="sxs-lookup"><span data-stu-id="69c04-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c04-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="69c04-126">-Location</span></span>
<span data-ttu-id="69c04-127">Specifica la posizione dell'area di distribuzione della gestione delle API master.</span><span class="sxs-lookup"><span data-stu-id="69c04-127">Specifies the location of the master API Management deployment region.</span></span>

<span data-ttu-id="69c04-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="69c04-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69c04-129">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="69c04-129">North Central US</span></span>
- <span data-ttu-id="69c04-130">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="69c04-130">South Central US</span></span>
- <span data-ttu-id="69c04-131">Stati Uniti centrali</span><span class="sxs-lookup"><span data-stu-id="69c04-131">Central US</span></span>
- <span data-ttu-id="69c04-132">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="69c04-132">West Europe</span></span>
- <span data-ttu-id="69c04-133">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="69c04-133">North Europe</span></span>
- <span data-ttu-id="69c04-134">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="69c04-134">West US</span></span>
- <span data-ttu-id="69c04-135">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="69c04-135">East US</span></span>
- <span data-ttu-id="69c04-136">Stati Uniti Est 2</span><span class="sxs-lookup"><span data-stu-id="69c04-136">East US 2</span></span>
- <span data-ttu-id="69c04-137">Giappone est</span><span class="sxs-lookup"><span data-stu-id="69c04-137">Japan East</span></span>
- <span data-ttu-id="69c04-138">Giappone ovest</span><span class="sxs-lookup"><span data-stu-id="69c04-138">Japan West</span></span>
- <span data-ttu-id="69c04-139">Brasile sud</span><span class="sxs-lookup"><span data-stu-id="69c04-139">Brazil South</span></span>
- <span data-ttu-id="69c04-140">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="69c04-140">Southeast Asia</span></span>
- <span data-ttu-id="69c04-141">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="69c04-141">East Asia</span></span>
- <span data-ttu-id="69c04-142">Australia Est</span><span class="sxs-lookup"><span data-stu-id="69c04-142">Australia East</span></span>
- <span data-ttu-id="69c04-143">Australia sud-est</span><span class="sxs-lookup"><span data-stu-id="69c04-143">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c04-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="69c04-144">-Name</span></span>
<span data-ttu-id="69c04-145">Specifica il nome della gestione delle API che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="69c04-145">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c04-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69c04-146">-PassThru</span></span>
<span data-ttu-id="69c04-147">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="69c04-147">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="69c04-148">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="69c04-148">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="69c04-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69c04-149">-ResourceGroupName</span></span>
<span data-ttu-id="69c04-150">Specifica il nome del gruppo di risorse in cui è presente la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="69c04-150">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c04-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="69c04-151">-Sku</span></span>
<span data-ttu-id="69c04-152">Specifica il livello dell'area di distribuzione di gestione API di Azure master.</span><span class="sxs-lookup"><span data-stu-id="69c04-152">Specifies the tier of the master Azure API Management deployment region.</span></span>

<span data-ttu-id="69c04-153">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="69c04-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69c04-154">Sviluppo</span><span class="sxs-lookup"><span data-stu-id="69c04-154">Developer</span></span>
- <span data-ttu-id="69c04-155">Standard</span><span class="sxs-lookup"><span data-stu-id="69c04-155">Standard</span></span>
- <span data-ttu-id="69c04-156">Premium</span><span class="sxs-lookup"><span data-stu-id="69c04-156">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c04-157">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="69c04-157">-VirtualNetwork</span></span>
<span data-ttu-id="69c04-158">Specifica la configurazione della rete virtuale dell'area di distribuzione di gestione API di Azure master.</span><span class="sxs-lookup"><span data-stu-id="69c04-158">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c04-159">-VpnType</span><span class="sxs-lookup"><span data-stu-id="69c04-159">-VpnType</span></span>
<span data-ttu-id="69c04-160">Specifica il tipo di rete virtuale della distribuzione della gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="69c04-160">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="69c04-161">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="69c04-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69c04-162">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="69c04-162">None.</span></span>
<span data-ttu-id="69c04-163">La distribuzione della gestione delle API non fa parte di una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="69c04-163">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="69c04-164">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="69c04-164">This is the default value.</span></span> 
- <span data-ttu-id="69c04-165">Esterno.</span><span class="sxs-lookup"><span data-stu-id="69c04-165">External.</span></span>
<span data-ttu-id="69c04-166">La distribuzione della gestione delle API ha un indirizzo virtuale con rivestimento esterno.</span><span class="sxs-lookup"><span data-stu-id="69c04-166">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="69c04-167">Interno.</span><span class="sxs-lookup"><span data-stu-id="69c04-167">Internal.</span></span>
<span data-ttu-id="69c04-168">La distribuzione della gestione delle API include un indirizzo virtuale di Intranet.</span><span class="sxs-lookup"><span data-stu-id="69c04-168">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c04-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c04-169">-DefaultProfile</span></span>
<span data-ttu-id="69c04-170">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69c04-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69c04-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c04-171">CommonParameters</span></span>
<span data-ttu-id="69c04-172">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69c04-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c04-173">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69c04-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c04-174">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69c04-174">INPUTS</span></span>

### <span data-ttu-id="69c04-175">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="69c04-175">PsApiManagement</span></span>
<span data-ttu-id="69c04-176">Il parametro ' ApiManagement ' accetta il valore di tipo ' PsApiManagement ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="69c04-176">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="69c04-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69c04-177">OUTPUTS</span></span>

### <span data-ttu-id="69c04-178">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="69c04-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="69c04-179">Note</span><span class="sxs-lookup"><span data-stu-id="69c04-179">NOTES</span></span>

## <span data-ttu-id="69c04-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69c04-180">RELATED LINKS</span></span>

[<span data-ttu-id="69c04-181">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="69c04-181">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


