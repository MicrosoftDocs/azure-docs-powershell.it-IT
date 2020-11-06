---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/enable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
ms.openlocfilehash: 0e875087d52ecddbf216c6e49db96fefdf63e82f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520432"
---
# <span data-ttu-id="313e5-101">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="313e5-101">Enable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="313e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="313e5-102">SYNOPSIS</span></span>
<span data-ttu-id="313e5-103">Consentire il salvataggio e la carica automatica delle credenziali di Azure, delle informazioni sull'account e dell'abbonamento quando si apre una finestra di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="313e5-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="313e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="313e5-104">SYNTAX</span></span>

```
Enable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="313e5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="313e5-105">DESCRIPTION</span></span>
<span data-ttu-id="313e5-106">Consentire il salvataggio e la carica automatica delle credenziali di Azure, delle informazioni sull'account e dell'abbonamento quando si apre una finestra di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="313e5-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="313e5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="313e5-107">EXAMPLES</span></span>

### <span data-ttu-id="313e5-108">Abilitare il salvataggio delle credenziali per l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="313e5-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzureRmContextAutosave
```

<span data-ttu-id="313e5-109">Attivare il salvataggio automatico delle credenziali per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="313e5-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="313e5-110">Ogni volta che viene aperta una finestra di PowerShell, il contesto corrente verrà ricordato senza effettuare l'accesso.</span><span class="sxs-lookup"><span data-stu-id="313e5-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="313e5-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="313e5-111">PARAMETERS</span></span>

### <span data-ttu-id="313e5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="313e5-112">-DefaultProfile</span></span>
<span data-ttu-id="313e5-113">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="313e5-113">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313e5-114">-Ambito</span><span class="sxs-lookup"><span data-stu-id="313e5-114">-Scope</span></span>
<span data-ttu-id="313e5-115">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente</span><span class="sxs-lookup"><span data-stu-id="313e5-115">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313e5-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="313e5-116">-Confirm</span></span>
<span data-ttu-id="313e5-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="313e5-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313e5-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="313e5-118">-WhatIf</span></span>
<span data-ttu-id="313e5-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="313e5-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="313e5-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="313e5-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313e5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="313e5-121">CommonParameters</span></span>
<span data-ttu-id="313e5-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="313e5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="313e5-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="313e5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="313e5-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="313e5-124">INPUTS</span></span>

### <span data-ttu-id="313e5-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="313e5-125">None</span></span>

## <span data-ttu-id="313e5-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="313e5-126">OUTPUTS</span></span>

### <span data-ttu-id="313e5-127">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="313e5-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="313e5-128">Informazioni sulle impostazioni di salvataggio automatico correnti, ad esempio se l'opzione Salvataggio automatico è abilitata per l'utente corrente e dove vengono salvati i file di contesto e credenziale.</span><span class="sxs-lookup"><span data-stu-id="313e5-128">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="313e5-129">Note</span><span class="sxs-lookup"><span data-stu-id="313e5-129">NOTES</span></span>

## <span data-ttu-id="313e5-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="313e5-130">RELATED LINKS</span></span>

