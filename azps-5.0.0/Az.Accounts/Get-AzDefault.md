---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 43806326f572030997299353cfc7e79e5587a4ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199761"
---
# <span data-ttu-id="30370-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="30370-101">Get-AzDefault</span></span>

## <span data-ttu-id="30370-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30370-102">SYNOPSIS</span></span>
<span data-ttu-id="30370-103">Ottenere i valori predefiniti impostati dall'utente nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="30370-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="30370-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30370-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30370-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30370-105">DESCRIPTION</span></span>
<span data-ttu-id="30370-106">Il cmdlet Get-AzDefault ottiene il gruppo di risorse che l'utente ha impostato come predefinito nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="30370-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="30370-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30370-107">EXAMPLES</span></span>

### <span data-ttu-id="30370-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="30370-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="30370-109">Questo comando restituisce i valori predefiniti correnti se sono impostati valori predefiniti oppure restituisce Nothing se non è impostato alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="30370-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="30370-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="30370-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="30370-111">Questo comando restituisce il gruppo di risorse predefinito corrente se è presente un set predefinito o restituisce Nothing se non è impostato alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="30370-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="30370-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30370-112">PARAMETERS</span></span>

### <span data-ttu-id="30370-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30370-113">-DefaultProfile</span></span>
<span data-ttu-id="30370-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30370-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30370-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="30370-115">-ResourceGroup</span></span>
<span data-ttu-id="30370-116">Visualizzare il gruppo di risorse predefinito</span><span class="sxs-lookup"><span data-stu-id="30370-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="30370-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30370-117">CommonParameters</span></span>
<span data-ttu-id="30370-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30370-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30370-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30370-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30370-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30370-120">INPUTS</span></span>

### <span data-ttu-id="30370-121">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="30370-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="30370-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30370-122">OUTPUTS</span></span>

### <span data-ttu-id="30370-123">Microsoft. Azure. Commands. profile. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="30370-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="30370-124">Note</span><span class="sxs-lookup"><span data-stu-id="30370-124">NOTES</span></span>

## <span data-ttu-id="30370-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30370-125">RELATED LINKS</span></span>