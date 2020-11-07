---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: 41d43bcb1164907bc7a06a7de4477f8a719604eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676237"
---
# <span data-ttu-id="86326-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="86326-101">Clear-AzDefault</span></span>

## <span data-ttu-id="86326-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86326-102">SYNOPSIS</span></span>
<span data-ttu-id="86326-103">Cancella le impostazioni predefinite impostate dall'utente nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="86326-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="86326-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86326-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86326-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86326-105">DESCRIPTION</span></span>
<span data-ttu-id="86326-106">Il cmdlet Clear-AzDefault rimuove i valori predefiniti impostati dall'utente in base ai parametri di switch specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="86326-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="86326-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86326-107">EXAMPLES</span></span>

### <span data-ttu-id="86326-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="86326-108">Example 1</span></span>
```
PS C:\> Clear-AzDefault
```

<span data-ttu-id="86326-109">Questo comando rimuove tutti i valori predefiniti impostati dall'utente nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="86326-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="86326-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="86326-110">Example 1</span></span>
```
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="86326-111">Questo comando rimuove il gruppo di risorse predefinito impostato dall'utente nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="86326-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="86326-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86326-112">PARAMETERS</span></span>

### <span data-ttu-id="86326-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86326-113">-DefaultProfile</span></span>
<span data-ttu-id="86326-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86326-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86326-115">-Force</span><span class="sxs-lookup"><span data-stu-id="86326-115">-Force</span></span>
<span data-ttu-id="86326-116">Rimuovere tutte le impostazioni predefinite se non è specificato alcun valore predefinito</span><span class="sxs-lookup"><span data-stu-id="86326-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="86326-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86326-117">-PassThru</span></span>
<span data-ttu-id="86326-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="86326-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="86326-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="86326-119">-ResourceGroup</span></span>
<span data-ttu-id="86326-120">Cancellare un gruppo di risorse predefinito</span><span class="sxs-lookup"><span data-stu-id="86326-120">Clear Default Resource Group</span></span>

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

### <span data-ttu-id="86326-121">-Ambito</span><span class="sxs-lookup"><span data-stu-id="86326-121">-Scope</span></span>
<span data-ttu-id="86326-122">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="86326-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="86326-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="86326-123">-Confirm</span></span>
<span data-ttu-id="86326-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86326-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86326-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86326-125">-WhatIf</span></span>
<span data-ttu-id="86326-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86326-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86326-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86326-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86326-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86326-128">CommonParameters</span></span>
<span data-ttu-id="86326-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86326-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86326-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86326-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86326-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86326-131">INPUTS</span></span>

### <span data-ttu-id="86326-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="86326-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="86326-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86326-133">OUTPUTS</span></span>

### <span data-ttu-id="86326-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86326-134">System.Boolean</span></span>

## <span data-ttu-id="86326-135">Note</span><span class="sxs-lookup"><span data-stu-id="86326-135">NOTES</span></span>

## <span data-ttu-id="86326-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86326-136">RELATED LINKS</span></span>
