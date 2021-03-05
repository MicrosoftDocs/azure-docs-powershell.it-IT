---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: 32e71b33b3c440701e501c4b68d740dcf121001d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983885"
---
# <span data-ttu-id="abe51-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="abe51-101">Get-AzWebApp</span></span>

## <span data-ttu-id="abe51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abe51-102">SYNOPSIS</span></span>
<span data-ttu-id="abe51-103">Ottiene Azure Web Apps nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="abe51-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="abe51-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="abe51-104">SYNTAX</span></span>

### <span data-ttu-id="abe51-105">S1</span><span class="sxs-lookup"><span data-stu-id="abe51-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="abe51-106">S2</span><span class="sxs-lookup"><span data-stu-id="abe51-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="abe51-107">S3</span><span class="sxs-lookup"><span data-stu-id="abe51-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abe51-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="abe51-108">DESCRIPTION</span></span>
<span data-ttu-id="abe51-109">Il cmdlet **Get-AzWebApp** ottiene informazioni su un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="abe51-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="abe51-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="abe51-110">EXAMPLES</span></span>

### <span data-ttu-id="abe51-111">Esempio 1: Ottenere un'app Web da un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="abe51-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="abe51-112">Questo comando recupera l'app Web denominata ContosoSite che appartiene al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="abe51-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="abe51-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abe51-113">PARAMETERS</span></span>

### <span data-ttu-id="abe51-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="abe51-114">-AppServicePlan</span></span>
<span data-ttu-id="abe51-115">Oggetto Piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="abe51-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abe51-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abe51-116">-DefaultProfile</span></span>
<span data-ttu-id="abe51-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="abe51-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abe51-118">-Location</span><span class="sxs-lookup"><span data-stu-id="abe51-118">-Location</span></span>
<span data-ttu-id="abe51-119">Posizione</span><span class="sxs-lookup"><span data-stu-id="abe51-119">Location</span></span>

```yaml
Type: System.String
Parameter Sets: S3
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abe51-120">-Name</span><span class="sxs-lookup"><span data-stu-id="abe51-120">-Name</span></span>
<span data-ttu-id="abe51-121">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="abe51-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abe51-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abe51-122">-ResourceGroupName</span></span>
<span data-ttu-id="abe51-123">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="abe51-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abe51-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abe51-124">CommonParameters</span></span>
<span data-ttu-id="abe51-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abe51-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abe51-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abe51-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abe51-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="abe51-127">INPUTS</span></span>

### <span data-ttu-id="abe51-128">System.String</span><span class="sxs-lookup"><span data-stu-id="abe51-128">System.String</span></span>

## <span data-ttu-id="abe51-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="abe51-129">OUTPUTS</span></span>

### <span data-ttu-id="abe51-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="abe51-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="abe51-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="abe51-131">NOTES</span></span>

## <span data-ttu-id="abe51-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="abe51-132">RELATED LINKS</span></span>

[<span data-ttu-id="abe51-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="abe51-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="abe51-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="abe51-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="abe51-135">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="abe51-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="abe51-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="abe51-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="abe51-137">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="abe51-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


