---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restart-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: 975b49af1e20c5b9f4839a561494eaeb8275f02f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861842"
---
# <span data-ttu-id="28acb-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="28acb-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="28acb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28acb-102">SYNOPSIS</span></span>
<span data-ttu-id="28acb-103">Riavvia un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="28acb-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="28acb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28acb-104">SYNTAX</span></span>

### <span data-ttu-id="28acb-105">S1</span><span class="sxs-lookup"><span data-stu-id="28acb-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28acb-106">S2</span><span class="sxs-lookup"><span data-stu-id="28acb-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28acb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28acb-107">DESCRIPTION</span></span>
<span data-ttu-id="28acb-108">Il cmdlet **Restart-AzWebApp** si arresta e quindi avvia un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="28acb-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="28acb-109">Se l'app Web è in uno stato interrotto, usa il cmdlet Start-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="28acb-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="28acb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28acb-110">EXAMPLES</span></span>

### <span data-ttu-id="28acb-111">Esempio 1: riavviare un'app Web</span><span class="sxs-lookup"><span data-stu-id="28acb-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="28acb-112">Questo comando Arresta l'app Azure Web denominata ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus e quindi lo riavvia.</span><span class="sxs-lookup"><span data-stu-id="28acb-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="28acb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28acb-113">PARAMETERS</span></span>

### <span data-ttu-id="28acb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28acb-114">-DefaultProfile</span></span>
<span data-ttu-id="28acb-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28acb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28acb-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="28acb-116">-Name</span></span>
<span data-ttu-id="28acb-117">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="28acb-117">WebApp Name</span></span>

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

### <span data-ttu-id="28acb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28acb-118">-ResourceGroupName</span></span>
<span data-ttu-id="28acb-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="28acb-119">Resource Group Name</span></span>

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

### <span data-ttu-id="28acb-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="28acb-120">-WebApp</span></span>
<span data-ttu-id="28acb-121">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="28acb-121">WebApp Object</span></span>

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

### <span data-ttu-id="28acb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28acb-122">CommonParameters</span></span>
<span data-ttu-id="28acb-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28acb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28acb-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28acb-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28acb-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28acb-125">INPUTS</span></span>

### <span data-ttu-id="28acb-126">Sito</span><span class="sxs-lookup"><span data-stu-id="28acb-126">Site</span></span>
<span data-ttu-id="28acb-127">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="28acb-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="28acb-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28acb-128">OUTPUTS</span></span>

## <span data-ttu-id="28acb-129">Note</span><span class="sxs-lookup"><span data-stu-id="28acb-129">NOTES</span></span>

## <span data-ttu-id="28acb-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28acb-130">RELATED LINKS</span></span>

[<span data-ttu-id="28acb-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="28acb-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="28acb-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="28acb-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="28acb-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="28acb-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="28acb-134">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="28acb-134">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="28acb-135">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="28acb-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


