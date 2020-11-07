---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 0d67d2de8aebd251f4c02f19ff6a544325f2db5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857862"
---
# <span data-ttu-id="639a3-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="639a3-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="639a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="639a3-102">SYNOPSIS</span></span>

## <span data-ttu-id="639a3-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="639a3-103">SYNTAX</span></span>

### <span data-ttu-id="639a3-104">S1</span><span class="sxs-lookup"><span data-stu-id="639a3-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="639a3-105">S2</span><span class="sxs-lookup"><span data-stu-id="639a3-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="639a3-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="639a3-106">DESCRIPTION</span></span>
<span data-ttu-id="639a3-107">Il cmdlet **Reset-AzWebAppSlotPublishingProfile** Reimposta il profilo di pubblicazione per lo slot per l'app Web specificato.</span><span class="sxs-lookup"><span data-stu-id="639a3-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="639a3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="639a3-108">EXAMPLES</span></span>

### <span data-ttu-id="639a3-109">1:</span><span class="sxs-lookup"><span data-stu-id="639a3-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="639a3-110">Questo comando Reimposta il profilo di pubblicazione per lo slot denominato slot001 per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="639a3-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="639a3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="639a3-111">PARAMETERS</span></span>

### <span data-ttu-id="639a3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="639a3-112">-DefaultProfile</span></span>
<span data-ttu-id="639a3-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="639a3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="639a3-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="639a3-114">-Name</span></span>
<span data-ttu-id="639a3-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="639a3-115">WebApp Name</span></span>

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

### <span data-ttu-id="639a3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="639a3-116">-ResourceGroupName</span></span>
<span data-ttu-id="639a3-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="639a3-117">Resource Group Name</span></span>

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

### <span data-ttu-id="639a3-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="639a3-118">-Slot</span></span>
<span data-ttu-id="639a3-119">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="639a3-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="639a3-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="639a3-120">-WebApp</span></span>
<span data-ttu-id="639a3-121">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="639a3-121">WebApp Object</span></span>

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

### <span data-ttu-id="639a3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="639a3-122">CommonParameters</span></span>
<span data-ttu-id="639a3-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="639a3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="639a3-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="639a3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="639a3-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="639a3-125">INPUTS</span></span>

### <span data-ttu-id="639a3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="639a3-126">System.String</span></span>

### <span data-ttu-id="639a3-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="639a3-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="639a3-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="639a3-128">OUTPUTS</span></span>

### <span data-ttu-id="639a3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="639a3-129">System.String</span></span>

## <span data-ttu-id="639a3-130">Note</span><span class="sxs-lookup"><span data-stu-id="639a3-130">NOTES</span></span>

## <span data-ttu-id="639a3-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="639a3-131">RELATED LINKS</span></span>
