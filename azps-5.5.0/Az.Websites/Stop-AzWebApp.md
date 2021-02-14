---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: d08303ec0057a42569455c9e52c38e561de73e4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197199"
---
# <span data-ttu-id="46d85-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="46d85-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="46d85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46d85-102">SYNOPSIS</span></span>
<span data-ttu-id="46d85-103">Interrompe un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="46d85-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="46d85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46d85-104">SYNTAX</span></span>

### <span data-ttu-id="46d85-105">S1</span><span class="sxs-lookup"><span data-stu-id="46d85-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46d85-106">S2</span><span class="sxs-lookup"><span data-stu-id="46d85-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46d85-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="46d85-107">DESCRIPTION</span></span>
<span data-ttu-id="46d85-108">Il cmdlet **Stop-AzWebApp** interrompe un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="46d85-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="46d85-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46d85-109">EXAMPLES</span></span>

### <span data-ttu-id="46d85-110">Esempio 1: Arrestare un'app Web</span><span class="sxs-lookup"><span data-stu-id="46d85-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="46d85-111">Questo comando interrompe l'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="46d85-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="46d85-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46d85-112">PARAMETERS</span></span>

### <span data-ttu-id="46d85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d85-113">-DefaultProfile</span></span>
<span data-ttu-id="46d85-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46d85-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46d85-115">-Name</span><span class="sxs-lookup"><span data-stu-id="46d85-115">-Name</span></span>
<span data-ttu-id="46d85-116">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="46d85-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46d85-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d85-117">-ResourceGroupName</span></span>
<span data-ttu-id="46d85-118">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="46d85-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d85-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="46d85-119">-WebApp</span></span>
<span data-ttu-id="46d85-120">Oggetto WebApp</span><span class="sxs-lookup"><span data-stu-id="46d85-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46d85-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d85-121">CommonParameters</span></span>
<span data-ttu-id="46d85-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46d85-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d85-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46d85-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d85-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="46d85-124">INPUTS</span></span>

### <span data-ttu-id="46d85-125">System.String</span><span class="sxs-lookup"><span data-stu-id="46d85-125">System.String</span></span>

### <span data-ttu-id="46d85-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="46d85-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="46d85-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46d85-127">OUTPUTS</span></span>

### <span data-ttu-id="46d85-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="46d85-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="46d85-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="46d85-129">NOTES</span></span>

## <span data-ttu-id="46d85-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46d85-130">RELATED LINKS</span></span>

[<span data-ttu-id="46d85-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="46d85-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="46d85-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="46d85-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="46d85-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="46d85-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="46d85-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="46d85-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="46d85-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="46d85-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


