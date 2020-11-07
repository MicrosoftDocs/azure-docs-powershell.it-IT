---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
ms.openlocfilehash: a29bf86b4104fb9a3936daad055da0eab4368690
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688066"
---
# <span data-ttu-id="32e20-101">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="32e20-101">Clear-AzureRmDefault</span></span>

## <span data-ttu-id="32e20-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32e20-102">SYNOPSIS</span></span>
<span data-ttu-id="32e20-103">Cancella le impostazioni predefinite impostate dall'utente nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="32e20-103">Clears the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32e20-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32e20-104">SYNTAX</span></span>

```
Clear-AzureRmDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32e20-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32e20-105">DESCRIPTION</span></span>
<span data-ttu-id="32e20-106">Il cmdlet Clear-AzureRmDefault rimuove i valori predefiniti impostati dall'utente in base ai parametri di switch specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="32e20-106">The Clear-AzureRmDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="32e20-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32e20-107">EXAMPLES</span></span>

### <span data-ttu-id="32e20-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="32e20-108">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault
```

<span data-ttu-id="32e20-109">Questo comando rimuove tutti i valori predefiniti impostati dall'utente nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="32e20-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="32e20-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="32e20-110">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault -ResourceGroup
```

<span data-ttu-id="32e20-111">Questo comando rimuove il gruppo di risorse predefinito impostato dall'utente nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="32e20-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="32e20-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32e20-112">PARAMETERS</span></span>

### <span data-ttu-id="32e20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32e20-113">-DefaultProfile</span></span>
<span data-ttu-id="32e20-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32e20-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32e20-115">-Force</span><span class="sxs-lookup"><span data-stu-id="32e20-115">-Force</span></span>
<span data-ttu-id="32e20-116">Rimuovere tutte le impostazioni predefinite se non è specificato alcun valore predefinito</span><span class="sxs-lookup"><span data-stu-id="32e20-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="32e20-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32e20-117">-PassThru</span></span>
<span data-ttu-id="32e20-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="32e20-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="32e20-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="32e20-119">-ResourceGroup</span></span>
<span data-ttu-id="32e20-120">Cancellare un gruppo di risorse predefinito</span><span class="sxs-lookup"><span data-stu-id="32e20-120">Clear Default Resource Group</span></span>

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

### <span data-ttu-id="32e20-121">-Ambito</span><span class="sxs-lookup"><span data-stu-id="32e20-121">-Scope</span></span>
<span data-ttu-id="32e20-122">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="32e20-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="32e20-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="32e20-123">-Confirm</span></span>
<span data-ttu-id="32e20-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32e20-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32e20-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32e20-125">-WhatIf</span></span>
<span data-ttu-id="32e20-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32e20-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32e20-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32e20-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32e20-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e20-128">CommonParameters</span></span>
<span data-ttu-id="32e20-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32e20-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e20-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32e20-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e20-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32e20-131">INPUTS</span></span>

### <span data-ttu-id="32e20-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="32e20-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="32e20-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32e20-133">OUTPUTS</span></span>

### <span data-ttu-id="32e20-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="32e20-134">System.Boolean</span></span>

## <span data-ttu-id="32e20-135">Note</span><span class="sxs-lookup"><span data-stu-id="32e20-135">NOTES</span></span>

## <span data-ttu-id="32e20-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32e20-136">RELATED LINKS</span></span>
