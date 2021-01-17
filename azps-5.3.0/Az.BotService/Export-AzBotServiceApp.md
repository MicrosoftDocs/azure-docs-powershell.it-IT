---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/export-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
ms.openlocfilehash: dd922730f03b715924a69219c0b1f1ccb11534de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488707"
---
# <span data-ttu-id="de1ef-101">Export-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="de1ef-101">Export-AzBotServiceApp</span></span>

## <span data-ttu-id="de1ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de1ef-102">SYNOPSIS</span></span>
<span data-ttu-id="de1ef-103">Restituisce un BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="de1ef-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="de1ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de1ef-104">SYNTAX</span></span>

```
Export-AzBotServiceApp [-Name <String>] [-ResourceGroupName <String>] [-SavePath <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="de1ef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de1ef-105">DESCRIPTION</span></span>
<span data-ttu-id="de1ef-106">Restituisce un BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="de1ef-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="de1ef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de1ef-107">EXAMPLES</span></span>

### <span data-ttu-id="de1ef-108">Esempio 1: scaricare la cartella dell'app BotService</span><span class="sxs-lookup"><span data-stu-id="de1ef-108">Example 1: DownLoad the BotService App folder</span></span>
```powershell
PS C:\> Export-AzBotServiceApp -ResourceGroupName youriBotTest -name youriechobottest

Parameter $SavePath not provided, defaulting to current working directory.

    Directory: D:\powershell\BotService\azure-powershell\src\BotService

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2020/12/15    13:45                youriechobottest
```

<span data-ttu-id="de1ef-109">Scaricare la cartella dell'app BotService</span><span class="sxs-lookup"><span data-stu-id="de1ef-109">DownLoad the BotService App folder</span></span>

## <span data-ttu-id="de1ef-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de1ef-110">PARAMETERS</span></span>

### <span data-ttu-id="de1ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de1ef-111">-DefaultProfile</span></span>
<span data-ttu-id="de1ef-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de1ef-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de1ef-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="de1ef-113">-Name</span></span>
<span data-ttu-id="de1ef-114">Il nome della risorsa bot.</span><span class="sxs-lookup"><span data-stu-id="de1ef-114">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="de1ef-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de1ef-115">-ResourceGroupName</span></span>
<span data-ttu-id="de1ef-116">Nome del gruppo di risorse bot nell'abbonamento utente.</span><span class="sxs-lookup"><span data-stu-id="de1ef-116">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="de1ef-117">-SavePath</span><span class="sxs-lookup"><span data-stu-id="de1ef-117">-SavePath</span></span>


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

### <span data-ttu-id="de1ef-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de1ef-118">-SubscriptionId</span></span>
<span data-ttu-id="de1ef-119">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="de1ef-119">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="de1ef-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de1ef-120">CommonParameters</span></span>
<span data-ttu-id="de1ef-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de1ef-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de1ef-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de1ef-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de1ef-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de1ef-123">INPUTS</span></span>

## <span data-ttu-id="de1ef-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de1ef-124">OUTPUTS</span></span>

### <span data-ttu-id="de1ef-125">Microsoft. Azure. PowerShell. Cmdlets. BotService. Models. Api20180712. IBot</span><span class="sxs-lookup"><span data-stu-id="de1ef-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="de1ef-126">Note</span><span class="sxs-lookup"><span data-stu-id="de1ef-126">NOTES</span></span>

<span data-ttu-id="de1ef-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="de1ef-127">ALIASES</span></span>

## <span data-ttu-id="de1ef-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de1ef-128">RELATED LINKS</span></span>

