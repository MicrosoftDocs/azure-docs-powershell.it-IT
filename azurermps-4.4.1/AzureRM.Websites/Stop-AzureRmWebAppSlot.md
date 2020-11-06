---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
ms.openlocfilehash: 91a8c53bc8600006a3a57a5dfefb1141652ca3d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508472"
---
# <span data-ttu-id="bcf72-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bcf72-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="bcf72-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bcf72-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf72-103">Interrompe uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bcf72-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcf72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcf72-104">SYNTAX</span></span>

### <span data-ttu-id="bcf72-105">S1</span><span class="sxs-lookup"><span data-stu-id="bcf72-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcf72-106">S2</span><span class="sxs-lookup"><span data-stu-id="bcf72-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcf72-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcf72-107">DESCRIPTION</span></span>
<span data-ttu-id="bcf72-108">Il cmdlet **Stop-AzureRmWebAppSlot** arresta uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bcf72-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="bcf72-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcf72-109">EXAMPLES</span></span>

### <span data-ttu-id="bcf72-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bcf72-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="bcf72-111">Questo comando Arresta lo slot Slot001 pertinente all'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="bcf72-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="bcf72-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bcf72-112">PARAMETERS</span></span>

### <span data-ttu-id="bcf72-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="bcf72-113">-Name</span></span>
<span data-ttu-id="bcf72-114">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="bcf72-114">WebApp Name</span></span>

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

### <span data-ttu-id="bcf72-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf72-115">-ResourceGroupName</span></span>
<span data-ttu-id="bcf72-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="bcf72-116">Resource Group Name</span></span>

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

### <span data-ttu-id="bcf72-117">-Slot</span><span class="sxs-lookup"><span data-stu-id="bcf72-117">-Slot</span></span>
<span data-ttu-id="bcf72-118">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="bcf72-118">WebApp Slot Name</span></span>

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

### <span data-ttu-id="bcf72-119">-Web App</span><span class="sxs-lookup"><span data-stu-id="bcf72-119">-WebApp</span></span>
<span data-ttu-id="bcf72-120">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="bcf72-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf72-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf72-121">-DefaultProfile</span></span>
<span data-ttu-id="bcf72-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bcf72-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcf72-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf72-123">CommonParameters</span></span>
<span data-ttu-id="bcf72-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcf72-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf72-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcf72-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf72-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bcf72-126">INPUTS</span></span>

### <span data-ttu-id="bcf72-127">Sito</span><span class="sxs-lookup"><span data-stu-id="bcf72-127">Site</span></span>
<span data-ttu-id="bcf72-128">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="bcf72-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="bcf72-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcf72-129">OUTPUTS</span></span>

## <span data-ttu-id="bcf72-130">Note</span><span class="sxs-lookup"><span data-stu-id="bcf72-130">NOTES</span></span>

## <span data-ttu-id="bcf72-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcf72-131">RELATED LINKS</span></span>

