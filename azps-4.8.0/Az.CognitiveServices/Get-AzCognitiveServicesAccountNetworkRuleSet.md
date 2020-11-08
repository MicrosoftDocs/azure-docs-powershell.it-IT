---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 24b2cb6efca1213365c99a2c095f90e675c317c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031617"
---
# <span data-ttu-id="9aced-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9aced-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="9aced-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9aced-102">SYNOPSIS</span></span>
<span data-ttu-id="9aced-103">Ottenere la proprietà NetworkRule di un account di servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="9aced-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="9aced-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9aced-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9aced-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9aced-105">DESCRIPTION</span></span>
<span data-ttu-id="9aced-106">Il cmdlet **Get-AzCognitiveServicesAccountNetworkRuleSet** ottiene la proprietà NetworkRule di un account di servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="9aced-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="9aced-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9aced-107">EXAMPLES</span></span>

### <span data-ttu-id="9aced-108">Esempio 1: ottenere la proprietà NetworkRule di un account di servizi cognitivi specificato</span><span class="sxs-lookup"><span data-stu-id="9aced-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="9aced-109">Questo comando ottiene la proprietà NetworkRule di un account di servizi cognitivi specificato</span><span class="sxs-lookup"><span data-stu-id="9aced-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="9aced-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9aced-110">PARAMETERS</span></span>

### <span data-ttu-id="9aced-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aced-111">-DefaultProfile</span></span>
<span data-ttu-id="9aced-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9aced-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9aced-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="9aced-113">-Name</span></span>
<span data-ttu-id="9aced-114">Nome account servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="9aced-114">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aced-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aced-115">-ResourceGroupName</span></span>
<span data-ttu-id="9aced-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9aced-116">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aced-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aced-117">CommonParameters</span></span>
<span data-ttu-id="9aced-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9aced-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aced-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9aced-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aced-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9aced-120">INPUTS</span></span>

### <span data-ttu-id="9aced-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9aced-121">System.String</span></span>

## <span data-ttu-id="9aced-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9aced-122">OUTPUTS</span></span>

### <span data-ttu-id="9aced-123">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9aced-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="9aced-124">Note</span><span class="sxs-lookup"><span data-stu-id="9aced-124">NOTES</span></span>

## <span data-ttu-id="9aced-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9aced-125">RELATED LINKS</span></span>
