---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: 48d37bf19ec6613ce1f42ee8cf7609bd6383e12f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861965"
---
# <span data-ttu-id="2dbbe-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2dbbe-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="2dbbe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2dbbe-102">SYNOPSIS</span></span>
<span data-ttu-id="2dbbe-103">Ottiene un piano di servizio app Azure nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="2dbbe-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="2dbbe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2dbbe-104">SYNTAX</span></span>

### <span data-ttu-id="2dbbe-105">S1</span><span class="sxs-lookup"><span data-stu-id="2dbbe-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2dbbe-106">S2</span><span class="sxs-lookup"><span data-stu-id="2dbbe-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dbbe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2dbbe-107">DESCRIPTION</span></span>
<span data-ttu-id="2dbbe-108">Il cmdlet **Get-AzAppServicePlan** ottiene un piano di servizio app Azure nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="2dbbe-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="2dbbe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2dbbe-109">EXAMPLES</span></span>

### <span data-ttu-id="2dbbe-110">Esempio 1: ottenere un piano di servizio app da un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2dbbe-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="2dbbe-111">Questo comando ottiene il piano di servizio app denominato ContosoASP che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="2dbbe-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="2dbbe-112">Esempio 2: ottenere tutti i piani del servizio app in una posizione</span><span class="sxs-lookup"><span data-stu-id="2dbbe-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="2dbbe-113">Questo comando consente di ottenere tutti i piani di servizio app situati nell'area "West US".</span><span class="sxs-lookup"><span data-stu-id="2dbbe-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="2dbbe-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2dbbe-114">PARAMETERS</span></span>

### <span data-ttu-id="2dbbe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dbbe-115">-DefaultProfile</span></span>
<span data-ttu-id="2dbbe-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2dbbe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dbbe-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2dbbe-117">-Location</span></span>
<span data-ttu-id="2dbbe-118">Posizione</span><span class="sxs-lookup"><span data-stu-id="2dbbe-118">Location</span></span> 

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

### <span data-ttu-id="2dbbe-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2dbbe-119">-Name</span></span>
<span data-ttu-id="2dbbe-120">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="2dbbe-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="2dbbe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dbbe-121">-ResourceGroupName</span></span>
<span data-ttu-id="2dbbe-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="2dbbe-122">Resource Group Name</span></span>

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

### <span data-ttu-id="2dbbe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dbbe-123">CommonParameters</span></span>
<span data-ttu-id="2dbbe-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dbbe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dbbe-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dbbe-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dbbe-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2dbbe-126">INPUTS</span></span>

### <span data-ttu-id="2dbbe-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2dbbe-127">None</span></span>
<span data-ttu-id="2dbbe-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="2dbbe-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2dbbe-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2dbbe-129">OUTPUTS</span></span>

### <span data-ttu-id="2dbbe-130">Microsoft. Azure. Management. website. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="2dbbe-130">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="2dbbe-131">Microsoft. Azure. Management. website. Models. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="2dbbe-131">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="2dbbe-132">Note</span><span class="sxs-lookup"><span data-stu-id="2dbbe-132">NOTES</span></span>

## <span data-ttu-id="2dbbe-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2dbbe-133">RELATED LINKS</span></span>

[<span data-ttu-id="2dbbe-134">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2dbbe-134">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="2dbbe-135">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2dbbe-135">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="2dbbe-136">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2dbbe-136">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


