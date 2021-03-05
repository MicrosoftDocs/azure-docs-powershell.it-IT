---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 551428a1c5d1737d32aeddf2dd5653586d1dbfbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965085"
---
# <span data-ttu-id="6e938-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="6e938-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="6e938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e938-102">SYNOPSIS</span></span>
<span data-ttu-id="6e938-103">Restituisce un servizio BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="6e938-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="6e938-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e938-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="6e938-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6e938-105">DESCRIPTION</span></span>
<span data-ttu-id="6e938-106">Restituisce un servizio BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="6e938-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="6e938-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e938-107">EXAMPLES</span></span>

### <span data-ttu-id="6e938-108">Esempio 1: Pubblicare il servizio BotService in Azure</span><span class="sxs-lookup"><span data-stu-id="6e938-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="6e938-109">Pubblicare il servizio BotService in Azure tramite codice</span><span class="sxs-lookup"><span data-stu-id="6e938-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="6e938-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e938-110">PARAMETERS</span></span>

### <span data-ttu-id="6e938-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="6e938-111">-CodeDir</span></span>
<span data-ttu-id="6e938-112">Questo parametro definisce il percorso del file ZIP</span><span class="sxs-lookup"><span data-stu-id="6e938-112">This parameter defines the Path of the ZIP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e938-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6e938-113">-Name</span></span>
<span data-ttu-id="6e938-114">Questo parametro definisce il nome del bot.</span><span class="sxs-lookup"><span data-stu-id="6e938-114">This parameter defines the name of the bot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e938-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e938-115">-ResourceGroupName</span></span>
<span data-ttu-id="6e938-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6e938-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e938-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e938-117">-Confirm</span></span>
<span data-ttu-id="6e938-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e938-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e938-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e938-119">-WhatIf</span></span>
<span data-ttu-id="6e938-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e938-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e938-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e938-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e938-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e938-122">CommonParameters</span></span>
<span data-ttu-id="6e938-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e938-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e938-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6e938-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e938-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="6e938-125">INPUTS</span></span>

## <span data-ttu-id="6e938-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e938-126">OUTPUTS</span></span>

## <span data-ttu-id="6e938-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="6e938-127">NOTES</span></span>

<span data-ttu-id="6e938-128">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6e938-128">ALIASES</span></span>

## <span data-ttu-id="6e938-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e938-129">RELATED LINKS</span></span>

