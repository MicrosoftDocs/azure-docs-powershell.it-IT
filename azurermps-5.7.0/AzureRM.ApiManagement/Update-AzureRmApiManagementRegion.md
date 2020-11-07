---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: d6c97ac0fc948ba3ee4f86a2e657a1386c693f73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687503"
---
# <span data-ttu-id="4ee17-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="4ee17-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="4ee17-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ee17-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee17-103">Aggiorna l'area di distribuzione esistente nell'istanza di PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="4ee17-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ee17-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ee17-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ee17-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ee17-105">DESCRIPTION</span></span>
<span data-ttu-id="4ee17-106">Il cmdlet **Update-AzureRmApiManagementRegion** aggiorna un'istanza esistente di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** in una raccolta di oggetti **AdditionalRegions** di un'istanza specificata di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="4ee17-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="4ee17-107">Questo cmdlet non distribuisce nulla, ma aggiorna un'istanza di **PsApiManagement** in memoria.</span><span class="sxs-lookup"><span data-stu-id="4ee17-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="4ee17-108">Per aggiornare una distribuzione di una gestione API, usare il **PsApiManagementInstance** modificato per il cmdlet Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="4ee17-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="4ee17-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ee17-109">EXAMPLES</span></span>

## <span data-ttu-id="4ee17-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ee17-110">PARAMETERS</span></span>

### <span data-ttu-id="4ee17-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ee17-111">-ApiManagement</span></span>
<span data-ttu-id="4ee17-112">Specifica l'istanza di **PsApiManagement** per l'aggiornamento di un'area di distribuzione esistente.</span><span class="sxs-lookup"><span data-stu-id="4ee17-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="4ee17-113">-Capacità</span><span class="sxs-lookup"><span data-stu-id="4ee17-113">-Capacity</span></span>
<span data-ttu-id="4ee17-114">Specifica il nuovo valore della capacità SKU per l'area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4ee17-114">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee17-115">-DefaultProfile</span></span>
<span data-ttu-id="4ee17-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ee17-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="4ee17-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4ee17-117">-Location</span></span>
<span data-ttu-id="4ee17-118">Specifica la posizione dell'area di distribuzione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="4ee17-118">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="4ee17-119">Specifica la posizione della nuova area di distribuzione tra l'area supportata per il servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="4ee17-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="4ee17-120">Per ottenere posizioni valide, usare il cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | dove {$ _. ResourceTypes [0]. ResourceTypeName-EQ "servizio"} | Posizioni Select-Object</span><span class="sxs-lookup"><span data-stu-id="4ee17-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="4ee17-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="4ee17-121">-Sku</span></span>
<span data-ttu-id="4ee17-122">Specifica il nuovo valore di livello per l'area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4ee17-122">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="4ee17-123">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="4ee17-123">Valid values are:</span></span>

- <span data-ttu-id="4ee17-124">Sviluppo</span><span class="sxs-lookup"><span data-stu-id="4ee17-124">Developer</span></span>
- <span data-ttu-id="4ee17-125">Standard</span><span class="sxs-lookup"><span data-stu-id="4ee17-125">Standard</span></span>
- <span data-ttu-id="4ee17-126">Premium</span><span class="sxs-lookup"><span data-stu-id="4ee17-126">Premium</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee17-127">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4ee17-127">-VirtualNetwork</span></span>
<span data-ttu-id="4ee17-128">Specifica una configurazione di rete virtuale per l'area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4ee17-128">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="4ee17-129">Passando $null verrà rimossa la configurazione della rete virtuale per l'area geografica.</span><span class="sxs-lookup"><span data-stu-id="4ee17-129">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="4ee17-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee17-130">CommonParameters</span></span>
<span data-ttu-id="4ee17-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ee17-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee17-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ee17-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee17-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ee17-133">INPUTS</span></span>

### <span data-ttu-id="4ee17-134">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ee17-134">PsApiManagement</span></span>
<span data-ttu-id="4ee17-135">Il parametro ' ApiManagement ' accetta il valore di tipo ' PsApiManagement ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="4ee17-135">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="4ee17-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ee17-136">OUTPUTS</span></span>

### <span data-ttu-id="4ee17-137">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ee17-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="4ee17-138">Note</span><span class="sxs-lookup"><span data-stu-id="4ee17-138">NOTES</span></span>

## <span data-ttu-id="4ee17-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ee17-139">RELATED LINKS</span></span>

[<span data-ttu-id="4ee17-140">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="4ee17-140">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="4ee17-141">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="4ee17-141">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="4ee17-142">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="4ee17-142">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
