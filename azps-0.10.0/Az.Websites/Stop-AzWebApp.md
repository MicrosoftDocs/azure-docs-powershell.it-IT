---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: 073c98abe9db8b8a8d52c6d9bb06e64b028d379b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861797"
---
# <span data-ttu-id="fab6e-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="fab6e-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="fab6e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fab6e-102">SYNOPSIS</span></span>
<span data-ttu-id="fab6e-103">Interrompe un'app Web Azure.</span><span class="sxs-lookup"><span data-stu-id="fab6e-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="fab6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fab6e-104">SYNTAX</span></span>

### <span data-ttu-id="fab6e-105">S1</span><span class="sxs-lookup"><span data-stu-id="fab6e-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fab6e-106">S2</span><span class="sxs-lookup"><span data-stu-id="fab6e-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fab6e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fab6e-107">DESCRIPTION</span></span>
<span data-ttu-id="fab6e-108">Il cmdlet **Stop-AzWebApp** interrompe un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="fab6e-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="fab6e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fab6e-109">EXAMPLES</span></span>

### <span data-ttu-id="fab6e-110">Esempio 1: arrestare un'app Web</span><span class="sxs-lookup"><span data-stu-id="fab6e-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="fab6e-111">Questo comando interrompe l'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="fab6e-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="fab6e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fab6e-112">PARAMETERS</span></span>

### <span data-ttu-id="fab6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab6e-113">-DefaultProfile</span></span>
<span data-ttu-id="fab6e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fab6e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fab6e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fab6e-115">-Name</span></span>
<span data-ttu-id="fab6e-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="fab6e-116">WebApp Name</span></span>

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

### <span data-ttu-id="fab6e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fab6e-117">-ResourceGroupName</span></span>
<span data-ttu-id="fab6e-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="fab6e-118">Resource Group Name</span></span>

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

### <span data-ttu-id="fab6e-119">-Web App</span><span class="sxs-lookup"><span data-stu-id="fab6e-119">-WebApp</span></span>
<span data-ttu-id="fab6e-120">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="fab6e-120">WebApp Object</span></span>

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

### <span data-ttu-id="fab6e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab6e-121">CommonParameters</span></span>
<span data-ttu-id="fab6e-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fab6e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab6e-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fab6e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab6e-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fab6e-124">INPUTS</span></span>

### <span data-ttu-id="fab6e-125">Sito</span><span class="sxs-lookup"><span data-stu-id="fab6e-125">Site</span></span>
<span data-ttu-id="fab6e-126">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fab6e-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="fab6e-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fab6e-127">OUTPUTS</span></span>

## <span data-ttu-id="fab6e-128">Note</span><span class="sxs-lookup"><span data-stu-id="fab6e-128">NOTES</span></span>

## <span data-ttu-id="fab6e-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fab6e-129">RELATED LINKS</span></span>

[<span data-ttu-id="fab6e-130">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="fab6e-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="fab6e-131">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="fab6e-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="fab6e-132">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="fab6e-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="fab6e-133">Riavviare-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="fab6e-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="fab6e-134">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="fab6e-134">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


