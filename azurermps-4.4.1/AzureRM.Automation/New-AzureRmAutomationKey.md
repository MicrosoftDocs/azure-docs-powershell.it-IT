---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
ms.openlocfilehash: 3b29d1b07ab0c11f42f1a7d4d9326ae19f6b79f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520801"
---
# <span data-ttu-id="798ea-101">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="798ea-101">New-AzureRmAutomationKey</span></span>

## <span data-ttu-id="798ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="798ea-102">SYNOPSIS</span></span>
<span data-ttu-id="798ea-103">Rigenera le chiavi di registrazione per un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="798ea-103">Regenerates registration keys for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="798ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="798ea-104">SYNTAX</span></span>

```
New-AzureRmAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="798ea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="798ea-105">DESCRIPTION</span></span>
<span data-ttu-id="798ea-106">Il cmdlet **New-AzureRmAutomationKey** rigenera le chiavi di registrazione per un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="798ea-106">The **New-AzureRmAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="798ea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="798ea-107">EXAMPLES</span></span>

### <span data-ttu-id="798ea-108">Esempio 1: rigenerare una chiave per un account di automazione</span><span class="sxs-lookup"><span data-stu-id="798ea-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzureAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="798ea-109">Questo comando rigenera la chiave primaria per l'account di automazione di Azure denominato AutomationAccount01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="798ea-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="798ea-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="798ea-110">PARAMETERS</span></span>

### <span data-ttu-id="798ea-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="798ea-111">-AutomationAccountName</span></span>
<span data-ttu-id="798ea-112">Specifica il nome di un account di automazione per il quale questo cmdlet rigenera le chiavi.</span><span class="sxs-lookup"><span data-stu-id="798ea-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="798ea-113">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="798ea-113">-KeyType</span></span>
<span data-ttu-id="798ea-114">Specifica il tipo di chiave di registrazione dell'agente.</span><span class="sxs-lookup"><span data-stu-id="798ea-114">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="798ea-115">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="798ea-115">Valid values are:</span></span> 

- <span data-ttu-id="798ea-116">Principale</span><span class="sxs-lookup"><span data-stu-id="798ea-116">Primary</span></span> 
- <span data-ttu-id="798ea-117">Secondario</span><span class="sxs-lookup"><span data-stu-id="798ea-117">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="798ea-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="798ea-118">-ResourceGroupName</span></span>
<span data-ttu-id="798ea-119">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="798ea-119">Specifies the name of a resource group.</span></span>
<span data-ttu-id="798ea-120">Questo cmdlet rigenera le chiavi di un account di automazione nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="798ea-120">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="798ea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="798ea-121">-DefaultProfile</span></span>
<span data-ttu-id="798ea-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="798ea-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="798ea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="798ea-123">CommonParameters</span></span>
<span data-ttu-id="798ea-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="798ea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="798ea-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="798ea-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="798ea-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="798ea-126">INPUTS</span></span>

## <span data-ttu-id="798ea-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="798ea-127">OUTPUTS</span></span>

### <span data-ttu-id="798ea-128">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="798ea-128">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="798ea-129">Note</span><span class="sxs-lookup"><span data-stu-id="798ea-129">NOTES</span></span>

## <span data-ttu-id="798ea-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="798ea-130">RELATED LINKS</span></span>

