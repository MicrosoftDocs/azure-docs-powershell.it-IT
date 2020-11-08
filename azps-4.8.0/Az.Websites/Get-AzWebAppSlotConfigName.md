---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 9ca0578aacbd0ca970211bc38419880cbe99675b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188662"
---
# <span data-ttu-id="c2af8-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="c2af8-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="c2af8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2af8-102">SYNOPSIS</span></span>
<span data-ttu-id="c2af8-103">Ottenere l'elenco dei nomi di configurazione degli slot Web App</span><span class="sxs-lookup"><span data-stu-id="c2af8-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="c2af8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2af8-104">SYNTAX</span></span>

### <span data-ttu-id="c2af8-105">S1</span><span class="sxs-lookup"><span data-stu-id="c2af8-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2af8-106">S2</span><span class="sxs-lookup"><span data-stu-id="c2af8-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2af8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2af8-107">DESCRIPTION</span></span>
<span data-ttu-id="c2af8-108">Il cmdlet **Get-AzWebAppSlotConfigName** recupera l'elenco delle impostazioni dell'app e dei nomi delle stringhe di connessione attualmente contrassegnati come slot</span><span class="sxs-lookup"><span data-stu-id="c2af8-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="c2af8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2af8-109">EXAMPLES</span></span>

### <span data-ttu-id="c2af8-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c2af8-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="c2af8-111">Questo comando consente di ottenere le impostazioni delle app e le stringhe di connessione relative all'app Web denominata ContosoSite associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="c2af8-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="c2af8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2af8-112">PARAMETERS</span></span>

### <span data-ttu-id="c2af8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2af8-113">-DefaultProfile</span></span>
<span data-ttu-id="c2af8-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2af8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2af8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2af8-115">-Name</span></span>
<span data-ttu-id="c2af8-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="c2af8-116">WebApp Name</span></span>

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

### <span data-ttu-id="c2af8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2af8-117">-ResourceGroupName</span></span>
<span data-ttu-id="c2af8-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c2af8-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c2af8-119">-Web App</span><span class="sxs-lookup"><span data-stu-id="c2af8-119">-WebApp</span></span>
<span data-ttu-id="c2af8-120">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="c2af8-120">WebApp Object</span></span>

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

### <span data-ttu-id="c2af8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2af8-121">CommonParameters</span></span>
<span data-ttu-id="c2af8-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2af8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2af8-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2af8-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2af8-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2af8-124">INPUTS</span></span>

### <span data-ttu-id="c2af8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c2af8-125">System.String</span></span>

### <span data-ttu-id="c2af8-126">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c2af8-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c2af8-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2af8-127">OUTPUTS</span></span>

### <span data-ttu-id="c2af8-128">Microsoft. Azure. Management. website. Models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="c2af8-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="c2af8-129">Note</span><span class="sxs-lookup"><span data-stu-id="c2af8-129">NOTES</span></span>

## <span data-ttu-id="c2af8-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2af8-130">RELATED LINKS</span></span>
