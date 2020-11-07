---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 7fa565eb16ced9e9146b219d7850354e499ef06e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675869"
---
# <span data-ttu-id="5560c-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="5560c-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="5560c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5560c-102">SYNOPSIS</span></span>
<span data-ttu-id="5560c-103">Aggiorna l'area di distribuzione esistente nell'istanza di PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="5560c-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="5560c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5560c-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5560c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5560c-105">DESCRIPTION</span></span>
<span data-ttu-id="5560c-106">Il cmdlet **Update-AzApiManagementRegion** aggiorna un'istanza esistente di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** in una raccolta di oggetti **AdditionalRegions** di un'istanza specificata di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="5560c-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="5560c-107">Questo cmdlet non distribuisce nulla, ma aggiorna un'istanza di **PsApiManagement** in memoria.</span><span class="sxs-lookup"><span data-stu-id="5560c-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="5560c-108">Per aggiornare una distribuzione di una gestione API, usare il **PsApiManagementInstance** modificato per il cmdlet Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="5560c-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="5560c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5560c-109">EXAMPLES</span></span>

### <span data-ttu-id="5560c-110">Esempio 1: aumenta la capacità di un'area aggiuntiva in un'istanza di PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="5560c-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="5560c-111">Questo comando ottiene il servizio SKU di gestione delle API Premium, con aree geografiche negli Stati Uniti del centro sud e in Nord America centrale.</span><span class="sxs-lookup"><span data-stu-id="5560c-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="5560c-112">Aumenta quindi la capacità dell'area nord-centrale degli Stati Uniti in 2 usando il **set-AzApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="5560c-112">It then increases the Capacity of the North Central US region to 2 using the **Set-AzApiManagement**.</span></span> <span data-ttu-id="5560c-113">Il cmdlet **set-AzApiManagement** successivo applica la modifica alla configurazione del servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="5560c-113">The next cmdlet **Set-AzApiManagement** applies the configuration change to the Api Management service.</span></span>

## <span data-ttu-id="5560c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5560c-114">PARAMETERS</span></span>

### <span data-ttu-id="5560c-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5560c-115">-ApiManagement</span></span>
<span data-ttu-id="5560c-116">Specifica l'istanza di **PsApiManagement** per l'aggiornamento di un'area di distribuzione esistente.</span><span class="sxs-lookup"><span data-stu-id="5560c-116">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="5560c-117">-Capacità</span><span class="sxs-lookup"><span data-stu-id="5560c-117">-Capacity</span></span>
<span data-ttu-id="5560c-118">Specifica il nuovo valore della capacità SKU per l'area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5560c-118">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="5560c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5560c-119">-DefaultProfile</span></span>
<span data-ttu-id="5560c-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5560c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5560c-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5560c-121">-Location</span></span>
<span data-ttu-id="5560c-122">Specifica la posizione dell'area di distribuzione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="5560c-122">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="5560c-123">Specifica la posizione della nuova area di distribuzione tra l'area supportata per il servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="5560c-123">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="5560c-124">Per ottenere posizioni valide, usare il cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | dove {$ _. ResourceTypes [0]. ResourceTypeName-EQ "servizio"} | Posizioni Select-Object</span><span class="sxs-lookup"><span data-stu-id="5560c-124">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="5560c-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="5560c-125">-Sku</span></span>
<span data-ttu-id="5560c-126">Specifica il nuovo valore di livello per l'area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5560c-126">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="5560c-127">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="5560c-127">Valid values are:</span></span>
- <span data-ttu-id="5560c-128">Sviluppo</span><span class="sxs-lookup"><span data-stu-id="5560c-128">Developer</span></span>
- <span data-ttu-id="5560c-129">Standard</span><span class="sxs-lookup"><span data-stu-id="5560c-129">Standard</span></span>
- <span data-ttu-id="5560c-130">Premium</span><span class="sxs-lookup"><span data-stu-id="5560c-130">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5560c-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5560c-131">-VirtualNetwork</span></span>
<span data-ttu-id="5560c-132">Specifica una configurazione di rete virtuale per l'area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5560c-132">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="5560c-133">Passando $null verrà rimossa la configurazione della rete virtuale per l'area geografica.</span><span class="sxs-lookup"><span data-stu-id="5560c-133">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="5560c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5560c-134">CommonParameters</span></span>
<span data-ttu-id="5560c-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5560c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5560c-136">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5560c-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5560c-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5560c-137">INPUTS</span></span>

### <span data-ttu-id="5560c-138">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="5560c-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="5560c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5560c-139">System.String</span></span>

### <span data-ttu-id="5560c-140">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="5560c-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="5560c-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5560c-141">System.Int32</span></span>

### <span data-ttu-id="5560c-142">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5560c-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="5560c-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5560c-143">OUTPUTS</span></span>

### <span data-ttu-id="5560c-144">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="5560c-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="5560c-145">Note</span><span class="sxs-lookup"><span data-stu-id="5560c-145">NOTES</span></span>

## <span data-ttu-id="5560c-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5560c-146">RELATED LINKS</span></span>

[<span data-ttu-id="5560c-147">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="5560c-147">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="5560c-148">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="5560c-148">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="5560c-149">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5560c-149">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
