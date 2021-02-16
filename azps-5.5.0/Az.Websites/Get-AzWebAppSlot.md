---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207483"
---
# <span data-ttu-id="dfe28-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dfe28-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="dfe28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfe28-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe28-103">Ottiene uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="dfe28-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="dfe28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfe28-104">SYNTAX</span></span>

### <span data-ttu-id="dfe28-105">S1</span><span class="sxs-lookup"><span data-stu-id="dfe28-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfe28-106">S2</span><span class="sxs-lookup"><span data-stu-id="dfe28-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfe28-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dfe28-107">DESCRIPTION</span></span>
<span data-ttu-id="dfe28-108">Il cmdlet **Get-AzWebAppSlot** ottiene informazioni su uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="dfe28-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="dfe28-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfe28-109">EXAMPLES</span></span>

### <span data-ttu-id="dfe28-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dfe28-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="dfe28-111">Questo comando recupera lo slot denominato Slot001 dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="dfe28-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="dfe28-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfe28-112">PARAMETERS</span></span>

### <span data-ttu-id="dfe28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe28-113">-DefaultProfile</span></span>
<span data-ttu-id="dfe28-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe28-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfe28-115">-Name</span><span class="sxs-lookup"><span data-stu-id="dfe28-115">-Name</span></span>
<span data-ttu-id="dfe28-116">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="dfe28-116">WebApp Name</span></span>

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

### <span data-ttu-id="dfe28-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe28-117">-ResourceGroupName</span></span>
<span data-ttu-id="dfe28-118">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="dfe28-118">Resource Group Name</span></span>

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

### <span data-ttu-id="dfe28-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="dfe28-119">-Slot</span></span>
<span data-ttu-id="dfe28-120">Nome slot WebApp</span><span class="sxs-lookup"><span data-stu-id="dfe28-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe28-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="dfe28-121">-WebApp</span></span>
<span data-ttu-id="dfe28-122">Oggetto WebApp</span><span class="sxs-lookup"><span data-stu-id="dfe28-122">WebApp Object</span></span>

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

### <span data-ttu-id="dfe28-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe28-123">CommonParameters</span></span>
<span data-ttu-id="dfe28-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfe28-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe28-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfe28-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe28-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="dfe28-126">INPUTS</span></span>

### <span data-ttu-id="dfe28-127">System.String</span><span class="sxs-lookup"><span data-stu-id="dfe28-127">System.String</span></span>

### <span data-ttu-id="dfe28-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="dfe28-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="dfe28-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfe28-129">OUTPUTS</span></span>

### <span data-ttu-id="dfe28-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="dfe28-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="dfe28-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="dfe28-131">NOTES</span></span>

## <span data-ttu-id="dfe28-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfe28-132">RELATED LINKS</span></span>

[<span data-ttu-id="dfe28-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dfe28-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="dfe28-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dfe28-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="dfe28-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dfe28-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="dfe28-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dfe28-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="dfe28-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dfe28-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="dfe28-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dfe28-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="dfe28-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dfe28-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
