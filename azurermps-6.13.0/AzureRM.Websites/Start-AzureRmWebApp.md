---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
ms.openlocfilehash: 034736bf55eb6dc13f7ba8a51ec57da728733eb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508919"
---
# <span data-ttu-id="052c5-101">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="052c5-101">Start-AzureRmWebApp</span></span>

## <span data-ttu-id="052c5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="052c5-102">SYNOPSIS</span></span>
<span data-ttu-id="052c5-103">Avvia un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="052c5-103">Starts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="052c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="052c5-104">SYNTAX</span></span>

### <span data-ttu-id="052c5-105">S1</span><span class="sxs-lookup"><span data-stu-id="052c5-105">S1</span></span>
```
Start-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="052c5-106">S2</span><span class="sxs-lookup"><span data-stu-id="052c5-106">S2</span></span>
```
Start-AzureRmWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="052c5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="052c5-107">DESCRIPTION</span></span>
<span data-ttu-id="052c5-108">Il cmdlet **Start-AzureRmWebApp** avvia un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="052c5-108">The **Start-AzureRmWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="052c5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="052c5-109">EXAMPLES</span></span>

### <span data-ttu-id="052c5-110">Esempio 1: avviare un'app Web</span><span class="sxs-lookup"><span data-stu-id="052c5-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="052c5-111">Questo comando avvia l'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="052c5-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="052c5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="052c5-112">PARAMETERS</span></span>

### <span data-ttu-id="052c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="052c5-113">-DefaultProfile</span></span>
<span data-ttu-id="052c5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="052c5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="052c5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="052c5-115">-Name</span></span>
<span data-ttu-id="052c5-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="052c5-116">WebApp Name</span></span>

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

### <span data-ttu-id="052c5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="052c5-117">-ResourceGroupName</span></span>
<span data-ttu-id="052c5-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="052c5-118">Resource Group Name</span></span>

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

### <span data-ttu-id="052c5-119">-Web App</span><span class="sxs-lookup"><span data-stu-id="052c5-119">-WebApp</span></span>
<span data-ttu-id="052c5-120">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="052c5-120">WebApp Object</span></span>

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

### <span data-ttu-id="052c5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="052c5-121">CommonParameters</span></span>
<span data-ttu-id="052c5-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="052c5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="052c5-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="052c5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="052c5-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="052c5-124">INPUTS</span></span>

### <span data-ttu-id="052c5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="052c5-125">System.String</span></span>

### <span data-ttu-id="052c5-126">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="052c5-126">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="052c5-127">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="052c5-127">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="052c5-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="052c5-128">OUTPUTS</span></span>

### <span data-ttu-id="052c5-129">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="052c5-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="052c5-130">Note</span><span class="sxs-lookup"><span data-stu-id="052c5-130">NOTES</span></span>

## <span data-ttu-id="052c5-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="052c5-131">RELATED LINKS</span></span>

[<span data-ttu-id="052c5-132">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="052c5-132">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="052c5-133">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="052c5-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="052c5-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="052c5-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="052c5-135">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="052c5-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="052c5-136">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="052c5-136">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


