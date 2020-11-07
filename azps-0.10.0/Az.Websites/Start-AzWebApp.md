---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/start-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: d533a2d7401236e374ca6f541e646cb85a080f9b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861825"
---
# <span data-ttu-id="c0cb1-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c0cb1-101">Start-AzWebApp</span></span>

## <span data-ttu-id="c0cb1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="c0cb1-103">Avvia un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="c0cb1-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="c0cb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0cb1-104">SYNTAX</span></span>

### <span data-ttu-id="c0cb1-105">S1</span><span class="sxs-lookup"><span data-stu-id="c0cb1-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0cb1-106">S2</span><span class="sxs-lookup"><span data-stu-id="c0cb1-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0cb1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0cb1-107">DESCRIPTION</span></span>
<span data-ttu-id="c0cb1-108">Il cmdlet **Start-AzWebApp** avvia un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="c0cb1-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="c0cb1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0cb1-109">EXAMPLES</span></span>

### <span data-ttu-id="c0cb1-110">Esempio 1: avviare un'app Web</span><span class="sxs-lookup"><span data-stu-id="c0cb1-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="c0cb1-111">Questo comando avvia l'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="c0cb1-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="c0cb1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0cb1-112">PARAMETERS</span></span>

### <span data-ttu-id="c0cb1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0cb1-113">-DefaultProfile</span></span>
<span data-ttu-id="c0cb1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0cb1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0cb1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0cb1-115">-Name</span></span>
<span data-ttu-id="c0cb1-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="c0cb1-116">WebApp Name</span></span>

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

### <span data-ttu-id="c0cb1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0cb1-117">-ResourceGroupName</span></span>
<span data-ttu-id="c0cb1-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c0cb1-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c0cb1-119">-Web App</span><span class="sxs-lookup"><span data-stu-id="c0cb1-119">-WebApp</span></span>
<span data-ttu-id="c0cb1-120">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="c0cb1-120">WebApp Object</span></span>

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

### <span data-ttu-id="c0cb1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0cb1-121">CommonParameters</span></span>
<span data-ttu-id="c0cb1-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0cb1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0cb1-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0cb1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0cb1-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0cb1-124">INPUTS</span></span>

### <span data-ttu-id="c0cb1-125">Sito</span><span class="sxs-lookup"><span data-stu-id="c0cb1-125">Site</span></span>
<span data-ttu-id="c0cb1-126">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c0cb1-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c0cb1-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0cb1-127">OUTPUTS</span></span>

## <span data-ttu-id="c0cb1-128">Note</span><span class="sxs-lookup"><span data-stu-id="c0cb1-128">NOTES</span></span>

## <span data-ttu-id="c0cb1-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0cb1-129">RELATED LINKS</span></span>

[<span data-ttu-id="c0cb1-130">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c0cb1-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="c0cb1-131">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c0cb1-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="c0cb1-132">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c0cb1-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="c0cb1-133">Riavviare-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c0cb1-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="c0cb1-134">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c0cb1-134">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


