---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
ms.openlocfilehash: 9fe7d3d9580411c31fdf5ca7e21ba1c4379217a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516347"
---
# <span data-ttu-id="39a78-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="39a78-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="39a78-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39a78-102">SYNOPSIS</span></span>
<span data-ttu-id="39a78-103">Ottiene un piano di servizio app Azure nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="39a78-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39a78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39a78-104">SYNTAX</span></span>

### <span data-ttu-id="39a78-105">S1</span><span class="sxs-lookup"><span data-stu-id="39a78-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39a78-106">S2</span><span class="sxs-lookup"><span data-stu-id="39a78-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39a78-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39a78-107">DESCRIPTION</span></span>
<span data-ttu-id="39a78-108">Il cmdlet **Get-AzureRmAppServicePlan** ottiene un piano di servizio app Azure nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="39a78-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="39a78-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39a78-109">EXAMPLES</span></span>

### <span data-ttu-id="39a78-110">Esempio 1: ottenere un piano di servizio app da un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="39a78-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="39a78-111">Questo comando ottiene il piano di servizio app denominato ContosoASP che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="39a78-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="39a78-112">Esempio 2: ottenere tutti i piani del servizio app in una posizione</span><span class="sxs-lookup"><span data-stu-id="39a78-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="39a78-113">Questo comando consente di ottenere tutti i piani di servizio app situati nell'area "West US".</span><span class="sxs-lookup"><span data-stu-id="39a78-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="39a78-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39a78-114">PARAMETERS</span></span>

### <span data-ttu-id="39a78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39a78-115">-DefaultProfile</span></span>
<span data-ttu-id="39a78-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39a78-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39a78-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="39a78-117">-Location</span></span>
<span data-ttu-id="39a78-118">Posizione</span><span class="sxs-lookup"><span data-stu-id="39a78-118">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a78-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="39a78-119">-Name</span></span>
<span data-ttu-id="39a78-120">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="39a78-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a78-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39a78-121">-ResourceGroupName</span></span>
<span data-ttu-id="39a78-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="39a78-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a78-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39a78-123">CommonParameters</span></span>
<span data-ttu-id="39a78-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39a78-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39a78-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39a78-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39a78-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39a78-126">INPUTS</span></span>

### <span data-ttu-id="39a78-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="39a78-127">None</span></span>

## <span data-ttu-id="39a78-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39a78-128">OUTPUTS</span></span>

### <span data-ttu-id="39a78-129">Microsoft. Azure. Management. website. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="39a78-129">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="39a78-130">Note</span><span class="sxs-lookup"><span data-stu-id="39a78-130">NOTES</span></span>

## <span data-ttu-id="39a78-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39a78-131">RELATED LINKS</span></span>

[<span data-ttu-id="39a78-132">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="39a78-132">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="39a78-133">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="39a78-133">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="39a78-134">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="39a78-134">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


