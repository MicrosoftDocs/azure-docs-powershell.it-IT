---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 4ef38ab40f90024124f7d5f09f1a55c16520dd6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488696"
---
# <span data-ttu-id="c54b3-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="c54b3-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="c54b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c54b3-102">SYNOPSIS</span></span>
<span data-ttu-id="c54b3-103">Restituisce un BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="c54b3-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="c54b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c54b3-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c54b3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c54b3-105">DESCRIPTION</span></span>
<span data-ttu-id="c54b3-106">Restituisce un BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="c54b3-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="c54b3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c54b3-107">EXAMPLES</span></span>

### <span data-ttu-id="c54b3-108">Esempio 1: pubblicare il proprio BotService in Azure</span><span class="sxs-lookup"><span data-stu-id="c54b3-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="c54b3-109">Pubblicare il BotService in Azure per codice</span><span class="sxs-lookup"><span data-stu-id="c54b3-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="c54b3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c54b3-110">PARAMETERS</span></span>

### <span data-ttu-id="c54b3-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="c54b3-111">-CodeDir</span></span>
<span data-ttu-id="c54b3-112">Questo parametro definisce il percorso della cerniera</span><span class="sxs-lookup"><span data-stu-id="c54b3-112">This parameter defines the Path of the ZIP</span></span>

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

### <span data-ttu-id="c54b3-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="c54b3-113">-Name</span></span>
<span data-ttu-id="c54b3-114">Questo parametro definisce il nome del bot.</span><span class="sxs-lookup"><span data-stu-id="c54b3-114">This parameter defines the name of the bot.</span></span>

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

### <span data-ttu-id="c54b3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c54b3-115">-ResourceGroupName</span></span>
<span data-ttu-id="c54b3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c54b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c54b3-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c54b3-117">-Confirm</span></span>
<span data-ttu-id="c54b3-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c54b3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c54b3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c54b3-119">-WhatIf</span></span>
<span data-ttu-id="c54b3-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c54b3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c54b3-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c54b3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c54b3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c54b3-122">CommonParameters</span></span>
<span data-ttu-id="c54b3-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c54b3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c54b3-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c54b3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c54b3-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c54b3-125">INPUTS</span></span>

## <span data-ttu-id="c54b3-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c54b3-126">OUTPUTS</span></span>

## <span data-ttu-id="c54b3-127">Note</span><span class="sxs-lookup"><span data-stu-id="c54b3-127">NOTES</span></span>

<span data-ttu-id="c54b3-128">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c54b3-128">ALIASES</span></span>

## <span data-ttu-id="c54b3-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c54b3-129">RELATED LINKS</span></span>

