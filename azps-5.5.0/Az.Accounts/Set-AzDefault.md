---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 25fd0e1cd651f70fa0900c528f9e5297a8eaf2df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176519"
---
# <span data-ttu-id="d9bcf-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="d9bcf-101">Set-AzDefault</span></span>

## <span data-ttu-id="d9bcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="d9bcf-103">Imposta un valore predefinito nel contesto corrente</span><span class="sxs-lookup"><span data-stu-id="d9bcf-103">Sets a default in the current context</span></span>

## <span data-ttu-id="d9bcf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9bcf-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9bcf-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d9bcf-105">DESCRIPTION</span></span>
<span data-ttu-id="d9bcf-106">Il Set-AzDefault cmdlet aggiunge o modifica le impostazioni predefinite nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="d9bcf-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="d9bcf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9bcf-107">EXAMPLES</span></span>

### <span data-ttu-id="d9bcf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d9bcf-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="d9bcf-109">Questo comando imposta il gruppo di risorse predefinito sul gruppo di risorse specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="d9bcf-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="d9bcf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9bcf-110">PARAMETERS</span></span>

### <span data-ttu-id="d9bcf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9bcf-111">-DefaultProfile</span></span>
<span data-ttu-id="d9bcf-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9bcf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9bcf-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d9bcf-113">-Force</span></span>
<span data-ttu-id="d9bcf-114">Creare un nuovo gruppo di risorse se il valore predefinito specificato non esiste</span><span class="sxs-lookup"><span data-stu-id="d9bcf-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="d9bcf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9bcf-115">-ResourceGroupName</span></span>
<span data-ttu-id="d9bcf-116">Nome del gruppo di risorse impostato come predefinito</span><span class="sxs-lookup"><span data-stu-id="d9bcf-116">Name of the resource group being set as default</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9bcf-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="d9bcf-117">-Scope</span></span>
<span data-ttu-id="d9bcf-118">Determina l'ambito delle modifiche di contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="d9bcf-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="d9bcf-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9bcf-119">-Confirm</span></span>
<span data-ttu-id="d9bcf-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9bcf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9bcf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9bcf-121">-WhatIf</span></span>
<span data-ttu-id="d9bcf-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9bcf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9bcf-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9bcf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9bcf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9bcf-124">CommonParameters</span></span>
<span data-ttu-id="d9bcf-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9bcf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9bcf-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9bcf-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9bcf-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="d9bcf-127">INPUTS</span></span>

### <span data-ttu-id="d9bcf-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d9bcf-128">System.String</span></span>

## <span data-ttu-id="d9bcf-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9bcf-129">OUTPUTS</span></span>

### <span data-ttu-id="d9bcf-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d9bcf-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="d9bcf-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="d9bcf-131">NOTES</span></span>

## <span data-ttu-id="d9bcf-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9bcf-132">RELATED LINKS</span></span>
