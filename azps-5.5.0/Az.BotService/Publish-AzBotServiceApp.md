---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 4ef38ab40f90024124f7d5f09f1a55c16520dd6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200846"
---
# <span data-ttu-id="ba8c0-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="ba8c0-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="ba8c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba8c0-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8c0-103">Restituisce un servizio BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="ba8c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba8c0-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ba8c0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ba8c0-105">DESCRIPTION</span></span>
<span data-ttu-id="ba8c0-106">Restituisce un servizio BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="ba8c0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba8c0-107">EXAMPLES</span></span>

### <span data-ttu-id="ba8c0-108">Esempio 1: Pubblicare il servizio BotService in Azure</span><span class="sxs-lookup"><span data-stu-id="ba8c0-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="ba8c0-109">Pubblicare il servizio BotService in Azure tramite codice</span><span class="sxs-lookup"><span data-stu-id="ba8c0-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="ba8c0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba8c0-110">PARAMETERS</span></span>

### <span data-ttu-id="ba8c0-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="ba8c0-111">-CodeDir</span></span>
<span data-ttu-id="ba8c0-112">Questo parametro definisce il percorso del file ZIP</span><span class="sxs-lookup"><span data-stu-id="ba8c0-112">This parameter defines the Path of the ZIP</span></span>

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

### <span data-ttu-id="ba8c0-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ba8c0-113">-Name</span></span>
<span data-ttu-id="ba8c0-114">Questo parametro definisce il nome del bot.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-114">This parameter defines the name of the bot.</span></span>

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

### <span data-ttu-id="ba8c0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba8c0-115">-ResourceGroupName</span></span>
<span data-ttu-id="ba8c0-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba8c0-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba8c0-117">-Confirm</span></span>
<span data-ttu-id="ba8c0-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba8c0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba8c0-119">-WhatIf</span></span>
<span data-ttu-id="ba8c0-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba8c0-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba8c0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8c0-122">CommonParameters</span></span>
<span data-ttu-id="ba8c0-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8c0-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8c0-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="ba8c0-125">INPUTS</span></span>

## <span data-ttu-id="ba8c0-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba8c0-126">OUTPUTS</span></span>

## <span data-ttu-id="ba8c0-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="ba8c0-127">NOTES</span></span>

<span data-ttu-id="ba8c0-128">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ba8c0-128">ALIASES</span></span>

## <span data-ttu-id="ba8c0-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba8c0-129">RELATED LINKS</span></span>

