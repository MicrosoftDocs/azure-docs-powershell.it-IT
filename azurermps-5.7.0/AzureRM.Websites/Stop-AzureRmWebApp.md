---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
ms.openlocfilehash: d1e4e029676eadec3f793aff99a2d68983891f2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520312"
---
# <span data-ttu-id="b6aa1-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b6aa1-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="b6aa1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="b6aa1-103">Interrompe un'app Web Azure.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6aa1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6aa1-104">SYNTAX</span></span>

### <span data-ttu-id="b6aa1-105">S1</span><span class="sxs-lookup"><span data-stu-id="b6aa1-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6aa1-106">S2</span><span class="sxs-lookup"><span data-stu-id="b6aa1-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6aa1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6aa1-107">DESCRIPTION</span></span>
<span data-ttu-id="b6aa1-108">Il cmdlet **Stop-AzureRmWebApp** interrompe un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="b6aa1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6aa1-109">EXAMPLES</span></span>

### <span data-ttu-id="b6aa1-110">Esempio 1: arrestare un'app Web</span><span class="sxs-lookup"><span data-stu-id="b6aa1-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="b6aa1-111">Questo comando interrompe l'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b6aa1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6aa1-112">PARAMETERS</span></span>

### <span data-ttu-id="b6aa1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6aa1-113">-DefaultProfile</span></span>
<span data-ttu-id="b6aa1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6aa1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6aa1-115">-Name</span></span>
<span data-ttu-id="b6aa1-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="b6aa1-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6aa1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6aa1-117">-ResourceGroupName</span></span>
<span data-ttu-id="b6aa1-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b6aa1-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6aa1-119">-Web App</span><span class="sxs-lookup"><span data-stu-id="b6aa1-119">-WebApp</span></span>
<span data-ttu-id="b6aa1-120">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="b6aa1-120">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6aa1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6aa1-121">CommonParameters</span></span>
<span data-ttu-id="b6aa1-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6aa1-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6aa1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6aa1-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6aa1-124">INPUTS</span></span>

### <span data-ttu-id="b6aa1-125">Sito</span><span class="sxs-lookup"><span data-stu-id="b6aa1-125">Site</span></span>
<span data-ttu-id="b6aa1-126">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b6aa1-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b6aa1-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6aa1-127">OUTPUTS</span></span>

## <span data-ttu-id="b6aa1-128">Note</span><span class="sxs-lookup"><span data-stu-id="b6aa1-128">NOTES</span></span>

## <span data-ttu-id="b6aa1-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6aa1-129">RELATED LINKS</span></span>

[<span data-ttu-id="b6aa1-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b6aa1-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="b6aa1-131">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b6aa1-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="b6aa1-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b6aa1-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="b6aa1-133">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b6aa1-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="b6aa1-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b6aa1-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

