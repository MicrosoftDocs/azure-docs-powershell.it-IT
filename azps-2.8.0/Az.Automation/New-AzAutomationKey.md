---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: 1d0587ae9d1d45de4f08b71baa48ebb5e1633a36
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675760"
---
# <span data-ttu-id="0ae87-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="0ae87-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="0ae87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ae87-102">SYNOPSIS</span></span>
<span data-ttu-id="0ae87-103">Rigenera le chiavi di registrazione per un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="0ae87-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="0ae87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ae87-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ae87-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ae87-105">DESCRIPTION</span></span>
<span data-ttu-id="0ae87-106">Il cmdlet **New-AzAutomationKey** rigenera le chiavi di registrazione per un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0ae87-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="0ae87-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ae87-107">EXAMPLES</span></span>

### <span data-ttu-id="0ae87-108">Esempio 1: rigenerare una chiave per un account di automazione</span><span class="sxs-lookup"><span data-stu-id="0ae87-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="0ae87-109">Questo comando rigenera la chiave primaria per l'account di automazione di Azure denominato AutomationAccount01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0ae87-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="0ae87-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ae87-110">PARAMETERS</span></span>

### <span data-ttu-id="0ae87-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0ae87-111">-AutomationAccountName</span></span>
<span data-ttu-id="0ae87-112">Specifica il nome di un account di automazione per il quale questo cmdlet rigenera le chiavi.</span><span class="sxs-lookup"><span data-stu-id="0ae87-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="0ae87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ae87-113">-DefaultProfile</span></span>
<span data-ttu-id="0ae87-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0ae87-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ae87-115">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="0ae87-115">-KeyType</span></span>
<span data-ttu-id="0ae87-116">Specifica il tipo di chiave di registrazione dell'agente.</span><span class="sxs-lookup"><span data-stu-id="0ae87-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="0ae87-117">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="0ae87-117">Valid values are:</span></span> 
- <span data-ttu-id="0ae87-118">Principale</span><span class="sxs-lookup"><span data-stu-id="0ae87-118">Primary</span></span> 
- <span data-ttu-id="0ae87-119">Secondario</span><span class="sxs-lookup"><span data-stu-id="0ae87-119">Secondary</span></span>

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

### <span data-ttu-id="0ae87-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ae87-120">-ResourceGroupName</span></span>
<span data-ttu-id="0ae87-121">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0ae87-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0ae87-122">Questo cmdlet rigenera le chiavi di un account di automazione nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0ae87-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0ae87-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ae87-123">CommonParameters</span></span>
<span data-ttu-id="0ae87-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ae87-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ae87-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ae87-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ae87-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ae87-126">INPUTS</span></span>

### <span data-ttu-id="0ae87-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0ae87-127">System.String</span></span>

## <span data-ttu-id="0ae87-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ae87-128">OUTPUTS</span></span>

### <span data-ttu-id="0ae87-129">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="0ae87-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="0ae87-130">Note</span><span class="sxs-lookup"><span data-stu-id="0ae87-130">NOTES</span></span>

## <span data-ttu-id="0ae87-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ae87-131">RELATED LINKS</span></span>