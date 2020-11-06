---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8bacb26b4e30521ddd840d2a8081365ed9c4c6ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508796"
---
# <span data-ttu-id="e09ed-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="e09ed-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="e09ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e09ed-102">SYNOPSIS</span></span>
<span data-ttu-id="e09ed-103">Rimuove un'area di distribuzione esistente dall'istanza di PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="e09ed-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e09ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e09ed-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e09ed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e09ed-105">DESCRIPTION</span></span>
<span data-ttu-id="e09ed-106">Il cmdlet **Remove-AzureRmApiManagementRegion** rimuove l'istanza di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** da una raccolta di **AdditionalRegions** di cui l'istanza di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="e09ed-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="e09ed-107">Questo cmdlet non modifica la distribuzione da solo, ma aggiorna l'istanza di **PsApiManagement** in memoria.</span><span class="sxs-lookup"><span data-stu-id="e09ed-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="e09ed-108">Per aggiornare una distribuzione di una gestione API, passare il **PsApiManagementInstance** modificato in **Update-AzureRmApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="e09ed-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="e09ed-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e09ed-109">EXAMPLES</span></span>

### <span data-ttu-id="e09ed-110">Esempio 1: rimuovere un'area da un'istanza di PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e09ed-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="e09ed-111">Questo comando consente di rimuovere l'area geografica denominata East US dall'istanza di **PsApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="e09ed-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="e09ed-112">Esempio 2: rimuovere un'area da un'istanza di PsApiManagement usando una serie di comandi</span><span class="sxs-lookup"><span data-stu-id="e09ed-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="e09ed-113">Questo primo comando consente di ottenere un'istanza di **PsApiManagement** dal gruppo di risorse denominato contoso denominato ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="e09ed-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="e09ed-114">Il comando finale rimuove quindi l'area denominata East US da tale istanza e quindi aggiorna la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="e09ed-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="e09ed-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e09ed-115">PARAMETERS</span></span>

### <span data-ttu-id="e09ed-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e09ed-116">-ApiManagement</span></span>
<span data-ttu-id="e09ed-117">Specifica l'istanza di **PsApiManagement** a cui questo cmdlet rimuove l'area di distribuzione aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="e09ed-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="e09ed-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e09ed-118">-Location</span></span>
<span data-ttu-id="e09ed-119">Specifica la posizione dell'area rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e09ed-119">Specifies the location of the region that this cmdlet removes.</span></span>

<span data-ttu-id="e09ed-120">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="e09ed-120">Valid values are:</span></span> 

- <span data-ttu-id="e09ed-121">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="e09ed-121">North Central US</span></span>
- <span data-ttu-id="e09ed-122">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="e09ed-122">South Central US</span></span>
- <span data-ttu-id="e09ed-123">Stati Uniti centrali</span><span class="sxs-lookup"><span data-stu-id="e09ed-123">Central US</span></span>
- <span data-ttu-id="e09ed-124">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="e09ed-124">West Europe</span></span>
- <span data-ttu-id="e09ed-125">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="e09ed-125">North Europe</span></span>
- <span data-ttu-id="e09ed-126">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="e09ed-126">West US</span></span>
- <span data-ttu-id="e09ed-127">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="e09ed-127">East US</span></span>
- <span data-ttu-id="e09ed-128">Stati Uniti Est 2</span><span class="sxs-lookup"><span data-stu-id="e09ed-128">East US 2</span></span>
- <span data-ttu-id="e09ed-129">Giappone est</span><span class="sxs-lookup"><span data-stu-id="e09ed-129">Japan East</span></span>
- <span data-ttu-id="e09ed-130">Giappone ovest</span><span class="sxs-lookup"><span data-stu-id="e09ed-130">Japan West</span></span>
- <span data-ttu-id="e09ed-131">Brasile sud</span><span class="sxs-lookup"><span data-stu-id="e09ed-131">Brazil South</span></span>
- <span data-ttu-id="e09ed-132">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="e09ed-132">Southeast Asia</span></span>
- <span data-ttu-id="e09ed-133">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="e09ed-133">East Asia</span></span>
- <span data-ttu-id="e09ed-134">Australia Est</span><span class="sxs-lookup"><span data-stu-id="e09ed-134">Australia East</span></span>
- <span data-ttu-id="e09ed-135">Australia sud-est</span><span class="sxs-lookup"><span data-stu-id="e09ed-135">Australia Southeast</span></span>

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

### <span data-ttu-id="e09ed-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e09ed-136">-DefaultProfile</span></span>
<span data-ttu-id="e09ed-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e09ed-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e09ed-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e09ed-138">CommonParameters</span></span>
<span data-ttu-id="e09ed-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e09ed-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e09ed-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e09ed-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e09ed-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e09ed-141">INPUTS</span></span>

### <span data-ttu-id="e09ed-142">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e09ed-142">PsApiManagement</span></span>
<span data-ttu-id="e09ed-143">Il parametro ' ApiManagement ' accetta il valore di tipo ' PsApiManagement ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e09ed-143">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="e09ed-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e09ed-144">OUTPUTS</span></span>

### <span data-ttu-id="e09ed-145">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e09ed-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="e09ed-146">Note</span><span class="sxs-lookup"><span data-stu-id="e09ed-146">NOTES</span></span>

## <span data-ttu-id="e09ed-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e09ed-147">RELATED LINKS</span></span>

[<span data-ttu-id="e09ed-148">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="e09ed-148">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="e09ed-149">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="e09ed-149">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


