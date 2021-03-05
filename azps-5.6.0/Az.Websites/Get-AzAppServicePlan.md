---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: bbe4cf87c3af86cd8a4e72f239d4aca7c3386786
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981358"
---
# <span data-ttu-id="6f380-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6f380-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="6f380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f380-102">SYNOPSIS</span></span>
<span data-ttu-id="6f380-103">Ottiene un piano di servizio app di Azure nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="6f380-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="6f380-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f380-104">SYNTAX</span></span>

### <span data-ttu-id="6f380-105">S1</span><span class="sxs-lookup"><span data-stu-id="6f380-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f380-106">S2</span><span class="sxs-lookup"><span data-stu-id="6f380-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f380-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6f380-107">DESCRIPTION</span></span>
<span data-ttu-id="6f380-108">Il cmdlet **Get-AzAppServicePlan** ottiene un piano del servizio app di Azure nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="6f380-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="6f380-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f380-109">EXAMPLES</span></span>

### <span data-ttu-id="6f380-110">Esempio 1: Ottenere un piano di servizio app da un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6f380-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="6f380-111">Questo comando recupera il piano di servizio app denominato ContosoASP che appartiene al gruppo di risorse denominato Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="6f380-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="6f380-112">Esempio 2: Ottenere tutti i piani di servizio app in una posizione</span><span class="sxs-lookup"><span data-stu-id="6f380-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="6f380-113">Questo comando recupera tutti i piani di servizio app che si trovano nell'area "Stati Uniti occidentali".</span><span class="sxs-lookup"><span data-stu-id="6f380-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="6f380-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f380-114">PARAMETERS</span></span>

### <span data-ttu-id="6f380-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f380-115">-DefaultProfile</span></span>
<span data-ttu-id="6f380-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6f380-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f380-117">-Location</span><span class="sxs-lookup"><span data-stu-id="6f380-117">-Location</span></span>
<span data-ttu-id="6f380-118">Posizione</span><span class="sxs-lookup"><span data-stu-id="6f380-118">Location</span></span> 

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

### <span data-ttu-id="6f380-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6f380-119">-Name</span></span>
<span data-ttu-id="6f380-120">Nome del piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="6f380-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="6f380-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f380-121">-ResourceGroupName</span></span>
<span data-ttu-id="6f380-122">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6f380-122">Resource Group Name</span></span>

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

### <span data-ttu-id="6f380-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f380-123">CommonParameters</span></span>
<span data-ttu-id="6f380-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f380-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f380-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f380-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f380-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="6f380-126">INPUTS</span></span>

### <span data-ttu-id="6f380-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6f380-127">None</span></span>

## <span data-ttu-id="6f380-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f380-128">OUTPUTS</span></span>

### <span data-ttu-id="6f380-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6f380-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="6f380-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="6f380-130">NOTES</span></span>

## <span data-ttu-id="6f380-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f380-131">RELATED LINKS</span></span>

[<span data-ttu-id="6f380-132">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6f380-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="6f380-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6f380-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="6f380-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6f380-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


