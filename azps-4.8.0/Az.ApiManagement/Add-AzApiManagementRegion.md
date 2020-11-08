---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: 172bd1490b105b942dc706afe9440030d39d5c49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032723"
---
# <span data-ttu-id="b4d8a-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b4d8a-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="b4d8a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4d8a-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d8a-103">Aggiunge nuove aree di distribuzione a un'istanza di PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="b4d8a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4d8a-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4d8a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4d8a-105">DESCRIPTION</span></span>
<span data-ttu-id="b4d8a-106">Il cmdlet **Add-AzApiManagementRegion** aggiunge una nuova istanza di tipo **PsApiManagementRegion** alla raccolta di **AdditionalRegions** dell'istanza specificata di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="b4d8a-107">Questo cmdlet non distribuisce nulla da solo, ma aggiorna l'istanza di **PsApiManagement** in memoria.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="b4d8a-108">Per aggiornare una distribuzione di una gestione API, passare l'istanza di **PsApiManagement** modificata a set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span></span>

## <span data-ttu-id="b4d8a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4d8a-109">EXAMPLES</span></span>

### <span data-ttu-id="b4d8a-110">Esempio 1: aggiungere nuove aree di distribuzione a un'istanza di PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d8a-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="b4d8a-111">Questo comando aggiunge due unità SKU Premium e l'area denominata East US all'istanza di **PsApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="b4d8a-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="b4d8a-112">Esempio 2: aggiungere nuove aree di distribuzione a un'istanza di PsApiManagement e quindi aggiornare la distribuzione</span><span class="sxs-lookup"><span data-stu-id="b4d8a-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

<span data-ttu-id="b4d8a-113">Questo comando ottiene un oggetto **PsApiManagement** , aggiunge due unità SKU Premium per l'area denominata East US e quindi aggiorna la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="b4d8a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4d8a-114">PARAMETERS</span></span>

### <span data-ttu-id="b4d8a-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d8a-115">-ApiManagement</span></span>
<span data-ttu-id="b4d8a-116">Specifica l'istanza di **PsApiManagement** a cui questo cmdlet aggiunge altre aree di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="b4d8a-117">-Capacità</span><span class="sxs-lookup"><span data-stu-id="b4d8a-117">-Capacity</span></span>
<span data-ttu-id="b4d8a-118">Specifica la capacità SKU dell'area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="b4d8a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d8a-119">-DefaultProfile</span></span>
<span data-ttu-id="b4d8a-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4d8a-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b4d8a-121">-Location</span></span>
<span data-ttu-id="b4d8a-122">Specifica la posizione della nuova area di distribuzione tra l'area supportata per il servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="b4d8a-123">Per ottenere posizioni valide, usare il cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | dove {$ _. ResourceTypes [0]. ResourceTypeName-EQ "servizio"} | Posizioni Select-Object</span><span class="sxs-lookup"><span data-stu-id="b4d8a-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="b4d8a-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="b4d8a-124">-Sku</span></span>
<span data-ttu-id="b4d8a-125">Specifica il livello dell'area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="b4d8a-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b4d8a-126">Valid values are:</span></span> 
- <span data-ttu-id="b4d8a-127">Sviluppo</span><span class="sxs-lookup"><span data-stu-id="b4d8a-127">Developer</span></span>
- <span data-ttu-id="b4d8a-128">Standard</span><span class="sxs-lookup"><span data-stu-id="b4d8a-128">Standard</span></span>
- <span data-ttu-id="b4d8a-129">Premium</span><span class="sxs-lookup"><span data-stu-id="b4d8a-129">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d8a-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b4d8a-130">-VirtualNetwork</span></span>
<span data-ttu-id="b4d8a-131">Specifica una configurazione di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-131">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="b4d8a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d8a-132">CommonParameters</span></span>
<span data-ttu-id="b4d8a-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d8a-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4d8a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d8a-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4d8a-135">INPUTS</span></span>

### <span data-ttu-id="b4d8a-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d8a-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b4d8a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4d8a-137">OUTPUTS</span></span>

### <span data-ttu-id="b4d8a-138">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d8a-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b4d8a-139">Note</span><span class="sxs-lookup"><span data-stu-id="b4d8a-139">NOTES</span></span>
* <span data-ttu-id="b4d8a-140">Il cmdlet scrive l'istanza di **PsApiManagement** aggiornata in pipeline.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="b4d8a-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4d8a-141">RELATED LINKS</span></span>

[<span data-ttu-id="b4d8a-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b4d8a-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="b4d8a-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b4d8a-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="b4d8a-144">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d8a-144">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


