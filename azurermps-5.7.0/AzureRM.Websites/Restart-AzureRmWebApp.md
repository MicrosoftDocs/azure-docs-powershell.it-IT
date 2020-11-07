---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
ms.openlocfilehash: 7543a1dfbbab0c2cedc59fd8ca0d3b60d78ca69d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685594"
---
# <span data-ttu-id="39c8e-101">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="39c8e-101">Restart-AzureRmWebApp</span></span>

## <span data-ttu-id="39c8e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="39c8e-103">Riavvia un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="39c8e-103">Restarts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39c8e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39c8e-104">SYNTAX</span></span>

### <span data-ttu-id="39c8e-105">S1</span><span class="sxs-lookup"><span data-stu-id="39c8e-105">S1</span></span>
```
Restart-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="39c8e-106">S2</span><span class="sxs-lookup"><span data-stu-id="39c8e-106">S2</span></span>
```
Restart-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39c8e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39c8e-107">DESCRIPTION</span></span>
<span data-ttu-id="39c8e-108">Il cmdlet **Restart-AzureRmWebApp** si arresta e quindi avvia un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="39c8e-108">The **Restart-AzureRmWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="39c8e-109">Se l'app Web è in uno stato interrotto, usa il cmdlet Start-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="39c8e-109">If the Web App is in a stopped state, use the Start-AzureRmWebApp cmdlet.</span></span>

## <span data-ttu-id="39c8e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39c8e-110">EXAMPLES</span></span>

### <span data-ttu-id="39c8e-111">Esempio 1: riavviare un'app Web</span><span class="sxs-lookup"><span data-stu-id="39c8e-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="39c8e-112">Questo comando Arresta l'app Azure Web denominata ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus e quindi lo riavvia.</span><span class="sxs-lookup"><span data-stu-id="39c8e-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="39c8e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39c8e-113">PARAMETERS</span></span>

### <span data-ttu-id="39c8e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c8e-114">-DefaultProfile</span></span>
<span data-ttu-id="39c8e-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39c8e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39c8e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="39c8e-116">-Name</span></span>
<span data-ttu-id="39c8e-117">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="39c8e-117">WebApp Name</span></span>

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

### <span data-ttu-id="39c8e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39c8e-118">-ResourceGroupName</span></span>
<span data-ttu-id="39c8e-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="39c8e-119">Resource Group Name</span></span>

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

### <span data-ttu-id="39c8e-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="39c8e-120">-WebApp</span></span>
<span data-ttu-id="39c8e-121">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="39c8e-121">WebApp Object</span></span>

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

### <span data-ttu-id="39c8e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c8e-122">CommonParameters</span></span>
<span data-ttu-id="39c8e-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39c8e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c8e-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39c8e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c8e-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39c8e-125">INPUTS</span></span>

### <span data-ttu-id="39c8e-126">Sito</span><span class="sxs-lookup"><span data-stu-id="39c8e-126">Site</span></span>
<span data-ttu-id="39c8e-127">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="39c8e-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="39c8e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39c8e-128">OUTPUTS</span></span>

## <span data-ttu-id="39c8e-129">Note</span><span class="sxs-lookup"><span data-stu-id="39c8e-129">NOTES</span></span>

## <span data-ttu-id="39c8e-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39c8e-130">RELATED LINKS</span></span>

[<span data-ttu-id="39c8e-131">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="39c8e-131">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="39c8e-132">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="39c8e-132">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="39c8e-133">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="39c8e-133">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="39c8e-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="39c8e-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="39c8e-135">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="39c8e-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


