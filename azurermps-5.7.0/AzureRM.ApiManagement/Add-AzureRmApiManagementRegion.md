---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: f7a2952bf466a0d964a8b9075832635d2560b6fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521940"
---
# <span data-ttu-id="9fe4b-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9fe4b-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="9fe4b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9fe4b-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe4b-103">Aggiunge nuove aree di distribuzione a un'istanza di PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="9fe4b-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fe4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9fe4b-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fe4b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fe4b-105">DESCRIPTION</span></span>
<span data-ttu-id="9fe4b-106">Il cmdlet **Add-AzureRmApiManagementRegion** aggiunge una nuova istanza di tipo **PsApiManagementRegion** alla raccolta di **AdditionalRegions** dell'istanza specificata di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="9fe4b-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="9fe4b-107">Questo cmdlet non distribuisce nulla da solo, ma aggiorna l'istanza di **PsApiManagement** in memoria.</span><span class="sxs-lookup"><span data-stu-id="9fe4b-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="9fe4b-108">Per aggiornare una distribuzione di una gestione API, passare l'istanza di **PsApiManagement** modificata a Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="9fe4b-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="9fe4b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9fe4b-109">EXAMPLES</span></span>

### <span data-ttu-id="9fe4b-110">Esempio 1: aggiungere nuove aree di distribuzione a un'istanza di PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9fe4b-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="9fe4b-111">Questo comando aggiunge due unità SKU Premium e l'area denominata East US all'istanza di **PsApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="9fe4b-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="9fe4b-112">Esempio 2: aggiungere nuove aree di distribuzione a un'istanza di PsApiManagement e quindi aggiornare la distribuzione</span><span class="sxs-lookup"><span data-stu-id="9fe4b-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="9fe4b-113">Questo comando ottiene un oggetto **PsApiManagement** , aggiunge due unità SKU Premium per l'area denominata East US e quindi aggiorna la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9fe4b-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="9fe4b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9fe4b-114">PARAMETERS</span></span>

### <span data-ttu-id="9fe4b-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9fe4b-115">-ApiManagement</span></span>
<span data-ttu-id="9fe4b-116">Specifica l'istanza di **PsApiManagement** a cui questo cmdlet aggiunge altre aree di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9fe4b-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe4b-117">-Capacità</span><span class="sxs-lookup"><span data-stu-id="9fe4b-117">-Capacity</span></span>
<span data-ttu-id="9fe4b-118">Specifica la capacità SKU dell'area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9fe4b-118">Specifies the SKU capacity of the deployment region.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe4b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe4b-119">-DefaultProfile</span></span>
<span data-ttu-id="9fe4b-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9fe4b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="9fe4b-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9fe4b-121">-Location</span></span>
<span data-ttu-id="9fe4b-122">Specifica la posizione della nuova area di distribuzione tra l'area supportata per il servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="9fe4b-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>

<span data-ttu-id="9fe4b-123">Per ottenere posizioni valide, usare il cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | dove {$ _. ResourceTypes [0]. ResourceTypeName-EQ "servizio"} | Posizioni Select-Object</span><span class="sxs-lookup"><span data-stu-id="9fe4b-123">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe4b-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="9fe4b-124">-Sku</span></span>
<span data-ttu-id="9fe4b-125">Specifica il livello dell'area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9fe4b-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="9fe4b-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="9fe4b-126">Valid values are:</span></span> 

- <span data-ttu-id="9fe4b-127">Sviluppo</span><span class="sxs-lookup"><span data-stu-id="9fe4b-127">Developer</span></span>
- <span data-ttu-id="9fe4b-128">Standard</span><span class="sxs-lookup"><span data-stu-id="9fe4b-128">Standard</span></span>
- <span data-ttu-id="9fe4b-129">Premium</span><span class="sxs-lookup"><span data-stu-id="9fe4b-129">Premium</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe4b-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9fe4b-130">-VirtualNetwork</span></span>
<span data-ttu-id="9fe4b-131">Specifica una configurazione di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9fe4b-131">Specifies a virtual network configuration.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe4b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe4b-132">CommonParameters</span></span>
<span data-ttu-id="9fe4b-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fe4b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe4b-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fe4b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe4b-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9fe4b-135">INPUTS</span></span>

### <span data-ttu-id="9fe4b-136">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9fe4b-136">PsApiManagement</span></span>
<span data-ttu-id="9fe4b-137">Il parametro ' ApiManagement ' accetta il valore di tipo ' PsApiManagement ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="9fe4b-137">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="9fe4b-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9fe4b-138">OUTPUTS</span></span>

### <span data-ttu-id="9fe4b-139">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9fe4b-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="9fe4b-140">Note</span><span class="sxs-lookup"><span data-stu-id="9fe4b-140">NOTES</span></span>
* <span data-ttu-id="9fe4b-141">Il cmdlet scrive l'istanza di **PsApiManagement** aggiornata in pipeline.</span><span class="sxs-lookup"><span data-stu-id="9fe4b-141">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="9fe4b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9fe4b-142">RELATED LINKS</span></span>

[<span data-ttu-id="9fe4b-143">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9fe4b-143">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="9fe4b-144">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9fe4b-144">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="9fe4b-145">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="9fe4b-145">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


