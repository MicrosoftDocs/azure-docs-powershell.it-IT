---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 99f591db004fe0c255b5d0ca836a470ff1e547a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675510"
---
# <span data-ttu-id="8cde0-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8cde0-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="8cde0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cde0-102">SYNOPSIS</span></span>
<span data-ttu-id="8cde0-103">Ottenere la proprietà NetworkRule di un account di servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="8cde0-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="8cde0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cde0-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cde0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cde0-105">DESCRIPTION</span></span>
<span data-ttu-id="8cde0-106">Il cmdlet **Get-AzCognitiveServicesAccountNetworkRuleSet** ottiene la proprietà NetworkRule di un account di servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="8cde0-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="8cde0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cde0-107">EXAMPLES</span></span>

### <span data-ttu-id="8cde0-108">Esempio 1: ottenere la proprietà NetworkRule di un account di servizi cognitivi specificato</span><span class="sxs-lookup"><span data-stu-id="8cde0-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="8cde0-109">Questo comando ottiene la proprietà NetworkRule di un account di servizi cognitivi specificato</span><span class="sxs-lookup"><span data-stu-id="8cde0-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="8cde0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cde0-110">PARAMETERS</span></span>

### <span data-ttu-id="8cde0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cde0-111">-DefaultProfile</span></span>
<span data-ttu-id="8cde0-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cde0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cde0-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="8cde0-113">-Name</span></span>
<span data-ttu-id="8cde0-114">Nome account servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="8cde0-114">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="8cde0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cde0-115">-ResourceGroupName</span></span>
<span data-ttu-id="8cde0-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8cde0-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="8cde0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cde0-117">CommonParameters</span></span>
<span data-ttu-id="8cde0-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cde0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cde0-119">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cde0-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cde0-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cde0-120">INPUTS</span></span>

### <span data-ttu-id="8cde0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="8cde0-121">System.String</span></span>

## <span data-ttu-id="8cde0-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cde0-122">OUTPUTS</span></span>

### <span data-ttu-id="8cde0-123">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8cde0-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="8cde0-124">Note</span><span class="sxs-lookup"><span data-stu-id="8cde0-124">NOTES</span></span>

## <span data-ttu-id="8cde0-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cde0-125">RELATED LINKS</span></span>
