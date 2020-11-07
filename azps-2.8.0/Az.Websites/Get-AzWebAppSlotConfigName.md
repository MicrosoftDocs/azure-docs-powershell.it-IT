---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: bd871e75e5a4f9c8e5c28e8788c8ef291a88e6db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858537"
---
# <span data-ttu-id="5e34a-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="5e34a-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="5e34a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e34a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e34a-103">Ottenere l'elenco dei nomi di configurazione degli slot Web App</span><span class="sxs-lookup"><span data-stu-id="5e34a-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="5e34a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e34a-104">SYNTAX</span></span>

### <span data-ttu-id="5e34a-105">S1</span><span class="sxs-lookup"><span data-stu-id="5e34a-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e34a-106">S2</span><span class="sxs-lookup"><span data-stu-id="5e34a-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e34a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e34a-107">DESCRIPTION</span></span>
<span data-ttu-id="5e34a-108">Il cmdlet **Get-AzWebAppSlotConfigName** recupera l'elenco delle impostazioni dell'app e dei nomi delle stringhe di connessione attualmente contrassegnati come slot</span><span class="sxs-lookup"><span data-stu-id="5e34a-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="5e34a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e34a-109">EXAMPLES</span></span>

### <span data-ttu-id="5e34a-110">1:</span><span class="sxs-lookup"><span data-stu-id="5e34a-110">1:</span></span>
```
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="5e34a-111">Questo comando consente di ottenere le impostazioni delle app e le stringhe di connessione relative all'app Web denominata ContosoSite associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="5e34a-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="5e34a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e34a-112">PARAMETERS</span></span>

### <span data-ttu-id="5e34a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e34a-113">-DefaultProfile</span></span>
<span data-ttu-id="5e34a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e34a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e34a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e34a-115">-Name</span></span>
<span data-ttu-id="5e34a-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="5e34a-116">WebApp Name</span></span>

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

### <span data-ttu-id="5e34a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e34a-117">-ResourceGroupName</span></span>
<span data-ttu-id="5e34a-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="5e34a-118">Resource Group Name</span></span>

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

### <span data-ttu-id="5e34a-119">-Web App</span><span class="sxs-lookup"><span data-stu-id="5e34a-119">-WebApp</span></span>
<span data-ttu-id="5e34a-120">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="5e34a-120">WebApp Object</span></span>

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

### <span data-ttu-id="5e34a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e34a-121">CommonParameters</span></span>
<span data-ttu-id="5e34a-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e34a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e34a-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e34a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e34a-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e34a-124">INPUTS</span></span>

### <span data-ttu-id="5e34a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5e34a-125">System.String</span></span>

### <span data-ttu-id="5e34a-126">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="5e34a-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5e34a-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e34a-127">OUTPUTS</span></span>

### <span data-ttu-id="5e34a-128">Microsoft. Azure. Management. website. Models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="5e34a-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="5e34a-129">Note</span><span class="sxs-lookup"><span data-stu-id="5e34a-129">NOTES</span></span>

## <span data-ttu-id="5e34a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e34a-130">RELATED LINKS</span></span>
