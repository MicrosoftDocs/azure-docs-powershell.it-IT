---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: b808f9272c000ed0ef17079dd31800860a31449b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199935"
---
# <span data-ttu-id="ecdc9-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="ecdc9-101">Clear-AzContext</span></span>

## <span data-ttu-id="ecdc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecdc9-102">SYNOPSIS</span></span>
<span data-ttu-id="ecdc9-103">Rimuovere tutte le informazioni su credenziali, account e abbonamenti di Azure.</span><span class="sxs-lookup"><span data-stu-id="ecdc9-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="ecdc9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecdc9-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecdc9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ecdc9-105">DESCRIPTION</span></span>
<span data-ttu-id="ecdc9-106">Rimuovere tutte le informazioni su credenziali, account e abbonamenti di Azure.</span><span class="sxs-lookup"><span data-stu-id="ecdc9-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="ecdc9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecdc9-107">EXAMPLES</span></span>

### <span data-ttu-id="ecdc9-108">Esempio 1: Cancellare il contesto globale</span><span class="sxs-lookup"><span data-stu-id="ecdc9-108">Example 1: Clear global context</span></span>
```powershell
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="ecdc9-109">Rimuovere tutte le informazioni relative all'account, all'abbonamento e alle credenziali per qualsiasi sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ecdc9-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="ecdc9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecdc9-110">PARAMETERS</span></span>

### <span data-ttu-id="ecdc9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecdc9-111">-DefaultProfile</span></span>
<span data-ttu-id="ecdc9-112">Le credenziali, il tenant e la sottoscrizione usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ecdc9-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecdc9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ecdc9-113">-Force</span></span>
<span data-ttu-id="ecdc9-114">Eliminare tutti gli utenti e i gruppi dall'ambito globale senza chiedere conferma</span><span class="sxs-lookup"><span data-stu-id="ecdc9-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="ecdc9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecdc9-115">-PassThru</span></span>
<span data-ttu-id="ecdc9-116">Restituisce un valore che indica un'operazione riuscita o non riuscita</span><span class="sxs-lookup"><span data-stu-id="ecdc9-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="ecdc9-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="ecdc9-117">-Scope</span></span>
<span data-ttu-id="ecdc9-118">Cancellare il contesto solo per la sessione corrente di PowerShell o per tutte le sessioni.</span><span class="sxs-lookup"><span data-stu-id="ecdc9-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecdc9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecdc9-119">-Confirm</span></span>
<span data-ttu-id="ecdc9-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecdc9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecdc9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecdc9-121">-WhatIf</span></span>
<span data-ttu-id="ecdc9-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecdc9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecdc9-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecdc9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecdc9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecdc9-124">CommonParameters</span></span>
<span data-ttu-id="ecdc9-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecdc9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecdc9-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecdc9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecdc9-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="ecdc9-127">INPUTS</span></span>

### <span data-ttu-id="ecdc9-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ecdc9-128">None</span></span>

## <span data-ttu-id="ecdc9-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecdc9-129">OUTPUTS</span></span>

### <span data-ttu-id="ecdc9-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ecdc9-130">System.Boolean</span></span>

## <span data-ttu-id="ecdc9-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="ecdc9-131">NOTES</span></span>

## <span data-ttu-id="ecdc9-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecdc9-132">RELATED LINKS</span></span>
