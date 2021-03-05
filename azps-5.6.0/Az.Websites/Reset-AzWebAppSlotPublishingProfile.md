---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: bdee1c1fdda561d7265b3f6ff52a443238b6d2b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995817"
---
# <span data-ttu-id="e8adc-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="e8adc-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="e8adc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8adc-102">SYNOPSIS</span></span>

## <span data-ttu-id="e8adc-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8adc-103">SYNTAX</span></span>

### <span data-ttu-id="e8adc-104">S1</span><span class="sxs-lookup"><span data-stu-id="e8adc-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8adc-105">S2</span><span class="sxs-lookup"><span data-stu-id="e8adc-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8adc-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e8adc-106">DESCRIPTION</span></span>
<span data-ttu-id="e8adc-107">Il cmdlet **Reset-AzWebAppSlotPublishingProfile** reimposta il profilo di pubblicazione per lo slot app Web specificato.</span><span class="sxs-lookup"><span data-stu-id="e8adc-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="e8adc-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8adc-108">EXAMPLES</span></span>

### <span data-ttu-id="e8adc-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e8adc-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="e8adc-110">Questo comando reimposta il profilo di pubblicazione per lo slot denominato slot001 per l'app Web ContosoWebApp associata al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="e8adc-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e8adc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8adc-111">PARAMETERS</span></span>

### <span data-ttu-id="e8adc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8adc-112">-DefaultProfile</span></span>
<span data-ttu-id="e8adc-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8adc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8adc-114">-Name</span><span class="sxs-lookup"><span data-stu-id="e8adc-114">-Name</span></span>
<span data-ttu-id="e8adc-115">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="e8adc-115">WebApp Name</span></span>

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

### <span data-ttu-id="e8adc-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8adc-116">-ResourceGroupName</span></span>
<span data-ttu-id="e8adc-117">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e8adc-117">Resource Group Name</span></span>

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

### <span data-ttu-id="e8adc-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="e8adc-118">-Slot</span></span>
<span data-ttu-id="e8adc-119">Nome slot WebApp</span><span class="sxs-lookup"><span data-stu-id="e8adc-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="e8adc-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e8adc-120">-WebApp</span></span>
<span data-ttu-id="e8adc-121">Oggetto WebApp</span><span class="sxs-lookup"><span data-stu-id="e8adc-121">WebApp Object</span></span>

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

### <span data-ttu-id="e8adc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8adc-122">CommonParameters</span></span>
<span data-ttu-id="e8adc-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8adc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8adc-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8adc-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8adc-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="e8adc-125">INPUTS</span></span>

### <span data-ttu-id="e8adc-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e8adc-126">System.String</span></span>

### <span data-ttu-id="e8adc-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e8adc-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e8adc-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8adc-128">OUTPUTS</span></span>

### <span data-ttu-id="e8adc-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e8adc-129">System.String</span></span>

## <span data-ttu-id="e8adc-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="e8adc-130">NOTES</span></span>

## <span data-ttu-id="e8adc-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8adc-131">RELATED LINKS</span></span>
