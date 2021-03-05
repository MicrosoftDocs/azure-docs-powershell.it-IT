---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 2157c7a570f38838a65e1d4bba40dade22e10367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962573"
---
# <span data-ttu-id="c25c7-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="c25c7-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="c25c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c25c7-102">SYNOPSIS</span></span>
<span data-ttu-id="c25c7-103">Ottenere l'elenco dei nomi di configurazione degli slot per le app Web</span><span class="sxs-lookup"><span data-stu-id="c25c7-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="c25c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c25c7-104">SYNTAX</span></span>

### <span data-ttu-id="c25c7-105">S1</span><span class="sxs-lookup"><span data-stu-id="c25c7-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c25c7-106">S2</span><span class="sxs-lookup"><span data-stu-id="c25c7-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c25c7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c25c7-107">DESCRIPTION</span></span>
<span data-ttu-id="c25c7-108">Il cmdlet **Get-AzWebAppSlotConfigName** recupera l'elenco dei nomi delle impostazioni delle app e delle stringhe di connessione attualmente contrassegnati come impostazioni di slot</span><span class="sxs-lookup"><span data-stu-id="c25c7-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="c25c7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c25c7-109">EXAMPLES</span></span>

### <span data-ttu-id="c25c7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c25c7-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="c25c7-111">Questo comando recupera le impostazioni dell'app e le stringhe di connessione relative all'app Web denominata ContosoSite associata al gruppo di risorse Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="c25c7-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="c25c7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c25c7-112">PARAMETERS</span></span>

### <span data-ttu-id="c25c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c25c7-113">-DefaultProfile</span></span>
<span data-ttu-id="c25c7-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c25c7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c25c7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c25c7-115">-Name</span></span>
<span data-ttu-id="c25c7-116">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="c25c7-116">WebApp Name</span></span>

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

### <span data-ttu-id="c25c7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c25c7-117">-ResourceGroupName</span></span>
<span data-ttu-id="c25c7-118">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c25c7-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c25c7-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c25c7-119">-WebApp</span></span>
<span data-ttu-id="c25c7-120">Oggetto WebApp</span><span class="sxs-lookup"><span data-stu-id="c25c7-120">WebApp Object</span></span>

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

### <span data-ttu-id="c25c7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c25c7-121">CommonParameters</span></span>
<span data-ttu-id="c25c7-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c25c7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c25c7-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c25c7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c25c7-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="c25c7-124">INPUTS</span></span>

### <span data-ttu-id="c25c7-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c25c7-125">System.String</span></span>

### <span data-ttu-id="c25c7-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c25c7-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c25c7-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c25c7-127">OUTPUTS</span></span>

### <span data-ttu-id="c25c7-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="c25c7-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="c25c7-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="c25c7-129">NOTES</span></span>

## <span data-ttu-id="c25c7-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c25c7-130">RELATED LINKS</span></span>
