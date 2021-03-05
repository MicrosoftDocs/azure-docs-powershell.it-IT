---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: a05b9ef015d1685e92bc56b0056c9213ff3370ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011086"
---
# <span data-ttu-id="984e3-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="984e3-101">Start-AzWebApp</span></span>

## <span data-ttu-id="984e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="984e3-102">SYNOPSIS</span></span>
<span data-ttu-id="984e3-103">Avvia Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="984e3-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="984e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="984e3-104">SYNTAX</span></span>

### <span data-ttu-id="984e3-105">S1</span><span class="sxs-lookup"><span data-stu-id="984e3-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="984e3-106">S2</span><span class="sxs-lookup"><span data-stu-id="984e3-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="984e3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="984e3-107">DESCRIPTION</span></span>
<span data-ttu-id="984e3-108">Il cmdlet **Start-AzWebApp avvia** Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="984e3-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="984e3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="984e3-109">EXAMPLES</span></span>

### <span data-ttu-id="984e3-110">Esempio 1: Avviare un'app Web</span><span class="sxs-lookup"><span data-stu-id="984e3-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="984e3-111">Questo comando avvia l'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="984e3-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="984e3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="984e3-112">PARAMETERS</span></span>

### <span data-ttu-id="984e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="984e3-113">-DefaultProfile</span></span>
<span data-ttu-id="984e3-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="984e3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="984e3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="984e3-115">-Name</span></span>
<span data-ttu-id="984e3-116">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="984e3-116">WebApp Name</span></span>

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

### <span data-ttu-id="984e3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="984e3-117">-ResourceGroupName</span></span>
<span data-ttu-id="984e3-118">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="984e3-118">Resource Group Name</span></span>

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

### <span data-ttu-id="984e3-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="984e3-119">-WebApp</span></span>
<span data-ttu-id="984e3-120">Oggetto WebApp</span><span class="sxs-lookup"><span data-stu-id="984e3-120">WebApp Object</span></span>

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

### <span data-ttu-id="984e3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="984e3-121">CommonParameters</span></span>
<span data-ttu-id="984e3-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="984e3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="984e3-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="984e3-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="984e3-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="984e3-124">INPUTS</span></span>

### <span data-ttu-id="984e3-125">System.String</span><span class="sxs-lookup"><span data-stu-id="984e3-125">System.String</span></span>

### <span data-ttu-id="984e3-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="984e3-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="984e3-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="984e3-127">OUTPUTS</span></span>

### <span data-ttu-id="984e3-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="984e3-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="984e3-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="984e3-129">NOTES</span></span>

## <span data-ttu-id="984e3-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="984e3-130">RELATED LINKS</span></span>

[<span data-ttu-id="984e3-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="984e3-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="984e3-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="984e3-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="984e3-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="984e3-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="984e3-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="984e3-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="984e3-135">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="984e3-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


