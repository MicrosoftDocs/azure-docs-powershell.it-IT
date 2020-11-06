---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
ms.openlocfilehash: 20d66412002e8feb1b4007608091cdbf0422b6c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520431"
---
# <span data-ttu-id="f146c-101">Get-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="f146c-101">Get-AzureRmDefault</span></span>

## <span data-ttu-id="f146c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f146c-102">SYNOPSIS</span></span>
<span data-ttu-id="f146c-103">Ottenere i valori predefiniti impostati dall'utente nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="f146c-103">Get the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f146c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f146c-104">SYNTAX</span></span>

```
Get-AzureRmDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f146c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f146c-105">DESCRIPTION</span></span>
<span data-ttu-id="f146c-106">Il cmdlet Get-AzureRmDefault ottiene il gruppo di risorse che l'utente ha impostato come predefinito nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="f146c-106">The Get-AzureRmDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="f146c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f146c-107">EXAMPLES</span></span>

### <span data-ttu-id="f146c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f146c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="f146c-109">Questo comando restituisce i valori predefiniti correnti se sono impostati valori predefiniti oppure restituisce Nothing se non è impostato alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="f146c-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="f146c-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f146c-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="f146c-111">Questo comando restituisce il gruppo di risorse predefinito corrente se è presente un set predefinito o restituisce Nothing se non è impostato alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="f146c-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="f146c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f146c-112">PARAMETERS</span></span>

### <span data-ttu-id="f146c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f146c-113">-DefaultProfile</span></span>
<span data-ttu-id="f146c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f146c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f146c-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f146c-115">-ResourceGroup</span></span>
<span data-ttu-id="f146c-116">Visualizzare il gruppo di risorse predefinito</span><span class="sxs-lookup"><span data-stu-id="f146c-116">Display Default Resource Group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f146c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f146c-117">CommonParameters</span></span>
<span data-ttu-id="f146c-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f146c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f146c-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f146c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f146c-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f146c-120">INPUTS</span></span>

### <span data-ttu-id="f146c-121">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f146c-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f146c-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f146c-122">OUTPUTS</span></span>

### <span data-ttu-id="f146c-123">Microsoft. Azure. Management. Internal. resources. Models. ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f146c-123">Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroup</span></span>

## <span data-ttu-id="f146c-124">Note</span><span class="sxs-lookup"><span data-stu-id="f146c-124">NOTES</span></span>

## <span data-ttu-id="f146c-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f146c-125">RELATED LINKS</span></span>

