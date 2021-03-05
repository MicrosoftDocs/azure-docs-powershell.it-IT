---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: aa1bfb0760480d5c2e24e113653037ecb83a9f6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014414"
---
# <span data-ttu-id="e1d25-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="e1d25-101">Get-AzDefault</span></span>

## <span data-ttu-id="e1d25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1d25-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d25-103">Ottenere le impostazioni predefinite impostate dall'utente nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="e1d25-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="e1d25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1d25-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1d25-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e1d25-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d25-106">Il cmdlet Get-AzDefault cmdlet ottiene il gruppo di risorse che l'utente ha impostato come predefinito nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="e1d25-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="e1d25-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1d25-107">EXAMPLES</span></span>

### <span data-ttu-id="e1d25-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e1d25-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="e1d25-109">Questo comando restituisce le impostazioni predefinite correnti se sono impostate impostazioni predefinite oppure non restituisce alcun valore se non è impostata alcuna impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e1d25-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="e1d25-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e1d25-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="e1d25-111">Questo comando restituisce il gruppo di risorse predefinito corrente se è presente un set predefinito oppure non restituisce alcun valore se non è impostata alcuna impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e1d25-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="e1d25-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1d25-112">PARAMETERS</span></span>

### <span data-ttu-id="e1d25-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d25-113">-DefaultProfile</span></span>
<span data-ttu-id="e1d25-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1d25-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1d25-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e1d25-115">-ResourceGroup</span></span>
<span data-ttu-id="e1d25-116">Visualizza gruppo di risorse predefinito</span><span class="sxs-lookup"><span data-stu-id="e1d25-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="e1d25-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d25-117">CommonParameters</span></span>
<span data-ttu-id="e1d25-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d25-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d25-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e1d25-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d25-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="e1d25-120">INPUTS</span></span>

### <span data-ttu-id="e1d25-121">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e1d25-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e1d25-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1d25-122">OUTPUTS</span></span>

### <span data-ttu-id="e1d25-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e1d25-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="e1d25-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="e1d25-124">NOTES</span></span>

## <span data-ttu-id="e1d25-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1d25-125">RELATED LINKS</span></span>
