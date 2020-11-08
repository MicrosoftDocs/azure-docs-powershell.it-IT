---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 840e0bb2bfa10a89a5ba963e83ab434e795b3dd4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202708"
---
# <span data-ttu-id="49e7f-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="49e7f-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="49e7f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49e7f-102">SYNOPSIS</span></span>

## <span data-ttu-id="49e7f-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49e7f-103">SYNTAX</span></span>

### <span data-ttu-id="49e7f-104">S1</span><span class="sxs-lookup"><span data-stu-id="49e7f-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49e7f-105">S2</span><span class="sxs-lookup"><span data-stu-id="49e7f-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49e7f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49e7f-106">DESCRIPTION</span></span>
<span data-ttu-id="49e7f-107">Il cmdlet **Reset-AzWebAppSlotPublishingProfile** Reimposta il profilo di pubblicazione per lo slot per l'app Web specificato.</span><span class="sxs-lookup"><span data-stu-id="49e7f-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="49e7f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49e7f-108">EXAMPLES</span></span>

### <span data-ttu-id="49e7f-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="49e7f-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="49e7f-110">Questo comando Reimposta il profilo di pubblicazione per lo slot denominato slot001 per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="49e7f-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="49e7f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49e7f-111">PARAMETERS</span></span>

### <span data-ttu-id="49e7f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49e7f-112">-DefaultProfile</span></span>
<span data-ttu-id="49e7f-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49e7f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49e7f-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="49e7f-114">-Name</span></span>
<span data-ttu-id="49e7f-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="49e7f-115">WebApp Name</span></span>

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

### <span data-ttu-id="49e7f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49e7f-116">-ResourceGroupName</span></span>
<span data-ttu-id="49e7f-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="49e7f-117">Resource Group Name</span></span>

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

### <span data-ttu-id="49e7f-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="49e7f-118">-Slot</span></span>
<span data-ttu-id="49e7f-119">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="49e7f-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="49e7f-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="49e7f-120">-WebApp</span></span>
<span data-ttu-id="49e7f-121">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="49e7f-121">WebApp Object</span></span>

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

### <span data-ttu-id="49e7f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e7f-122">CommonParameters</span></span>
<span data-ttu-id="49e7f-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49e7f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49e7f-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49e7f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e7f-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49e7f-125">INPUTS</span></span>

### <span data-ttu-id="49e7f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="49e7f-126">System.String</span></span>

### <span data-ttu-id="49e7f-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="49e7f-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="49e7f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49e7f-128">OUTPUTS</span></span>

### <span data-ttu-id="49e7f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="49e7f-129">System.String</span></span>

## <span data-ttu-id="49e7f-130">Note</span><span class="sxs-lookup"><span data-stu-id="49e7f-130">NOTES</span></span>

## <span data-ttu-id="49e7f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49e7f-131">RELATED LINKS</span></span>
