---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: 29dd6d1938228d3e76c0393ca27f49a3a9fe2564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508772"
---
# <span data-ttu-id="3b062-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3b062-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="3b062-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b062-102">SYNOPSIS</span></span>
<span data-ttu-id="3b062-103">Aggiorna l'area di distribuzione esistente nell'istanza di PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3b062-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b062-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b062-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b062-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b062-105">DESCRIPTION</span></span>
<span data-ttu-id="3b062-106">Il cmdlet **Update-AzureRmApiManagementRegion** aggiorna un'istanza esistente di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** in una raccolta di oggetti **AdditionalRegions** di un'istanza specificata di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="3b062-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="3b062-107">Questo cmdlet non distribuisce nulla, ma aggiorna un'istanza di **PsApiManagement** in memoria.</span><span class="sxs-lookup"><span data-stu-id="3b062-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="3b062-108">Per aggiornare una distribuzione di una gestione API, usare il **PsApiManagementInstance** modificato per il cmdlet Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="3b062-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="3b062-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b062-109">EXAMPLES</span></span>

## <span data-ttu-id="3b062-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b062-110">PARAMETERS</span></span>

### <span data-ttu-id="3b062-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3b062-111">-ApiManagement</span></span>
<span data-ttu-id="3b062-112">Specifica l'istanza di **PsApiManagement** per l'aggiornamento di un'area di distribuzione esistente.</span><span class="sxs-lookup"><span data-stu-id="3b062-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b062-113">-Capacità</span><span class="sxs-lookup"><span data-stu-id="3b062-113">-Capacity</span></span>
<span data-ttu-id="3b062-114">Specifica il nuovo valore della capacità SKU per l'area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="3b062-114">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b062-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3b062-115">-Location</span></span>
<span data-ttu-id="3b062-116">Specifica la posizione dell'area di distribuzione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="3b062-116">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="3b062-117">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="3b062-117">Valid values are:</span></span>

- <span data-ttu-id="3b062-118">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="3b062-118">North Central US</span></span>
- <span data-ttu-id="3b062-119">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="3b062-119">South Central US</span></span>
- <span data-ttu-id="3b062-120">Stati Uniti centrali</span><span class="sxs-lookup"><span data-stu-id="3b062-120">Central US</span></span>
- <span data-ttu-id="3b062-121">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="3b062-121">West Europe</span></span>
- <span data-ttu-id="3b062-122">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="3b062-122">North Europe</span></span>
- <span data-ttu-id="3b062-123">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="3b062-123">West US</span></span>
- <span data-ttu-id="3b062-124">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="3b062-124">East US</span></span>
- <span data-ttu-id="3b062-125">Stati Uniti Est 2</span><span class="sxs-lookup"><span data-stu-id="3b062-125">East US 2</span></span>
- <span data-ttu-id="3b062-126">Giappone est</span><span class="sxs-lookup"><span data-stu-id="3b062-126">Japan East</span></span>
- <span data-ttu-id="3b062-127">Giappone ovest</span><span class="sxs-lookup"><span data-stu-id="3b062-127">Japan West</span></span>
- <span data-ttu-id="3b062-128">Brasile sud</span><span class="sxs-lookup"><span data-stu-id="3b062-128">Brazil South</span></span>
- <span data-ttu-id="3b062-129">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="3b062-129">Southeast Asia</span></span>
- <span data-ttu-id="3b062-130">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="3b062-130">East Asia</span></span>
- <span data-ttu-id="3b062-131">Australia Est</span><span class="sxs-lookup"><span data-stu-id="3b062-131">Australia East</span></span>
- <span data-ttu-id="3b062-132">Australia sud-est</span><span class="sxs-lookup"><span data-stu-id="3b062-132">Australia Southeast</span></span>

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

### <span data-ttu-id="3b062-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="3b062-133">-Sku</span></span>
<span data-ttu-id="3b062-134">Specifica il nuovo valore di livello per l'area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="3b062-134">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="3b062-135">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="3b062-135">Valid values are:</span></span>

- <span data-ttu-id="3b062-136">Sviluppo</span><span class="sxs-lookup"><span data-stu-id="3b062-136">Developer</span></span>
- <span data-ttu-id="3b062-137">Standard</span><span class="sxs-lookup"><span data-stu-id="3b062-137">Standard</span></span>
- <span data-ttu-id="3b062-138">Premium</span><span class="sxs-lookup"><span data-stu-id="3b062-138">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b062-139">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3b062-139">-VirtualNetwork</span></span>
<span data-ttu-id="3b062-140">Specifica una configurazione di rete virtuale per l'area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="3b062-140">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="3b062-141">Passando $null verrà rimossa la configurazione della rete virtuale per l'area geografica.</span><span class="sxs-lookup"><span data-stu-id="3b062-141">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="3b062-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b062-142">-DefaultProfile</span></span>
<span data-ttu-id="3b062-143">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b062-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b062-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b062-144">CommonParameters</span></span>
<span data-ttu-id="3b062-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b062-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b062-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b062-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b062-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b062-147">INPUTS</span></span>

### <span data-ttu-id="3b062-148">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3b062-148">PsApiManagement</span></span>
<span data-ttu-id="3b062-149">Il parametro ' ApiManagement ' accetta il valore di tipo ' PsApiManagement ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3b062-149">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="3b062-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b062-150">OUTPUTS</span></span>

### <span data-ttu-id="3b062-151">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3b062-151">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="3b062-152">Note</span><span class="sxs-lookup"><span data-stu-id="3b062-152">NOTES</span></span>

## <span data-ttu-id="3b062-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b062-153">RELATED LINKS</span></span>

[<span data-ttu-id="3b062-154">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3b062-154">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="3b062-155">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3b062-155">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="3b062-156">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="3b062-156">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
