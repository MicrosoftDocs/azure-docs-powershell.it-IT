---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: 948088f99e90af4594e239dc379133955340e1d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516319"
---
# <span data-ttu-id="a4fbb-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="a4fbb-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="a4fbb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4fbb-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4fbb-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4fbb-103">SYNTAX</span></span>

### <span data-ttu-id="a4fbb-104">S1</span><span class="sxs-lookup"><span data-stu-id="a4fbb-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4fbb-105">S2</span><span class="sxs-lookup"><span data-stu-id="a4fbb-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4fbb-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4fbb-106">DESCRIPTION</span></span>
<span data-ttu-id="a4fbb-107">Il cmdlet **Reset-AzureRmWebAppSlotPublishingProfile** Reimposta il profilo di pubblicazione per lo slot per l'app Web specificato.</span><span class="sxs-lookup"><span data-stu-id="a4fbb-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="a4fbb-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4fbb-108">EXAMPLES</span></span>

### <span data-ttu-id="a4fbb-109">1:</span><span class="sxs-lookup"><span data-stu-id="a4fbb-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="a4fbb-110">Questo comando Reimposta il profilo di pubblicazione per lo slot denominato slot001 per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="a4fbb-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a4fbb-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4fbb-111">PARAMETERS</span></span>

### <span data-ttu-id="a4fbb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4fbb-112">-DefaultProfile</span></span>
<span data-ttu-id="a4fbb-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4fbb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4fbb-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4fbb-114">-Name</span></span>
<span data-ttu-id="a4fbb-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="a4fbb-115">WebApp Name</span></span>

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

### <span data-ttu-id="a4fbb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4fbb-116">-ResourceGroupName</span></span>
<span data-ttu-id="a4fbb-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a4fbb-117">Resource Group Name</span></span>

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

### <span data-ttu-id="a4fbb-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="a4fbb-118">-Slot</span></span>
<span data-ttu-id="a4fbb-119">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="a4fbb-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="a4fbb-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="a4fbb-120">-WebApp</span></span>
<span data-ttu-id="a4fbb-121">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="a4fbb-121">WebApp Object</span></span>

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

### <span data-ttu-id="a4fbb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4fbb-122">CommonParameters</span></span>
<span data-ttu-id="a4fbb-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4fbb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4fbb-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4fbb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4fbb-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4fbb-125">INPUTS</span></span>

### <span data-ttu-id="a4fbb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a4fbb-126">System.String</span></span>

### <span data-ttu-id="a4fbb-127">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="a4fbb-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="a4fbb-128">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a4fbb-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="a4fbb-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4fbb-129">OUTPUTS</span></span>

### <span data-ttu-id="a4fbb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a4fbb-130">System.String</span></span>

## <span data-ttu-id="a4fbb-131">Note</span><span class="sxs-lookup"><span data-stu-id="a4fbb-131">NOTES</span></span>

## <span data-ttu-id="a4fbb-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4fbb-132">RELATED LINKS</span></span>
