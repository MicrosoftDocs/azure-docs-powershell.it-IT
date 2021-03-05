---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: dd5ca513c327a1ed5d045c3b0283a8b220f6a062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967022"
---
# <span data-ttu-id="f5907-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5907-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="f5907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5907-102">SYNOPSIS</span></span>
<span data-ttu-id="f5907-103">Ottenere le configurazioni di Azure Advisor per la sottoscrizione o il gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="f5907-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="f5907-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5907-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5907-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f5907-105">DESCRIPTION</span></span>
<span data-ttu-id="f5907-106">Le configurazioni associate a un abbonamento sono di due tipi:</span><span class="sxs-lookup"><span data-stu-id="f5907-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="f5907-107">Configurazione a livello di abbonamento: per una sottoscrizione può essere presente una sola configurazione di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="f5907-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="f5907-108">LowCpuThreshold ed Exclude sono l'unica proprietà di questo tipo di configurazione.</span><span class="sxs-lookup"><span data-stu-id="f5907-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="f5907-109">Configurazione a livello di Gruppo Risorse: può essere presente una sola configurazione per ogni ResourceGroup di una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="f5907-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="f5907-110">Exclude è l'unica proprietà di questo tipo di configurazione.</span><span class="sxs-lookup"><span data-stu-id="f5907-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="f5907-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5907-111">EXAMPLES</span></span>

### <span data-ttu-id="f5907-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f5907-112">Example 1</span></span>
```powershell
PS C:\>$data = Get-AzAdvisorConfiguration
Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}-{resourceGroupName}
Name       : {user_subscription}-{resourceGroupName}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

PS C:\>$data[0].Properties
AdditionalProperties :
Exclude              : False
LowCpuThreshold      : 20

PS C:\>$data[1].Properties
AdditionalProperties :
Exclude              : True
LowCpuThreshold      : null

```
<span data-ttu-id="f5907-113">Recupera un elenco di configurazioni di Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="f5907-113">Retrieves a list of Azure Advisor Configuration(s).</span></span>

## <span data-ttu-id="f5907-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5907-114">PARAMETERS</span></span>

### <span data-ttu-id="f5907-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5907-115">-DefaultProfile</span></span>
<span data-ttu-id="f5907-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f5907-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5907-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5907-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5907-118">Nome del gruppo di risorse della configurazione</span><span class="sxs-lookup"><span data-stu-id="f5907-118">Resource Group name of the configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5907-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5907-119">CommonParameters</span></span>
<span data-ttu-id="f5907-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5907-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f5907-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5907-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5907-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="f5907-122">INPUTS</span></span>

### <span data-ttu-id="f5907-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f5907-123">None</span></span>

## <span data-ttu-id="f5907-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5907-124">OUTPUTS</span></span>

### <span data-ttu-id="f5907-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="f5907-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="f5907-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="f5907-126">NOTES</span></span>

## <span data-ttu-id="f5907-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5907-127">RELATED LINKS</span></span>
