---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: 5b14c694ca61d5c63642012aa954b0e288551b83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676263"
---
# <span data-ttu-id="20121-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="20121-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="20121-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="20121-102">SYNOPSIS</span></span>
<span data-ttu-id="20121-103">Riavvia un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="20121-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="20121-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20121-104">SYNTAX</span></span>

### <span data-ttu-id="20121-105">S1</span><span class="sxs-lookup"><span data-stu-id="20121-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20121-106">S2</span><span class="sxs-lookup"><span data-stu-id="20121-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20121-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20121-107">DESCRIPTION</span></span>
<span data-ttu-id="20121-108">Il cmdlet **Restart-AzWebApp** si arresta e quindi avvia un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="20121-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="20121-109">Se l'app Web è in uno stato interrotto, usa il cmdlet Start-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="20121-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="20121-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20121-110">EXAMPLES</span></span>

### <span data-ttu-id="20121-111">Esempio 1: riavviare un'app Web</span><span class="sxs-lookup"><span data-stu-id="20121-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="20121-112">Questo comando Arresta l'app Azure Web denominata ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus e quindi lo riavvia.</span><span class="sxs-lookup"><span data-stu-id="20121-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="20121-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20121-113">PARAMETERS</span></span>

### <span data-ttu-id="20121-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20121-114">-DefaultProfile</span></span>
<span data-ttu-id="20121-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20121-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20121-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="20121-116">-Name</span></span>
<span data-ttu-id="20121-117">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="20121-117">WebApp Name</span></span>

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

### <span data-ttu-id="20121-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20121-118">-ResourceGroupName</span></span>
<span data-ttu-id="20121-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="20121-119">Resource Group Name</span></span>

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

### <span data-ttu-id="20121-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="20121-120">-WebApp</span></span>
<span data-ttu-id="20121-121">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="20121-121">WebApp Object</span></span>

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

### <span data-ttu-id="20121-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20121-122">CommonParameters</span></span>
<span data-ttu-id="20121-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20121-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20121-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20121-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20121-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="20121-125">INPUTS</span></span>

### <span data-ttu-id="20121-126">System. String</span><span class="sxs-lookup"><span data-stu-id="20121-126">System.String</span></span>

### <span data-ttu-id="20121-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="20121-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="20121-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20121-128">OUTPUTS</span></span>

### <span data-ttu-id="20121-129">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="20121-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="20121-130">Note</span><span class="sxs-lookup"><span data-stu-id="20121-130">NOTES</span></span>

## <span data-ttu-id="20121-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20121-131">RELATED LINKS</span></span>

[<span data-ttu-id="20121-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="20121-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="20121-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="20121-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="20121-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="20121-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="20121-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="20121-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="20121-136">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="20121-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


