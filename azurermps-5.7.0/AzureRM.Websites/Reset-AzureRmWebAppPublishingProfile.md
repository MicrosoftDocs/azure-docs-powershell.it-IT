---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: b519012104472d9b97f5f0a5e4b699829b99fff4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520315"
---
# <span data-ttu-id="a8c1d-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="a8c1d-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="a8c1d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8c1d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8c1d-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8c1d-103">SYNTAX</span></span>

### <span data-ttu-id="a8c1d-104">S1</span><span class="sxs-lookup"><span data-stu-id="a8c1d-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8c1d-105">S2</span><span class="sxs-lookup"><span data-stu-id="a8c1d-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8c1d-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8c1d-106">DESCRIPTION</span></span>
<span data-ttu-id="a8c1d-107">Il cmdlet **Reset-AzureRmWebAppPublishingProfile** Reimposta il profilo di pubblicazione per l'app Web specificata.</span><span class="sxs-lookup"><span data-stu-id="a8c1d-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="a8c1d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8c1d-108">EXAMPLES</span></span>

### <span data-ttu-id="a8c1d-109">1:</span><span class="sxs-lookup"><span data-stu-id="a8c1d-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="a8c1d-110">Questo comando Reimposta il profilo di pubblicazione per l'app Web ContosoWebApp associato al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="a8c1d-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a8c1d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8c1d-111">PARAMETERS</span></span>

### <span data-ttu-id="a8c1d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8c1d-112">-DefaultProfile</span></span>
<span data-ttu-id="a8c1d-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8c1d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c1d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8c1d-114">-Name</span></span>
<span data-ttu-id="a8c1d-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="a8c1d-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8c1d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8c1d-116">-ResourceGroupName</span></span>
<span data-ttu-id="a8c1d-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a8c1d-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c1d-118">-Web App</span><span class="sxs-lookup"><span data-stu-id="a8c1d-118">-WebApp</span></span>
<span data-ttu-id="a8c1d-119">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="a8c1d-119">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8c1d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c1d-120">CommonParameters</span></span>
<span data-ttu-id="a8c1d-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8c1d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c1d-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8c1d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c1d-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8c1d-123">INPUTS</span></span>

### <span data-ttu-id="a8c1d-124">Sito</span><span class="sxs-lookup"><span data-stu-id="a8c1d-124">Site</span></span>
<span data-ttu-id="a8c1d-125">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a8c1d-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a8c1d-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8c1d-126">OUTPUTS</span></span>

## <span data-ttu-id="a8c1d-127">Note</span><span class="sxs-lookup"><span data-stu-id="a8c1d-127">NOTES</span></span>

## <span data-ttu-id="a8c1d-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8c1d-128">RELATED LINKS</span></span>

