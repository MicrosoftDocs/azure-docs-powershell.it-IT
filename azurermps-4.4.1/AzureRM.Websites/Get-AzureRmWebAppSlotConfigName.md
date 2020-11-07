---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 196e653447204b65c7f431e29fe76078a268dda1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687965"
---
# <span data-ttu-id="ac4eb-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="ac4eb-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="ac4eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ac4eb-103">Ottenere l'elenco dei nomi di configurazione degli slot Web App</span><span class="sxs-lookup"><span data-stu-id="ac4eb-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac4eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac4eb-104">SYNTAX</span></span>

### <span data-ttu-id="ac4eb-105">S1</span><span class="sxs-lookup"><span data-stu-id="ac4eb-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac4eb-106">S2</span><span class="sxs-lookup"><span data-stu-id="ac4eb-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac4eb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac4eb-107">DESCRIPTION</span></span>
<span data-ttu-id="ac4eb-108">Il cmdlet **Get-AzureRmWebAppSlotConfigName** recupera l'elenco delle impostazioni dell'app e dei nomi delle stringhe di connessione attualmente contrassegnati come slot</span><span class="sxs-lookup"><span data-stu-id="ac4eb-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="ac4eb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac4eb-109">EXAMPLES</span></span>

### <span data-ttu-id="ac4eb-110">1:</span><span class="sxs-lookup"><span data-stu-id="ac4eb-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="ac4eb-111">Questo comando consente di ottenere le impostazioni delle app e le stringhe di connessione relative all'app Web denominata ContosoSite associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="ac4eb-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ac4eb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac4eb-112">PARAMETERS</span></span>

### <span data-ttu-id="ac4eb-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac4eb-113">-Name</span></span>
<span data-ttu-id="ac4eb-114">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="ac4eb-114">WebApp Name</span></span>

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

### <span data-ttu-id="ac4eb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac4eb-115">-ResourceGroupName</span></span>
<span data-ttu-id="ac4eb-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ac4eb-116">Resource Group Name</span></span>

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

### <span data-ttu-id="ac4eb-117">-Web App</span><span class="sxs-lookup"><span data-stu-id="ac4eb-117">-WebApp</span></span>
<span data-ttu-id="ac4eb-118">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="ac4eb-118">WebApp Object</span></span>

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

### <span data-ttu-id="ac4eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac4eb-119">-DefaultProfile</span></span>
<span data-ttu-id="ac4eb-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac4eb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac4eb-121">CommonParameters</span></span>
<span data-ttu-id="ac4eb-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac4eb-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac4eb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac4eb-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac4eb-124">INPUTS</span></span>

### <span data-ttu-id="ac4eb-125">Sito</span><span class="sxs-lookup"><span data-stu-id="ac4eb-125">Site</span></span>
<span data-ttu-id="ac4eb-126">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ac4eb-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ac4eb-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac4eb-127">OUTPUTS</span></span>

## <span data-ttu-id="ac4eb-128">Note</span><span class="sxs-lookup"><span data-stu-id="ac4eb-128">NOTES</span></span>

## <span data-ttu-id="ac4eb-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac4eb-129">RELATED LINKS</span></span>

