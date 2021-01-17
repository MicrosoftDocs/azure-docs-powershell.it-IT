---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: d08303ec0057a42569455c9e52c38e561de73e4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351292"
---
# <span data-ttu-id="72b92-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="72b92-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="72b92-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72b92-102">SYNOPSIS</span></span>
<span data-ttu-id="72b92-103">Interrompe un'app Web Azure.</span><span class="sxs-lookup"><span data-stu-id="72b92-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="72b92-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72b92-104">SYNTAX</span></span>

### <span data-ttu-id="72b92-105">S1</span><span class="sxs-lookup"><span data-stu-id="72b92-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="72b92-106">S2</span><span class="sxs-lookup"><span data-stu-id="72b92-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72b92-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72b92-107">DESCRIPTION</span></span>
<span data-ttu-id="72b92-108">Il cmdlet **Stop-AzWebApp** interrompe un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="72b92-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="72b92-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72b92-109">EXAMPLES</span></span>

### <span data-ttu-id="72b92-110">Esempio 1: arrestare un'app Web</span><span class="sxs-lookup"><span data-stu-id="72b92-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="72b92-111">Questo comando interrompe l'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="72b92-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="72b92-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72b92-112">PARAMETERS</span></span>

### <span data-ttu-id="72b92-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72b92-113">-DefaultProfile</span></span>
<span data-ttu-id="72b92-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72b92-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72b92-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="72b92-115">-Name</span></span>
<span data-ttu-id="72b92-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="72b92-116">WebApp Name</span></span>

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

### <span data-ttu-id="72b92-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72b92-117">-ResourceGroupName</span></span>
<span data-ttu-id="72b92-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="72b92-118">Resource Group Name</span></span>

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

### <span data-ttu-id="72b92-119">-Web App</span><span class="sxs-lookup"><span data-stu-id="72b92-119">-WebApp</span></span>
<span data-ttu-id="72b92-120">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="72b92-120">WebApp Object</span></span>

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

### <span data-ttu-id="72b92-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72b92-121">CommonParameters</span></span>
<span data-ttu-id="72b92-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72b92-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72b92-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72b92-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72b92-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72b92-124">INPUTS</span></span>

### <span data-ttu-id="72b92-125">System. String</span><span class="sxs-lookup"><span data-stu-id="72b92-125">System.String</span></span>

### <span data-ttu-id="72b92-126">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="72b92-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="72b92-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72b92-127">OUTPUTS</span></span>

### <span data-ttu-id="72b92-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="72b92-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="72b92-129">Note</span><span class="sxs-lookup"><span data-stu-id="72b92-129">NOTES</span></span>

## <span data-ttu-id="72b92-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72b92-130">RELATED LINKS</span></span>

[<span data-ttu-id="72b92-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="72b92-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="72b92-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="72b92-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="72b92-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="72b92-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="72b92-134">Riavviare-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="72b92-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="72b92-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="72b92-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


