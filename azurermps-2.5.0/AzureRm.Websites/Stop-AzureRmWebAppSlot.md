---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: c59e40765fc5da07c5d079e3b5abd6224a8cbc5f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866612"
---
# <span data-ttu-id="a6219-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a6219-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="a6219-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6219-102">SYNOPSIS</span></span>
<span data-ttu-id="a6219-103">Interrompe uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a6219-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6219-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6219-104">SYNTAX</span></span>

### <span data-ttu-id="a6219-105">S1</span><span class="sxs-lookup"><span data-stu-id="a6219-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6219-106">S2</span><span class="sxs-lookup"><span data-stu-id="a6219-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6219-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6219-107">DESCRIPTION</span></span>
<span data-ttu-id="a6219-108">Il cmdlet **Stop-AzureRmWebAppSlot** arresta uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a6219-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="a6219-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6219-109">EXAMPLES</span></span>

### <span data-ttu-id="a6219-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a6219-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="a6219-111">Questo comando Arresta lo slot Slot001 pertinente all'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="a6219-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a6219-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6219-112">PARAMETERS</span></span>

### <span data-ttu-id="a6219-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6219-113">-DefaultProfile</span></span>
<span data-ttu-id="a6219-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6219-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6219-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6219-115">-Name</span></span>
<span data-ttu-id="a6219-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="a6219-116">WebApp Name</span></span>

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

### <span data-ttu-id="a6219-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6219-117">-ResourceGroupName</span></span>
<span data-ttu-id="a6219-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a6219-118">Resource Group Name</span></span>

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

### <span data-ttu-id="a6219-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="a6219-119">-Slot</span></span>
<span data-ttu-id="a6219-120">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="a6219-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="a6219-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="a6219-121">-WebApp</span></span>
<span data-ttu-id="a6219-122">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="a6219-122">WebApp Object</span></span>

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

### <span data-ttu-id="a6219-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6219-123">CommonParameters</span></span>
<span data-ttu-id="a6219-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6219-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6219-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6219-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6219-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6219-126">INPUTS</span></span>

### <span data-ttu-id="a6219-127">Sito</span><span class="sxs-lookup"><span data-stu-id="a6219-127">Site</span></span>
<span data-ttu-id="a6219-128">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a6219-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a6219-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6219-129">OUTPUTS</span></span>

## <span data-ttu-id="a6219-130">Note</span><span class="sxs-lookup"><span data-stu-id="a6219-130">NOTES</span></span>

## <span data-ttu-id="a6219-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6219-131">RELATED LINKS</span></span>

