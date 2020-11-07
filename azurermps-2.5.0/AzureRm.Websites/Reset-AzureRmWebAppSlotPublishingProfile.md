---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebappslotpublishingprofile
schema: 2.0.0
ms.openlocfilehash: 7c385f230456da60df76c56fc652dda53362c778
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866950"
---
# <span data-ttu-id="6a30b-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="6a30b-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="6a30b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a30b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a30b-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a30b-103">SYNTAX</span></span>

### <span data-ttu-id="6a30b-104">S1</span><span class="sxs-lookup"><span data-stu-id="6a30b-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a30b-105">S2</span><span class="sxs-lookup"><span data-stu-id="6a30b-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a30b-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a30b-106">DESCRIPTION</span></span>
<span data-ttu-id="6a30b-107">Il cmdlet **Reset-AzureRmWebAppSlotPublishingProfile** Reimposta il profilo di pubblicazione per lo slot per l'app Web specificato.</span><span class="sxs-lookup"><span data-stu-id="6a30b-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="6a30b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a30b-108">EXAMPLES</span></span>

### <span data-ttu-id="6a30b-109">1:</span><span class="sxs-lookup"><span data-stu-id="6a30b-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="6a30b-110">Questo comando Reimposta il profilo di pubblicazione per lo slot denominato slot001 per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="6a30b-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="6a30b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a30b-111">PARAMETERS</span></span>

### <span data-ttu-id="6a30b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a30b-112">-DefaultProfile</span></span>
<span data-ttu-id="6a30b-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a30b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a30b-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a30b-114">-Name</span></span>
<span data-ttu-id="6a30b-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="6a30b-115">WebApp Name</span></span>

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

### <span data-ttu-id="6a30b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a30b-116">-ResourceGroupName</span></span>
<span data-ttu-id="6a30b-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="6a30b-117">Resource Group Name</span></span>

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

### <span data-ttu-id="6a30b-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="6a30b-118">-Slot</span></span>
<span data-ttu-id="6a30b-119">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="6a30b-119">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a30b-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="6a30b-120">-WebApp</span></span>
<span data-ttu-id="6a30b-121">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="6a30b-121">WebApp Object</span></span>

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

### <span data-ttu-id="6a30b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a30b-122">CommonParameters</span></span>
<span data-ttu-id="6a30b-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a30b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a30b-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a30b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a30b-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a30b-125">INPUTS</span></span>

### <span data-ttu-id="6a30b-126">Sito</span><span class="sxs-lookup"><span data-stu-id="6a30b-126">Site</span></span>
<span data-ttu-id="6a30b-127">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6a30b-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6a30b-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a30b-128">OUTPUTS</span></span>

## <span data-ttu-id="6a30b-129">Note</span><span class="sxs-lookup"><span data-stu-id="6a30b-129">NOTES</span></span>

## <span data-ttu-id="6a30b-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a30b-130">RELATED LINKS</span></span>

