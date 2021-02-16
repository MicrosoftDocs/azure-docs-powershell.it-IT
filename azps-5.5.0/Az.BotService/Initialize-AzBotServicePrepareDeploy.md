---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 97f13dc7c9a74fef3775d0aed0db9d7acfa4da43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200854"
---
# <span data-ttu-id="13c74-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="13c74-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="13c74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13c74-102">SYNOPSIS</span></span>
<span data-ttu-id="13c74-103">Restituisce un servizio BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="13c74-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="13c74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13c74-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="13c74-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="13c74-105">DESCRIPTION</span></span>
<span data-ttu-id="13c74-106">Restituisce un servizio BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="13c74-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="13c74-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13c74-107">EXAMPLES</span></span>

### <span data-ttu-id="13c74-108">Esempio 1: Inizializzare la cartella FileFolder del progetto</span><span class="sxs-lookup"><span data-stu-id="13c74-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="13c74-109">Initialize consente di preparare una risorsa per l'uso e impostarla su uno stato predefinito</span><span class="sxs-lookup"><span data-stu-id="13c74-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="13c74-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13c74-110">PARAMETERS</span></span>

### <span data-ttu-id="13c74-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="13c74-111">-CodeDir</span></span>
<span data-ttu-id="13c74-112">Nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="13c74-112">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="13c74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c74-113">-DefaultProfile</span></span>
<span data-ttu-id="13c74-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13c74-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13c74-115">-Lingua</span><span class="sxs-lookup"><span data-stu-id="13c74-115">-Language</span></span>


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

### <span data-ttu-id="13c74-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="13c74-116">-ProjFileName</span></span>


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

### <span data-ttu-id="13c74-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13c74-117">-SubscriptionId</span></span>
<span data-ttu-id="13c74-118">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="13c74-118">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="13c74-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c74-119">CommonParameters</span></span>
<span data-ttu-id="13c74-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13c74-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c74-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="13c74-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c74-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="13c74-122">INPUTS</span></span>

## <span data-ttu-id="13c74-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13c74-123">OUTPUTS</span></span>

### <span data-ttu-id="13c74-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="13c74-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="13c74-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="13c74-125">NOTES</span></span>

<span data-ttu-id="13c74-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="13c74-126">ALIASES</span></span>

## <span data-ttu-id="13c74-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13c74-127">RELATED LINKS</span></span>

