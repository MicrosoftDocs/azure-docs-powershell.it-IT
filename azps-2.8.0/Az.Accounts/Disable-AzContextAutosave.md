---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
ms.openlocfilehash: 2147fd87cae8ef87010c54ce42dc33c85a8f6374
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676232"
---
# <span data-ttu-id="0b4ab-101">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="0b4ab-101">Disable-AzContextAutosave</span></span>

## <span data-ttu-id="0b4ab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b4ab-102">SYNOPSIS</span></span>
<span data-ttu-id="0b4ab-103">Disattivare il salvataggio delle credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="0b4ab-104">Le informazioni di accesso verranno dimenticate la volta successiva che si apre una finestra di PowerShell</span><span class="sxs-lookup"><span data-stu-id="0b4ab-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="0b4ab-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b4ab-105">SYNTAX</span></span>

```
Disable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b4ab-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b4ab-106">DESCRIPTION</span></span>
<span data-ttu-id="0b4ab-107">Disattivare il salvataggio delle credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="0b4ab-108">Le informazioni di accesso verranno dimenticate la volta successiva che si apre una finestra di PowerShell</span><span class="sxs-lookup"><span data-stu-id="0b4ab-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="0b4ab-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b4ab-109">EXAMPLES</span></span>

### <span data-ttu-id="0b4ab-110">Disabilitare il salvataggio del contesto</span><span class="sxs-lookup"><span data-stu-id="0b4ab-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzContextAutosave
```

<span data-ttu-id="0b4ab-111">Disabilitare il salvataggio automatico per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="0b4ab-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b4ab-112">PARAMETERS</span></span>

### <span data-ttu-id="0b4ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b4ab-113">-DefaultProfile</span></span>
<span data-ttu-id="0b4ab-114">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0b4ab-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b4ab-115">-Ambito</span><span class="sxs-lookup"><span data-stu-id="0b4ab-115">-Scope</span></span>
<span data-ttu-id="0b4ab-116">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente</span><span class="sxs-lookup"><span data-stu-id="0b4ab-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="0b4ab-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0b4ab-117">-Confirm</span></span>
<span data-ttu-id="0b4ab-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b4ab-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b4ab-119">-WhatIf</span></span>
<span data-ttu-id="0b4ab-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b4ab-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b4ab-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b4ab-122">CommonParameters</span></span>
<span data-ttu-id="0b4ab-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b4ab-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b4ab-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b4ab-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b4ab-125">INPUTS</span></span>

### <span data-ttu-id="0b4ab-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0b4ab-126">None</span></span>

## <span data-ttu-id="0b4ab-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b4ab-127">OUTPUTS</span></span>

### <span data-ttu-id="0b4ab-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="0b4ab-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="0b4ab-129">Note</span><span class="sxs-lookup"><span data-stu-id="0b4ab-129">NOTES</span></span>

## <span data-ttu-id="0b4ab-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b4ab-130">RELATED LINKS</span></span>
