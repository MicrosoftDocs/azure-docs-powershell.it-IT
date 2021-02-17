---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: aebcb8be906811607aefee7dbdc2c7630b9e391e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401182"
---
# <span data-ttu-id="8e627-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="8e627-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="8e627-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e627-102">SYNOPSIS</span></span>
<span data-ttu-id="8e627-103">Aggiunge nuove aree di distribuzione a un'istanza di PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8e627-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="8e627-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e627-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e627-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8e627-105">DESCRIPTION</span></span>
<span data-ttu-id="8e627-106">Il cmdlet **Add-AzApiManagementRegion** aggiunge una nuova istanza del tipo **PsApiManagementRegion** alla raccolta di **AdditionalRegions** dell'istanza fornita di **tipo Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="8e627-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="8e627-107">Questo cmdlet non distribuisce da solo, ma aggiorna l'istanza di **PsApiManagement** in memoria.</span><span class="sxs-lookup"><span data-stu-id="8e627-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="8e627-108">Per aggiornare una distribuzione di gestione delle API, passare l'istanza **di PsApiManagement** modificata a Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8e627-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span></span>

## <span data-ttu-id="8e627-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e627-109">EXAMPLES</span></span>

### <span data-ttu-id="8e627-110">Esempio 1: Aggiungere nuove aree di distribuzione a un'istanza di PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="8e627-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="8e627-111">Questo comando aggiunge due unità di SKU premium e l'area geografica Stati Uniti orientali **all'istanza PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="8e627-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="8e627-112">Esempio 2: Aggiungere nuove aree di distribuzione a un'istanza di PsApiManagement e quindi aggiornare la distribuzione</span><span class="sxs-lookup"><span data-stu-id="8e627-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Set-AzApiManagement
```

<span data-ttu-id="8e627-113">Questo comando ottiene un **oggetto PsApiManagement,** aggiunge due unità di SKU premium per l'area geografica degli Stati Uniti orientali e quindi aggiorna la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8e627-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="8e627-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e627-114">PARAMETERS</span></span>

### <span data-ttu-id="8e627-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8e627-115">-ApiManagement</span></span>
<span data-ttu-id="8e627-116">Specifica **l'istanza PsApiManagement** a cui questo cmdlet aggiunge altre aree di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8e627-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="8e627-117">-Capacità</span><span class="sxs-lookup"><span data-stu-id="8e627-117">-Capacity</span></span>
<span data-ttu-id="8e627-118">Specifica la capacità di SKU dell'area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8e627-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="8e627-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e627-119">-DefaultProfile</span></span>
<span data-ttu-id="8e627-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e627-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e627-121">-Location</span><span class="sxs-lookup"><span data-stu-id="8e627-121">-Location</span></span>
<span data-ttu-id="8e627-122">Specifica la posizione della nuova area di distribuzione tra l'area supportata per il servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="8e627-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="8e627-123">Per ottenere posizioni valide, usare il cmdlet Get-AzResourceProvider -ProviderManagement "Microsoft.ApiManagement" | dove {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object percorsi</span><span class="sxs-lookup"><span data-stu-id="8e627-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="8e627-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="8e627-124">-Sku</span></span>
<span data-ttu-id="8e627-125">Specifica il livello dell'area di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8e627-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="8e627-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="8e627-126">Valid values are:</span></span>
- <span data-ttu-id="8e627-127">Sviluppatore</span><span class="sxs-lookup"><span data-stu-id="8e627-127">Developer</span></span>
- <span data-ttu-id="8e627-128">Standard</span><span class="sxs-lookup"><span data-stu-id="8e627-128">Standard</span></span>
- <span data-ttu-id="8e627-129">Premium</span><span class="sxs-lookup"><span data-stu-id="8e627-129">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e627-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8e627-130">-VirtualNetwork</span></span>
<span data-ttu-id="8e627-131">Specifica una configurazione di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8e627-131">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="8e627-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e627-132">CommonParameters</span></span>
<span data-ttu-id="8e627-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e627-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e627-134">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e627-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e627-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="8e627-135">INPUTS</span></span>

### <span data-ttu-id="8e627-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="8e627-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="8e627-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e627-137">OUTPUTS</span></span>

### <span data-ttu-id="8e627-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="8e627-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="8e627-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="8e627-139">NOTES</span></span>
* <span data-ttu-id="8e627-140">Il cmdlet scrive **l'istanza di PsApiManagement aggiornata** nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e627-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="8e627-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e627-141">RELATED LINKS</span></span>

[<span data-ttu-id="8e627-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="8e627-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="8e627-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="8e627-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="8e627-144">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8e627-144">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


