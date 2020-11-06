---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: c7a4a34e3969f209bcd6fcaae46ed93cd316aba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511020"
---
# <span data-ttu-id="28f6f-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="28f6f-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="28f6f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="28f6f-103">Abilita o Disabilita il pacchetto di informazioni specificato.</span><span class="sxs-lookup"><span data-stu-id="28f6f-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28f6f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28f6f-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28f6f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28f6f-105">DESCRIPTION</span></span>
<span data-ttu-id="28f6f-106">Il cmdlet **set-AzureRmOperationalInsightsIntelligencePack** Abilita l'intelligence Pack specificata se *Enabled* è impostato su $true e lo Disabilita se *Enabled* è impostato su $false.</span><span class="sxs-lookup"><span data-stu-id="28f6f-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="28f6f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28f6f-107">EXAMPLES</span></span>

### <span data-ttu-id="28f6f-108">Esempio 1: impostare i pacchetti di intelligence</span><span class="sxs-lookup"><span data-stu-id="28f6f-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="28f6f-109">Questo comando Abilita il pacchetto di informazioni specificato.</span><span class="sxs-lookup"><span data-stu-id="28f6f-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="28f6f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28f6f-110">PARAMETERS</span></span>

### <span data-ttu-id="28f6f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28f6f-111">-DefaultProfile</span></span>
<span data-ttu-id="28f6f-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="28f6f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28f6f-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="28f6f-113">-Enabled</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28f6f-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="28f6f-114">-IntelligencePackName</span></span>
<span data-ttu-id="28f6f-115">Specifica il nome del pacchetto di intelligence.</span><span class="sxs-lookup"><span data-stu-id="28f6f-115">Specifies the Intelligence Pack name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28f6f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28f6f-116">-ResourceGroupName</span></span>
<span data-ttu-id="28f6f-117">Specifica il nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="28f6f-117">Specifies the resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28f6f-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="28f6f-118">-WorkspaceName</span></span>
<span data-ttu-id="28f6f-119">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="28f6f-119">Specifies the name of the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28f6f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28f6f-120">CommonParameters</span></span>
<span data-ttu-id="28f6f-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28f6f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28f6f-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28f6f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28f6f-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28f6f-123">INPUTS</span></span>

### <span data-ttu-id="28f6f-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="28f6f-124">None</span></span>
<span data-ttu-id="28f6f-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="28f6f-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="28f6f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28f6f-126">OUTPUTS</span></span>

## <span data-ttu-id="28f6f-127">Note</span><span class="sxs-lookup"><span data-stu-id="28f6f-127">NOTES</span></span>

## <span data-ttu-id="28f6f-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28f6f-128">RELATED LINKS</span></span>

[<span data-ttu-id="28f6f-129">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="28f6f-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


