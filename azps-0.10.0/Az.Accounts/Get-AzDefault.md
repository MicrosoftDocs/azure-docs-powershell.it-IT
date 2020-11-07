---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 3e929d2df0b2132b89f6ccff6b83020453b61ad2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860214"
---
# <span data-ttu-id="42f97-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="42f97-101">Get-AzDefault</span></span>

## <span data-ttu-id="42f97-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42f97-102">SYNOPSIS</span></span>
<span data-ttu-id="42f97-103">Ottenere i valori predefiniti impostati dall'utente nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="42f97-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="42f97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42f97-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42f97-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42f97-105">DESCRIPTION</span></span>
<span data-ttu-id="42f97-106">Il cmdlet Get-AzDefault ottiene il gruppo di risorse che l'utente ha impostato come predefinito nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="42f97-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="42f97-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42f97-107">EXAMPLES</span></span>

### <span data-ttu-id="42f97-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="42f97-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="42f97-109">Questo comando restituisce i valori predefiniti correnti se sono impostati valori predefiniti oppure restituisce Nothing se non è impostato alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="42f97-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="42f97-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="42f97-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="42f97-111">Questo comando restituisce il gruppo di risorse predefinito corrente se è presente un set predefinito o restituisce Nothing se non è impostato alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="42f97-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="42f97-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42f97-112">PARAMETERS</span></span>

### <span data-ttu-id="42f97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f97-113">-DefaultProfile</span></span>
<span data-ttu-id="42f97-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42f97-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42f97-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="42f97-115">-ResourceGroup</span></span>
<span data-ttu-id="42f97-116">Visualizzare il gruppo di risorse predefinito</span><span class="sxs-lookup"><span data-stu-id="42f97-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="42f97-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f97-117">CommonParameters</span></span>
<span data-ttu-id="42f97-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42f97-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f97-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42f97-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f97-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42f97-120">INPUTS</span></span>

### <span data-ttu-id="42f97-121">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="42f97-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="42f97-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42f97-122">OUTPUTS</span></span>

### <span data-ttu-id="42f97-123">Microsoft. Azure. Commands. profile. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="42f97-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="42f97-124">Note</span><span class="sxs-lookup"><span data-stu-id="42f97-124">NOTES</span></span>

## <span data-ttu-id="42f97-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42f97-125">RELATED LINKS</span></span>
