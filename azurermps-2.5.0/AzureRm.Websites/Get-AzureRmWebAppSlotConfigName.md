---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotconfigname
schema: 2.0.0
ms.openlocfilehash: ff05a30c495475b63b0385f3398c78e0b018a4bc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866626"
---
# <span data-ttu-id="fe97c-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="fe97c-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="fe97c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe97c-102">SYNOPSIS</span></span>
<span data-ttu-id="fe97c-103">Ottenere l'elenco dei nomi di configurazione degli slot Web App</span><span class="sxs-lookup"><span data-stu-id="fe97c-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe97c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe97c-104">SYNTAX</span></span>

### <span data-ttu-id="fe97c-105">S1</span><span class="sxs-lookup"><span data-stu-id="fe97c-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe97c-106">S2</span><span class="sxs-lookup"><span data-stu-id="fe97c-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe97c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe97c-107">DESCRIPTION</span></span>
<span data-ttu-id="fe97c-108">Il cmdlet **Get-AzureRmWebAppSlotConfigName** recupera l'elenco delle impostazioni dell'app e dei nomi delle stringhe di connessione attualmente contrassegnati come slot</span><span class="sxs-lookup"><span data-stu-id="fe97c-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="fe97c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe97c-109">EXAMPLES</span></span>

### <span data-ttu-id="fe97c-110">1:</span><span class="sxs-lookup"><span data-stu-id="fe97c-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="fe97c-111">Questo comando consente di ottenere le impostazioni delle app e le stringhe di connessione relative all'app Web denominata ContosoSite associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="fe97c-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="fe97c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe97c-112">PARAMETERS</span></span>

### <span data-ttu-id="fe97c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe97c-113">-DefaultProfile</span></span>
<span data-ttu-id="fe97c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe97c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe97c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe97c-115">-Name</span></span>
<span data-ttu-id="fe97c-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="fe97c-116">WebApp Name</span></span>

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

### <span data-ttu-id="fe97c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe97c-117">-ResourceGroupName</span></span>
<span data-ttu-id="fe97c-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="fe97c-118">Resource Group Name</span></span>

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

### <span data-ttu-id="fe97c-119">-Web App</span><span class="sxs-lookup"><span data-stu-id="fe97c-119">-WebApp</span></span>
<span data-ttu-id="fe97c-120">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="fe97c-120">WebApp Object</span></span>

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

### <span data-ttu-id="fe97c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe97c-121">CommonParameters</span></span>
<span data-ttu-id="fe97c-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe97c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe97c-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe97c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe97c-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe97c-124">INPUTS</span></span>

### <span data-ttu-id="fe97c-125">Sito</span><span class="sxs-lookup"><span data-stu-id="fe97c-125">Site</span></span>
<span data-ttu-id="fe97c-126">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fe97c-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="fe97c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe97c-127">OUTPUTS</span></span>

## <span data-ttu-id="fe97c-128">Note</span><span class="sxs-lookup"><span data-stu-id="fe97c-128">NOTES</span></span>

## <span data-ttu-id="fe97c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe97c-129">RELATED LINKS</span></span>

