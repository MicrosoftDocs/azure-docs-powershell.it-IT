---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: eba40b4c372fd900ac42bead0e2c0b39305c91cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197190"
---
# <span data-ttu-id="0589a-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0589a-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="0589a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0589a-102">SYNOPSIS</span></span>
<span data-ttu-id="0589a-103">Interrompe uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0589a-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="0589a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0589a-104">SYNTAX</span></span>

### <span data-ttu-id="0589a-105">S1</span><span class="sxs-lookup"><span data-stu-id="0589a-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0589a-106">S2</span><span class="sxs-lookup"><span data-stu-id="0589a-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0589a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0589a-107">DESCRIPTION</span></span>
<span data-ttu-id="0589a-108">Il cmdlet **Stop-AzWebAppSlot** interrompe uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0589a-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="0589a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0589a-109">EXAMPLES</span></span>

### <span data-ttu-id="0589a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0589a-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="0589a-111">Questo comando interrompe lo slot Slot001 relativo all'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="0589a-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="0589a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0589a-112">PARAMETERS</span></span>

### <span data-ttu-id="0589a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0589a-113">-DefaultProfile</span></span>
<span data-ttu-id="0589a-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0589a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0589a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0589a-115">-Name</span></span>
<span data-ttu-id="0589a-116">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="0589a-116">WebApp Name</span></span>

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

### <span data-ttu-id="0589a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0589a-117">-ResourceGroupName</span></span>
<span data-ttu-id="0589a-118">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0589a-118">Resource Group Name</span></span>

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

### <span data-ttu-id="0589a-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="0589a-119">-Slot</span></span>
<span data-ttu-id="0589a-120">Nome slot WebApp</span><span class="sxs-lookup"><span data-stu-id="0589a-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="0589a-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0589a-121">-WebApp</span></span>
<span data-ttu-id="0589a-122">Oggetto WebApp</span><span class="sxs-lookup"><span data-stu-id="0589a-122">WebApp Object</span></span>

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

### <span data-ttu-id="0589a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0589a-123">CommonParameters</span></span>
<span data-ttu-id="0589a-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0589a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0589a-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0589a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0589a-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="0589a-126">INPUTS</span></span>

### <span data-ttu-id="0589a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="0589a-127">System.String</span></span>

### <span data-ttu-id="0589a-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="0589a-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0589a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0589a-129">OUTPUTS</span></span>

### <span data-ttu-id="0589a-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="0589a-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0589a-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="0589a-131">NOTES</span></span>

## <span data-ttu-id="0589a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0589a-132">RELATED LINKS</span></span>
