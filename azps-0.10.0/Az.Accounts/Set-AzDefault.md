---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 8abb473eb5def0d2ca360e0b6116069aecc21b16
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860161"
---
# <span data-ttu-id="2cfc4-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="2cfc4-101">Set-AzDefault</span></span>

## <span data-ttu-id="2cfc4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2cfc4-102">SYNOPSIS</span></span>
<span data-ttu-id="2cfc4-103">Imposta un valore predefinito nel contesto corrente</span><span class="sxs-lookup"><span data-stu-id="2cfc4-103">Sets a default in the current context</span></span>

## <span data-ttu-id="2cfc4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2cfc4-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cfc4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2cfc4-105">DESCRIPTION</span></span>
<span data-ttu-id="2cfc4-106">Il cmdlet Set-AzDefault aggiunge o modifica le impostazioni predefinite nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="2cfc4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2cfc4-107">EXAMPLES</span></span>

### <span data-ttu-id="2cfc4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2cfc4-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="2cfc4-109">Questo comando imposta il gruppo di risorse predefinito per il gruppo di risorse specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="2cfc4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2cfc4-110">PARAMETERS</span></span>

### <span data-ttu-id="2cfc4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cfc4-111">-DefaultProfile</span></span>
<span data-ttu-id="2cfc4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cfc4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2cfc4-113">-Force</span></span>
<span data-ttu-id="2cfc4-114">Creare un nuovo gruppo di risorse se l'impostazione predefinita specificata non esiste</span><span class="sxs-lookup"><span data-stu-id="2cfc4-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="2cfc4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cfc4-115">-ResourceGroupName</span></span>
<span data-ttu-id="2cfc4-116">Nome del gruppo di risorse impostato come predefinito</span><span class="sxs-lookup"><span data-stu-id="2cfc4-116">Name of the resource group being set as default</span></span>

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

### <span data-ttu-id="2cfc4-117">-Ambito</span><span class="sxs-lookup"><span data-stu-id="2cfc4-117">-Scope</span></span>
<span data-ttu-id="2cfc4-118">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="2cfc4-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2cfc4-119">-Confirm</span></span>
<span data-ttu-id="2cfc4-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cfc4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cfc4-121">-WhatIf</span></span>
<span data-ttu-id="2cfc4-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cfc4-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cfc4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cfc4-124">CommonParameters</span></span>
<span data-ttu-id="2cfc4-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cfc4-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cfc4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cfc4-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2cfc4-127">INPUTS</span></span>

### <span data-ttu-id="2cfc4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2cfc4-128">System.String</span></span>

## <span data-ttu-id="2cfc4-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2cfc4-129">OUTPUTS</span></span>

### <span data-ttu-id="2cfc4-130">Microsoft. Azure. Commands. profile. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2cfc4-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="2cfc4-131">Note</span><span class="sxs-lookup"><span data-stu-id="2cfc4-131">NOTES</span></span>

## <span data-ttu-id="2cfc4-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2cfc4-132">RELATED LINKS</span></span>
