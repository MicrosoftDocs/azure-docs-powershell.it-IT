---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 75bedf4546bee73767c0488f578cdb5e17c1b745
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002078"
---
# <span data-ttu-id="86aa5-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86aa5-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="86aa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86aa5-102">SYNOPSIS</span></span>

## <span data-ttu-id="86aa5-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86aa5-103">SYNTAX</span></span>

### <span data-ttu-id="86aa5-104">S1</span><span class="sxs-lookup"><span data-stu-id="86aa5-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86aa5-105">S2</span><span class="sxs-lookup"><span data-stu-id="86aa5-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86aa5-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="86aa5-106">DESCRIPTION</span></span>
<span data-ttu-id="86aa5-107">Il cmdlet **Restart-AzWebAppSlot** si arresta e avvia uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="86aa5-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="86aa5-108">Se lo slot dell'app Web è in stato di interruzione, usare il cmdlet Start-AzWebAppSlot Web.</span><span class="sxs-lookup"><span data-stu-id="86aa5-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="86aa5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86aa5-109">EXAMPLES</span></span>

### <span data-ttu-id="86aa5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="86aa5-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="86aa5-111">Questo comando riavvia lo slot Slot001 per l'app Web ContosoWebApp associata al gruppo di risorse Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="86aa5-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="86aa5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86aa5-112">PARAMETERS</span></span>

### <span data-ttu-id="86aa5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86aa5-113">-DefaultProfile</span></span>
<span data-ttu-id="86aa5-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86aa5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86aa5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="86aa5-115">-Name</span></span>
<span data-ttu-id="86aa5-116">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="86aa5-116">WebApp Name</span></span>

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

### <span data-ttu-id="86aa5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86aa5-117">-ResourceGroupName</span></span>
<span data-ttu-id="86aa5-118">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="86aa5-118">Resource Group Name</span></span>

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

### <span data-ttu-id="86aa5-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="86aa5-119">-Slot</span></span>
<span data-ttu-id="86aa5-120">Nome slot WebApp</span><span class="sxs-lookup"><span data-stu-id="86aa5-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86aa5-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="86aa5-121">-WebApp</span></span>
<span data-ttu-id="86aa5-122">Oggetto WebApp</span><span class="sxs-lookup"><span data-stu-id="86aa5-122">WebApp Object</span></span>

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

### <span data-ttu-id="86aa5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86aa5-123">CommonParameters</span></span>
<span data-ttu-id="86aa5-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86aa5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86aa5-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86aa5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86aa5-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="86aa5-126">INPUTS</span></span>

### <span data-ttu-id="86aa5-127">System.String</span><span class="sxs-lookup"><span data-stu-id="86aa5-127">System.String</span></span>

### <span data-ttu-id="86aa5-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="86aa5-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="86aa5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86aa5-129">OUTPUTS</span></span>

### <span data-ttu-id="86aa5-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="86aa5-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="86aa5-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="86aa5-131">NOTES</span></span>

## <span data-ttu-id="86aa5-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86aa5-132">RELATED LINKS</span></span>

[<span data-ttu-id="86aa5-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86aa5-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="86aa5-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86aa5-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="86aa5-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86aa5-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="86aa5-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86aa5-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="86aa5-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86aa5-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="86aa5-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86aa5-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="86aa5-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="86aa5-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
