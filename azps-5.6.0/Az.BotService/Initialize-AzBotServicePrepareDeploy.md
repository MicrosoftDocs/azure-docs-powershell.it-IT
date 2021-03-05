---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 118fce3e75ee7ba66fa30e6e07cfce16e5dadcff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009309"
---
# <span data-ttu-id="d9e97-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="d9e97-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="d9e97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9e97-102">SYNOPSIS</span></span>
<span data-ttu-id="d9e97-103">Restituisce un servizio BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="d9e97-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="d9e97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9e97-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d9e97-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d9e97-105">DESCRIPTION</span></span>
<span data-ttu-id="d9e97-106">Restituisce un servizio BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="d9e97-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="d9e97-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9e97-107">EXAMPLES</span></span>

### <span data-ttu-id="d9e97-108">Esempio 1: Inizializzare la cartella FileFolder del progetto</span><span class="sxs-lookup"><span data-stu-id="d9e97-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="d9e97-109">Initialize consente di preparare una risorsa per l'uso e impostarla su uno stato predefinito</span><span class="sxs-lookup"><span data-stu-id="d9e97-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="d9e97-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9e97-110">PARAMETERS</span></span>

### <span data-ttu-id="d9e97-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="d9e97-111">-CodeDir</span></span>
<span data-ttu-id="d9e97-112">Nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d9e97-112">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="d9e97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9e97-113">-DefaultProfile</span></span>
<span data-ttu-id="d9e97-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9e97-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9e97-115">-Lingua</span><span class="sxs-lookup"><span data-stu-id="d9e97-115">-Language</span></span>


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

### <span data-ttu-id="d9e97-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="d9e97-116">-ProjFileName</span></span>


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

### <span data-ttu-id="d9e97-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9e97-117">-SubscriptionId</span></span>
<span data-ttu-id="d9e97-118">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="d9e97-118">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d9e97-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9e97-119">CommonParameters</span></span>
<span data-ttu-id="d9e97-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9e97-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9e97-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d9e97-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9e97-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="d9e97-122">INPUTS</span></span>

## <span data-ttu-id="d9e97-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9e97-123">OUTPUTS</span></span>

### <span data-ttu-id="d9e97-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="d9e97-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="d9e97-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="d9e97-125">NOTES</span></span>

<span data-ttu-id="d9e97-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d9e97-126">ALIASES</span></span>

## <span data-ttu-id="d9e97-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9e97-127">RELATED LINKS</span></span>

