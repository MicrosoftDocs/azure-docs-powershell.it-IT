---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: b85d22d1030eaa12e58cded1c7225231c7e8b964
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865995"
---
# <span data-ttu-id="b7de6-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b7de6-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="b7de6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7de6-102">SYNOPSIS</span></span>
<span data-ttu-id="b7de6-103">Ottiene un piano di servizio app Azure nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b7de6-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7de6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7de6-104">SYNTAX</span></span>

### <span data-ttu-id="b7de6-105">S1</span><span class="sxs-lookup"><span data-stu-id="b7de6-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7de6-106">S2</span><span class="sxs-lookup"><span data-stu-id="b7de6-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7de6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7de6-107">DESCRIPTION</span></span>
<span data-ttu-id="b7de6-108">Il cmdlet **Get-AzureRmAppServicePlan** ottiene un piano di servizio app Azure nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b7de6-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="b7de6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7de6-109">EXAMPLES</span></span>

### <span data-ttu-id="b7de6-110">Esempio 1: ottenere un piano di servizio app da un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b7de6-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="b7de6-111">Questo comando ottiene il piano di servizio app denominato ContosoASP che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="b7de6-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="b7de6-112">Esempio 2: ottenere tutti i piani del servizio app in una posizione</span><span class="sxs-lookup"><span data-stu-id="b7de6-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="b7de6-113">Questo comando consente di ottenere tutti i piani di servizio app situati nell'area "West US".</span><span class="sxs-lookup"><span data-stu-id="b7de6-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="b7de6-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7de6-114">PARAMETERS</span></span>

### <span data-ttu-id="b7de6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7de6-115">-DefaultProfile</span></span>
<span data-ttu-id="b7de6-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7de6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7de6-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b7de6-117">-Location</span></span>
<span data-ttu-id="b7de6-118">Posizione</span><span class="sxs-lookup"><span data-stu-id="b7de6-118">Location</span></span> 

```yaml
Type: String
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7de6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7de6-119">-Name</span></span>
<span data-ttu-id="b7de6-120">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="b7de6-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7de6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7de6-121">-ResourceGroupName</span></span>
<span data-ttu-id="b7de6-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b7de6-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7de6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7de6-123">CommonParameters</span></span>
<span data-ttu-id="b7de6-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7de6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7de6-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7de6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7de6-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7de6-126">INPUTS</span></span>

### <span data-ttu-id="b7de6-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b7de6-127">None</span></span>
<span data-ttu-id="b7de6-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b7de6-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b7de6-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7de6-129">OUTPUTS</span></span>

### <span data-ttu-id="b7de6-130">Microsoft. Azure. Management. website. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="b7de6-130">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="b7de6-131">Microsoft. Azure. Management. website. Models. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="b7de6-131">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="b7de6-132">Note</span><span class="sxs-lookup"><span data-stu-id="b7de6-132">NOTES</span></span>

## <span data-ttu-id="b7de6-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7de6-133">RELATED LINKS</span></span>

[<span data-ttu-id="b7de6-134">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b7de6-134">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="b7de6-135">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b7de6-135">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="b7de6-136">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b7de6-136">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


