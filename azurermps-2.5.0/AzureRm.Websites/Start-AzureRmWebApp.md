---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: b05ba189c4b718689f95acac1bfcead84cd3415b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866617"
---
# <span data-ttu-id="f54a4-101">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f54a4-101">Start-AzureRmWebApp</span></span>

## <span data-ttu-id="f54a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f54a4-102">SYNOPSIS</span></span>
<span data-ttu-id="f54a4-103">Avvia un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="f54a4-103">Starts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f54a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f54a4-104">SYNTAX</span></span>

### <span data-ttu-id="f54a4-105">S1</span><span class="sxs-lookup"><span data-stu-id="f54a4-105">S1</span></span>
```
Start-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f54a4-106">S2</span><span class="sxs-lookup"><span data-stu-id="f54a4-106">S2</span></span>
```
Start-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f54a4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f54a4-107">DESCRIPTION</span></span>
<span data-ttu-id="f54a4-108">Il cmdlet **Start-AzureRmWebApp** avvia un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="f54a4-108">The **Start-AzureRmWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="f54a4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f54a4-109">EXAMPLES</span></span>

### <span data-ttu-id="f54a4-110">Esempio 1: avviare un'app Web</span><span class="sxs-lookup"><span data-stu-id="f54a4-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="f54a4-111">Questo comando avvia l'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="f54a4-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="f54a4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f54a4-112">PARAMETERS</span></span>

### <span data-ttu-id="f54a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f54a4-113">-DefaultProfile</span></span>
<span data-ttu-id="f54a4-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f54a4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f54a4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f54a4-115">-Name</span></span>
<span data-ttu-id="f54a4-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="f54a4-116">WebApp Name</span></span>

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

### <span data-ttu-id="f54a4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f54a4-117">-ResourceGroupName</span></span>
<span data-ttu-id="f54a4-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="f54a4-118">Resource Group Name</span></span>

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

### <span data-ttu-id="f54a4-119">-Web App</span><span class="sxs-lookup"><span data-stu-id="f54a4-119">-WebApp</span></span>
<span data-ttu-id="f54a4-120">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="f54a4-120">WebApp Object</span></span>

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

### <span data-ttu-id="f54a4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f54a4-121">CommonParameters</span></span>
<span data-ttu-id="f54a4-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f54a4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f54a4-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f54a4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f54a4-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f54a4-124">INPUTS</span></span>

### <span data-ttu-id="f54a4-125">Sito</span><span class="sxs-lookup"><span data-stu-id="f54a4-125">Site</span></span>
<span data-ttu-id="f54a4-126">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f54a4-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f54a4-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f54a4-127">OUTPUTS</span></span>

## <span data-ttu-id="f54a4-128">Note</span><span class="sxs-lookup"><span data-stu-id="f54a4-128">NOTES</span></span>

## <span data-ttu-id="f54a4-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f54a4-129">RELATED LINKS</span></span>

[<span data-ttu-id="f54a4-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f54a4-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="f54a4-131">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f54a4-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="f54a4-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f54a4-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="f54a4-133">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f54a4-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="f54a4-134">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f54a4-134">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


