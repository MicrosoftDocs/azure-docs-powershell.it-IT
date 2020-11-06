---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: 7edf16a6970f831235f76c64ef5cb5181a49bf98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520822"
---
# <span data-ttu-id="f46de-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f46de-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="f46de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f46de-102">SYNOPSIS</span></span>
<span data-ttu-id="f46de-103">Aggiunge nuove aree di distribuzione a un'istanza di PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f46de-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f46de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f46de-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f46de-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f46de-105">DESCRIPTION</span></span>
<span data-ttu-id="f46de-106">Il cmdlet **Add-AzureRmApiManagementRegion** aggiunge una nuova istanza di tipo **PsApiManagementRegion** alla raccolta di **AdditionalRegions** dell'istanza specificata di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="f46de-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="f46de-107">Questo cmdlet non distribuisce nulla da solo, ma aggiorna l'istanza di **PsApiManagement** in memoria.</span><span class="sxs-lookup"><span data-stu-id="f46de-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="f46de-108">Per aggiornare una distribuzione di una gestione API, passare l'istanza di **PsApiManagement** modificata a Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="f46de-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="f46de-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f46de-109">EXAMPLES</span></span>

### <span data-ttu-id="f46de-110">Esempio 1: aggiungere nuove aree di distribuzione a un'istanza di PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="f46de-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="f46de-111">Questo comando aggiunge due unità SKU Premium e l'area denominata East US all'istanza di **PsApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="f46de-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="f46de-112">Esempio 2: aggiungere nuove aree di distribuzione a un'istanza di PsApiManagement e quindi aggiornare la distribuzione</span><span class="sxs-lookup"><span data-stu-id="f46de-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="f46de-113">Questo comando ottiene un oggetto **PsApiManagement** , aggiunge due unità SKU Premium per l'area denominata East US e quindi aggiorna la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f46de-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="f46de-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f46de-114">PARAMETERS</span></span>

### <span data-ttu-id="f46de-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f46de-115">-ApiManagement</span></span>
<span data-ttu-id="f46de-116">Specifica l'istanza di **PsApiManagement** a cui questo cmdlet aggiunge altre aree di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f46de-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="f46de-117">-Capacità</span><span class="sxs-lookup"><span data-stu-id="f46de-117">-Capacity</span></span>
<span data-ttu-id="f46de-118">Specifica la capacità SKU dell'area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f46de-118">Specifies the SKU capacity of the deployment region.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f46de-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f46de-119">-Location</span></span>
<span data-ttu-id="f46de-120">Specifica la posizione della nuova area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f46de-120">Specifies the location of the new deployment region.</span></span>

<span data-ttu-id="f46de-121">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="f46de-121">Valid values are:</span></span> 

- <span data-ttu-id="f46de-122">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="f46de-122">North Central US</span></span>
- <span data-ttu-id="f46de-123">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="f46de-123">South Central US</span></span>
- <span data-ttu-id="f46de-124">Stati Uniti centrali</span><span class="sxs-lookup"><span data-stu-id="f46de-124">Central US</span></span>
- <span data-ttu-id="f46de-125">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="f46de-125">West Europe</span></span>
- <span data-ttu-id="f46de-126">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="f46de-126">North Europe</span></span>
- <span data-ttu-id="f46de-127">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="f46de-127">West US</span></span>
- <span data-ttu-id="f46de-128">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="f46de-128">East US</span></span>
- <span data-ttu-id="f46de-129">Stati Uniti Est 2</span><span class="sxs-lookup"><span data-stu-id="f46de-129">East US 2</span></span>
- <span data-ttu-id="f46de-130">Giappone est</span><span class="sxs-lookup"><span data-stu-id="f46de-130">Japan East</span></span>
- <span data-ttu-id="f46de-131">Giappone ovest</span><span class="sxs-lookup"><span data-stu-id="f46de-131">Japan West</span></span>
- <span data-ttu-id="f46de-132">Brasile sud</span><span class="sxs-lookup"><span data-stu-id="f46de-132">Brazil South</span></span>
- <span data-ttu-id="f46de-133">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="f46de-133">Southeast Asia</span></span>
- <span data-ttu-id="f46de-134">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="f46de-134">East Asia</span></span>
- <span data-ttu-id="f46de-135">Australia Est</span><span class="sxs-lookup"><span data-stu-id="f46de-135">Australia East</span></span>
- <span data-ttu-id="f46de-136">Australia sud-est</span><span class="sxs-lookup"><span data-stu-id="f46de-136">Australia Southeast</span></span>

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

### <span data-ttu-id="f46de-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="f46de-137">-Sku</span></span>
<span data-ttu-id="f46de-138">Specifica il livello dell'area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f46de-138">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="f46de-139">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="f46de-139">Valid values are:</span></span> 

- <span data-ttu-id="f46de-140">Sviluppo</span><span class="sxs-lookup"><span data-stu-id="f46de-140">Developer</span></span>
- <span data-ttu-id="f46de-141">Standard</span><span class="sxs-lookup"><span data-stu-id="f46de-141">Standard</span></span>
- <span data-ttu-id="f46de-142">Premium</span><span class="sxs-lookup"><span data-stu-id="f46de-142">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f46de-143">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f46de-143">-VirtualNetwork</span></span>
<span data-ttu-id="f46de-144">Specifica una configurazione di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f46de-144">Specifies a virtual network configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f46de-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46de-145">-DefaultProfile</span></span>
<span data-ttu-id="f46de-146">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f46de-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f46de-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46de-147">CommonParameters</span></span>
<span data-ttu-id="f46de-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f46de-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46de-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f46de-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46de-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f46de-150">INPUTS</span></span>

### <span data-ttu-id="f46de-151">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="f46de-151">PsApiManagement</span></span>
<span data-ttu-id="f46de-152">Il parametro ' ApiManagement ' accetta il valore di tipo ' PsApiManagement ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f46de-152">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="f46de-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f46de-153">OUTPUTS</span></span>

### <span data-ttu-id="f46de-154">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="f46de-154">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="f46de-155">Note</span><span class="sxs-lookup"><span data-stu-id="f46de-155">NOTES</span></span>
* <span data-ttu-id="f46de-156">Il cmdlet scrive l'istanza di **PsApiManagement** aggiornata in pipeline.</span><span class="sxs-lookup"><span data-stu-id="f46de-156">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="f46de-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f46de-157">RELATED LINKS</span></span>

[<span data-ttu-id="f46de-158">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f46de-158">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="f46de-159">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f46de-159">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="f46de-160">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="f46de-160">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


