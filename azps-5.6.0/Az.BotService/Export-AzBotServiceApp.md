---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/export-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
ms.openlocfilehash: 79ef8a92997790f547847e05eae6ca101016bc42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960877"
---
# <span data-ttu-id="2574b-101">Export-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="2574b-101">Export-AzBotServiceApp</span></span>

## <span data-ttu-id="2574b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2574b-102">SYNOPSIS</span></span>
<span data-ttu-id="2574b-103">Restituisce un servizio BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="2574b-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="2574b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2574b-104">SYNTAX</span></span>

```
Export-AzBotServiceApp [-Name <String>] [-ResourceGroupName <String>] [-SavePath <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2574b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2574b-105">DESCRIPTION</span></span>
<span data-ttu-id="2574b-106">Restituisce un servizio BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="2574b-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="2574b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2574b-107">EXAMPLES</span></span>

### <span data-ttu-id="2574b-108">Esempio 1: Scaricare la cartella dell'app BotService</span><span class="sxs-lookup"><span data-stu-id="2574b-108">Example 1: DownLoad the BotService App folder</span></span>
```powershell
PS C:\> Export-AzBotServiceApp -ResourceGroupName youriBotTest -name youriechobottest

Parameter $SavePath not provided, defaulting to current working directory.

    Directory: D:\powershell\BotService\azure-powershell\src\BotService

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2020/12/15    13:45                youriechobottest
```

<span data-ttu-id="2574b-109">DownLoad the BotService App folder</span><span class="sxs-lookup"><span data-stu-id="2574b-109">DownLoad the BotService App folder</span></span>

## <span data-ttu-id="2574b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2574b-110">PARAMETERS</span></span>

### <span data-ttu-id="2574b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2574b-111">-DefaultProfile</span></span>
<span data-ttu-id="2574b-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2574b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2574b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="2574b-113">-Name</span></span>
<span data-ttu-id="2574b-114">Nome della risorsa Bot.</span><span class="sxs-lookup"><span data-stu-id="2574b-114">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2574b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2574b-115">-ResourceGroupName</span></span>
<span data-ttu-id="2574b-116">Nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2574b-116">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2574b-117">-SavePath</span><span class="sxs-lookup"><span data-stu-id="2574b-117">-SavePath</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2574b-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2574b-118">-SubscriptionId</span></span>
<span data-ttu-id="2574b-119">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="2574b-119">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2574b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2574b-120">CommonParameters</span></span>
<span data-ttu-id="2574b-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2574b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2574b-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2574b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2574b-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="2574b-123">INPUTS</span></span>

## <span data-ttu-id="2574b-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2574b-124">OUTPUTS</span></span>

### <span data-ttu-id="2574b-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="2574b-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="2574b-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="2574b-126">NOTES</span></span>

<span data-ttu-id="2574b-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2574b-127">ALIASES</span></span>

## <span data-ttu-id="2574b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2574b-128">RELATED LINKS</span></span>

