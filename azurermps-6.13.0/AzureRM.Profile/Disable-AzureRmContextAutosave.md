---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
ms.openlocfilehash: c421489490dcd579384b211619180209e9d71f5d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521312"
---
# <span data-ttu-id="412c0-101">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="412c0-101">Disable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="412c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="412c0-102">SYNOPSIS</span></span>
<span data-ttu-id="412c0-103">Disattivare il salvataggio delle credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="412c0-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="412c0-104">Le informazioni di accesso verranno dimenticate la volta successiva che si apre una finestra di PowerShell</span><span class="sxs-lookup"><span data-stu-id="412c0-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="412c0-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="412c0-105">SYNTAX</span></span>

```
Disable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="412c0-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="412c0-106">DESCRIPTION</span></span>
<span data-ttu-id="412c0-107">Disattivare il salvataggio delle credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="412c0-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="412c0-108">Le informazioni di accesso verranno dimenticate la volta successiva che si apre una finestra di PowerShell</span><span class="sxs-lookup"><span data-stu-id="412c0-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="412c0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="412c0-109">EXAMPLES</span></span>

### <span data-ttu-id="412c0-110">Disabilitare il salvataggio del contesto</span><span class="sxs-lookup"><span data-stu-id="412c0-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzureRmContextAutosave
```

<span data-ttu-id="412c0-111">Disabilitare il salvataggio automatico per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="412c0-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="412c0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="412c0-112">PARAMETERS</span></span>

### <span data-ttu-id="412c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="412c0-113">-DefaultProfile</span></span>
<span data-ttu-id="412c0-114">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="412c0-114">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="412c0-115">-Ambito</span><span class="sxs-lookup"><span data-stu-id="412c0-115">-Scope</span></span>
<span data-ttu-id="412c0-116">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente</span><span class="sxs-lookup"><span data-stu-id="412c0-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="412c0-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="412c0-117">-Confirm</span></span>
<span data-ttu-id="412c0-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="412c0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="412c0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="412c0-119">-WhatIf</span></span>
<span data-ttu-id="412c0-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="412c0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="412c0-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="412c0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="412c0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="412c0-122">CommonParameters</span></span>
<span data-ttu-id="412c0-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="412c0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="412c0-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="412c0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="412c0-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="412c0-125">INPUTS</span></span>

### <span data-ttu-id="412c0-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="412c0-126">None</span></span>

## <span data-ttu-id="412c0-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="412c0-127">OUTPUTS</span></span>

### <span data-ttu-id="412c0-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="412c0-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="412c0-129">Note</span><span class="sxs-lookup"><span data-stu-id="412c0-129">NOTES</span></span>

## <span data-ttu-id="412c0-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="412c0-130">RELATED LINKS</span></span>
