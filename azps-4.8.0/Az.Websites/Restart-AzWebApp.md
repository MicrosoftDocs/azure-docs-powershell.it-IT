---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: faa3264dbf9fa65a2970f578c635868d185f2ef8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188659"
---
# <span data-ttu-id="a44c3-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a44c3-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="a44c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a44c3-102">SYNOPSIS</span></span>
<span data-ttu-id="a44c3-103">Riavvia un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="a44c3-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="a44c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a44c3-104">SYNTAX</span></span>

### <span data-ttu-id="a44c3-105">S1</span><span class="sxs-lookup"><span data-stu-id="a44c3-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a44c3-106">S2</span><span class="sxs-lookup"><span data-stu-id="a44c3-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a44c3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a44c3-107">DESCRIPTION</span></span>
<span data-ttu-id="a44c3-108">Il cmdlet **Restart-AzWebApp** si arresta e quindi avvia un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="a44c3-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="a44c3-109">Se l'app Web è in uno stato interrotto, usa il cmdlet Start-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="a44c3-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="a44c3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a44c3-110">EXAMPLES</span></span>

### <span data-ttu-id="a44c3-111">Esempio 1: riavviare un'app Web</span><span class="sxs-lookup"><span data-stu-id="a44c3-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="a44c3-112">Questo comando Arresta l'app Azure Web denominata ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus e quindi lo riavvia.</span><span class="sxs-lookup"><span data-stu-id="a44c3-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="a44c3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a44c3-113">PARAMETERS</span></span>

### <span data-ttu-id="a44c3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a44c3-114">-DefaultProfile</span></span>
<span data-ttu-id="a44c3-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a44c3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a44c3-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a44c3-116">-Name</span></span>
<span data-ttu-id="a44c3-117">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="a44c3-117">WebApp Name</span></span>

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

### <span data-ttu-id="a44c3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a44c3-118">-ResourceGroupName</span></span>
<span data-ttu-id="a44c3-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a44c3-119">Resource Group Name</span></span>

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

### <span data-ttu-id="a44c3-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="a44c3-120">-WebApp</span></span>
<span data-ttu-id="a44c3-121">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="a44c3-121">WebApp Object</span></span>

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

### <span data-ttu-id="a44c3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a44c3-122">CommonParameters</span></span>
<span data-ttu-id="a44c3-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a44c3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a44c3-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a44c3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a44c3-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a44c3-125">INPUTS</span></span>

### <span data-ttu-id="a44c3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a44c3-126">System.String</span></span>

### <span data-ttu-id="a44c3-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="a44c3-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a44c3-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a44c3-128">OUTPUTS</span></span>

### <span data-ttu-id="a44c3-129">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="a44c3-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a44c3-130">Note</span><span class="sxs-lookup"><span data-stu-id="a44c3-130">NOTES</span></span>

## <span data-ttu-id="a44c3-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a44c3-131">RELATED LINKS</span></span>

[<span data-ttu-id="a44c3-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a44c3-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="a44c3-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a44c3-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="a44c3-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a44c3-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="a44c3-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a44c3-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="a44c3-136">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a44c3-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


