---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: b7ee3110fec96a10388ffb41b0a82647db461f37
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479195"
---
# <span data-ttu-id="059bd-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="059bd-101">Clear-AzDefault</span></span>

## <span data-ttu-id="059bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="059bd-102">SYNOPSIS</span></span>
<span data-ttu-id="059bd-103">Cancella le impostazioni predefinite impostate dall'utente nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="059bd-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="059bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="059bd-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="059bd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="059bd-105">DESCRIPTION</span></span>
<span data-ttu-id="059bd-106">Il cmdlet Clear-AzDefault rimuove i valori predefiniti impostati dall'utente in base ai parametri di switch specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="059bd-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="059bd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="059bd-107">EXAMPLES</span></span>

### <span data-ttu-id="059bd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="059bd-108">Example 1</span></span>
```powershell
PS C:\> Clear-AzDefault
```

<span data-ttu-id="059bd-109">Questo comando rimuove tutti i valori predefiniti impostati dall'utente nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="059bd-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="059bd-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="059bd-110">Example 2</span></span>
```powershell
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="059bd-111">Questo comando rimuove il gruppo di risorse predefinito impostato dall'utente nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="059bd-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="059bd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="059bd-112">PARAMETERS</span></span>

### <span data-ttu-id="059bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059bd-113">-DefaultProfile</span></span>
<span data-ttu-id="059bd-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="059bd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="059bd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="059bd-115">-Force</span></span>
<span data-ttu-id="059bd-116">Rimuovere tutte le impostazioni predefinite se non è specificato alcun valore predefinito</span><span class="sxs-lookup"><span data-stu-id="059bd-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="059bd-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="059bd-117">-PassThru</span></span>
<span data-ttu-id="059bd-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="059bd-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="059bd-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="059bd-119">-ResourceGroup</span></span>
<span data-ttu-id="059bd-120">Cancellare un gruppo di risorse predefinito</span><span class="sxs-lookup"><span data-stu-id="059bd-120">Clear Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="059bd-121">-Ambito</span><span class="sxs-lookup"><span data-stu-id="059bd-121">-Scope</span></span>
<span data-ttu-id="059bd-122">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="059bd-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="059bd-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="059bd-123">-Confirm</span></span>
<span data-ttu-id="059bd-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="059bd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="059bd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="059bd-125">-WhatIf</span></span>
<span data-ttu-id="059bd-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="059bd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="059bd-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="059bd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="059bd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059bd-128">CommonParameters</span></span>
<span data-ttu-id="059bd-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="059bd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059bd-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="059bd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059bd-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="059bd-131">INPUTS</span></span>

### <span data-ttu-id="059bd-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="059bd-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="059bd-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="059bd-133">OUTPUTS</span></span>

### <span data-ttu-id="059bd-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="059bd-134">System.Boolean</span></span>

## <span data-ttu-id="059bd-135">Note</span><span class="sxs-lookup"><span data-stu-id="059bd-135">NOTES</span></span>

## <span data-ttu-id="059bd-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="059bd-136">RELATED LINKS</span></span>
