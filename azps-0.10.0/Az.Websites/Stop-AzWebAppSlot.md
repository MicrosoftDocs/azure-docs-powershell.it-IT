---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: 4ac4482cb5972553b1dad3972200d2f0eb032fe4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861801"
---
# <span data-ttu-id="6467a-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6467a-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="6467a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6467a-102">SYNOPSIS</span></span>
<span data-ttu-id="6467a-103">Interrompe uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="6467a-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="6467a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6467a-104">SYNTAX</span></span>

### <span data-ttu-id="6467a-105">S1</span><span class="sxs-lookup"><span data-stu-id="6467a-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6467a-106">S2</span><span class="sxs-lookup"><span data-stu-id="6467a-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6467a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6467a-107">DESCRIPTION</span></span>
<span data-ttu-id="6467a-108">Il cmdlet **Stop-AzWebAppSlot** arresta uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="6467a-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="6467a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6467a-109">EXAMPLES</span></span>

### <span data-ttu-id="6467a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6467a-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="6467a-111">Questo comando Arresta lo slot Slot001 pertinente all'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="6467a-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="6467a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6467a-112">PARAMETERS</span></span>

### <span data-ttu-id="6467a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6467a-113">-DefaultProfile</span></span>
<span data-ttu-id="6467a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6467a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6467a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6467a-115">-Name</span></span>
<span data-ttu-id="6467a-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="6467a-116">WebApp Name</span></span>

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

### <span data-ttu-id="6467a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6467a-117">-ResourceGroupName</span></span>
<span data-ttu-id="6467a-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="6467a-118">Resource Group Name</span></span>

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

### <span data-ttu-id="6467a-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="6467a-119">-Slot</span></span>
<span data-ttu-id="6467a-120">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="6467a-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="6467a-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="6467a-121">-WebApp</span></span>
<span data-ttu-id="6467a-122">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="6467a-122">WebApp Object</span></span>

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

### <span data-ttu-id="6467a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6467a-123">CommonParameters</span></span>
<span data-ttu-id="6467a-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6467a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6467a-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6467a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6467a-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6467a-126">INPUTS</span></span>

### <span data-ttu-id="6467a-127">Sito</span><span class="sxs-lookup"><span data-stu-id="6467a-127">Site</span></span>
<span data-ttu-id="6467a-128">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6467a-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6467a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6467a-129">OUTPUTS</span></span>

## <span data-ttu-id="6467a-130">Note</span><span class="sxs-lookup"><span data-stu-id="6467a-130">NOTES</span></span>

## <span data-ttu-id="6467a-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6467a-131">RELATED LINKS</span></span>

