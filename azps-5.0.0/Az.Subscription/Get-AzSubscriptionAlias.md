---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: a76c993abb254b1e24200267bf0195cb613d8207
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201440"
---
# <span data-ttu-id="1148e-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="1148e-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="1148e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1148e-102">SYNOPSIS</span></span>
<span data-ttu-id="1148e-103">Ottiene i dettagli degli alias di sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="1148e-103">Gets subscription alias details</span></span>

## <span data-ttu-id="1148e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1148e-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1148e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1148e-105">DESCRIPTION</span></span>
<span data-ttu-id="1148e-106">Il cmdlet **Get-AzSubscriptionAlias** ottiene i dettagli degli alias di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="1148e-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="1148e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1148e-107">EXAMPLES</span></span>

### <span data-ttu-id="1148e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1148e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="1148e-109">Ottiene i dettagli degli alias di sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="1148e-109">Gets subscription alias details</span></span>

## <span data-ttu-id="1148e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1148e-110">PARAMETERS</span></span>

### <span data-ttu-id="1148e-111">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="1148e-111">-AliasName</span></span>
<span data-ttu-id="1148e-112">Alias per l'abbonamento</span><span class="sxs-lookup"><span data-stu-id="1148e-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="1148e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1148e-113">-AsJob</span></span>
<span data-ttu-id="1148e-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1148e-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1148e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1148e-115">-DefaultProfile</span></span>
<span data-ttu-id="1148e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1148e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1148e-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1148e-117">-Confirm</span></span>
<span data-ttu-id="1148e-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1148e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1148e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1148e-119">-WhatIf</span></span>
<span data-ttu-id="1148e-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1148e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1148e-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1148e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1148e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1148e-122">CommonParameters</span></span>
<span data-ttu-id="1148e-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1148e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1148e-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1148e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1148e-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1148e-125">INPUTS</span></span>

### <span data-ttu-id="1148e-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1148e-126">None</span></span>

## <span data-ttu-id="1148e-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1148e-127">OUTPUTS</span></span>

### <span data-ttu-id="1148e-128">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="1148e-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="1148e-129">Note</span><span class="sxs-lookup"><span data-stu-id="1148e-129">NOTES</span></span>

## <span data-ttu-id="1148e-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1148e-130">RELATED LINKS</span></span>
