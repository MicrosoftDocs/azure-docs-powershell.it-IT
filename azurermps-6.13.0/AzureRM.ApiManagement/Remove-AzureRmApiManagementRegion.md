---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 9ccd7379a07b83b3ed45eff5f8095b950868810c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686970"
---
# <span data-ttu-id="1bf72-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="1bf72-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="1bf72-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1bf72-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf72-103">Rimuove un'area di distribuzione esistente dall'istanza di PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="1bf72-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bf72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1bf72-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bf72-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bf72-105">DESCRIPTION</span></span>
<span data-ttu-id="1bf72-106">Il cmdlet **Remove-AzureRmApiManagementRegion** rimuove l'istanza di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** da una raccolta di **AdditionalRegions** di cui l'istanza di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="1bf72-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="1bf72-107">Questo cmdlet non modifica la distribuzione da solo, ma aggiorna l'istanza di **PsApiManagement** in memoria.</span><span class="sxs-lookup"><span data-stu-id="1bf72-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="1bf72-108">Per aggiornare una distribuzione di una gestione API, passare il **PsApiManagementInstance** modificato in **Update-AzureRmApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="1bf72-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="1bf72-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1bf72-109">EXAMPLES</span></span>

### <span data-ttu-id="1bf72-110">Esempio 1: rimuovere un'area da un'istanza di PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="1bf72-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="1bf72-111">Questo comando consente di rimuovere l'area geografica denominata East US dall'istanza di **PsApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="1bf72-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="1bf72-112">Esempio 2: rimuovere un'area da un'istanza di PsApiManagement usando una serie di comandi</span><span class="sxs-lookup"><span data-stu-id="1bf72-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="1bf72-113">Questo primo comando consente di ottenere un'istanza di **PsApiManagement** dal gruppo di risorse denominato contoso denominato ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="1bf72-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="1bf72-114">Il comando finale rimuove quindi l'area denominata East US da tale istanza e quindi aggiorna la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="1bf72-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="1bf72-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1bf72-115">PARAMETERS</span></span>

### <span data-ttu-id="1bf72-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1bf72-116">-ApiManagement</span></span>
<span data-ttu-id="1bf72-117">Specifica l'istanza di **PsApiManagement** a cui questo cmdlet rimuove l'area di distribuzione aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="1bf72-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="1bf72-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf72-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="1bf72-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1bf72-119">-Location</span></span>
<span data-ttu-id="1bf72-120">Specifica la posizione dell'area rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bf72-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="1bf72-121">Specifica la posizione della nuova area di distribuzione tra l'area supportata per il servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="1bf72-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="1bf72-122">Per ottenere posizioni valide, usare il cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | dove {$ _. ResourceTypes [0]. ResourceTypeName-EQ "servizio"} | Posizioni Select-Object</span><span class="sxs-lookup"><span data-stu-id="1bf72-122">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="1bf72-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf72-123">CommonParameters</span></span>
<span data-ttu-id="1bf72-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf72-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf72-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bf72-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf72-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1bf72-126">INPUTS</span></span>

### <span data-ttu-id="1bf72-127">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="1bf72-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="1bf72-128">Parametri: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1bf72-128">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="1bf72-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1bf72-129">System.String</span></span>

## <span data-ttu-id="1bf72-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1bf72-130">OUTPUTS</span></span>

### <span data-ttu-id="1bf72-131">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="1bf72-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="1bf72-132">Note</span><span class="sxs-lookup"><span data-stu-id="1bf72-132">NOTES</span></span>

## <span data-ttu-id="1bf72-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1bf72-133">RELATED LINKS</span></span>

[<span data-ttu-id="1bf72-134">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="1bf72-134">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="1bf72-135">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="1bf72-135">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


