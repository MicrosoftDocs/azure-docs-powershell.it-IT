---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 09c618e617775e0c2bfffab1794f2427f97d811c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858649"
---
# <span data-ttu-id="5ce68-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5ce68-101">Start-AzWebApp</span></span>

## <span data-ttu-id="5ce68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ce68-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce68-103">Avvia un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce68-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="5ce68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ce68-104">SYNTAX</span></span>

### <span data-ttu-id="5ce68-105">S1</span><span class="sxs-lookup"><span data-stu-id="5ce68-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ce68-106">S2</span><span class="sxs-lookup"><span data-stu-id="5ce68-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ce68-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ce68-107">DESCRIPTION</span></span>
<span data-ttu-id="5ce68-108">Il cmdlet **Start-AzWebApp** avvia un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce68-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="5ce68-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ce68-109">EXAMPLES</span></span>

### <span data-ttu-id="5ce68-110">Esempio 1: avviare un'app Web</span><span class="sxs-lookup"><span data-stu-id="5ce68-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="5ce68-111">Questo comando avvia l'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="5ce68-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="5ce68-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ce68-112">PARAMETERS</span></span>

### <span data-ttu-id="5ce68-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce68-113">-DefaultProfile</span></span>
<span data-ttu-id="5ce68-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce68-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ce68-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ce68-115">-Name</span></span>
<span data-ttu-id="5ce68-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="5ce68-116">WebApp Name</span></span>

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

### <span data-ttu-id="5ce68-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ce68-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ce68-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="5ce68-118">Resource Group Name</span></span>

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

### <span data-ttu-id="5ce68-119">-Web App</span><span class="sxs-lookup"><span data-stu-id="5ce68-119">-WebApp</span></span>
<span data-ttu-id="5ce68-120">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="5ce68-120">WebApp Object</span></span>

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

### <span data-ttu-id="5ce68-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce68-121">CommonParameters</span></span>
<span data-ttu-id="5ce68-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ce68-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce68-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ce68-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce68-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ce68-124">INPUTS</span></span>

### <span data-ttu-id="5ce68-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5ce68-125">System.String</span></span>

### <span data-ttu-id="5ce68-126">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="5ce68-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5ce68-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ce68-127">OUTPUTS</span></span>

### <span data-ttu-id="5ce68-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="5ce68-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5ce68-129">Note</span><span class="sxs-lookup"><span data-stu-id="5ce68-129">NOTES</span></span>

## <span data-ttu-id="5ce68-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ce68-130">RELATED LINKS</span></span>

[<span data-ttu-id="5ce68-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5ce68-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="5ce68-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5ce68-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="5ce68-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5ce68-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="5ce68-134">Riavviare-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5ce68-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="5ce68-135">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5ce68-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


