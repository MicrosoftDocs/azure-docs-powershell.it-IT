---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
ms.openlocfilehash: 02253a59a7f05bfdecd8147325575605334f13ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507444"
---
# <span data-ttu-id="cdd6b-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="cdd6b-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span></span>

## <span data-ttu-id="cdd6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cdd6b-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd6b-103">Creare un oggetto RuleGroupOverride per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="cdd6b-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdd6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdd6b-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRuleGroupOverrideObject -Override <PSRuleGroupOverride> -Action <PSAction>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdd6b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdd6b-105">DESCRIPTION</span></span>
<span data-ttu-id="cdd6b-106">Creare un oggetto RuleGroupOverride per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="cdd6b-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="cdd6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdd6b-107">EXAMPLES</span></span>

### <span data-ttu-id="cdd6b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cdd6b-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorRuleGroupOverrideObject -Override SqlInjection -Action Block

Action RuleGroupOverride
------ -----------------
 Block      SqlInjection
```

<span data-ttu-id="cdd6b-109">Creare un oggetto RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="cdd6b-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="cdd6b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cdd6b-110">PARAMETERS</span></span>

### <span data-ttu-id="cdd6b-111">-Azione</span><span class="sxs-lookup"><span data-stu-id="cdd6b-111">-Action</span></span>
<span data-ttu-id="cdd6b-112">Tipo di azioni.</span><span class="sxs-lookup"><span data-stu-id="cdd6b-112">Type of Actions.</span></span>
<span data-ttu-id="cdd6b-113">I valori possibili includono:' Consenti ',' blocco ',' log '</span><span class="sxs-lookup"><span data-stu-id="cdd6b-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdd6b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd6b-114">-DefaultProfile</span></span>
<span data-ttu-id="cdd6b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cdd6b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdd6b-116">-Override</span><span class="sxs-lookup"><span data-stu-id="cdd6b-116">-Override</span></span>
<span data-ttu-id="cdd6b-117">Descrive overrideruleGroup.</span><span class="sxs-lookup"><span data-stu-id="cdd6b-117">Describes overrideruleGroup.</span></span>
<span data-ttu-id="cdd6b-118">I valori possibili includono: "sqlinjection", "XSS"</span><span class="sxs-lookup"><span data-stu-id="cdd6b-118">Possible values include: 'SqlInjection', 'XSS'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRuleGroupOverride
Parameter Sets: (All)
Aliases:
Accepted values: SqlInjection, XSS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdd6b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd6b-119">CommonParameters</span></span>
<span data-ttu-id="cdd6b-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdd6b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd6b-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdd6b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd6b-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cdd6b-122">INPUTS</span></span>

### <span data-ttu-id="cdd6b-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cdd6b-123">None</span></span>

## <span data-ttu-id="cdd6b-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdd6b-124">OUTPUTS</span></span>

### <span data-ttu-id="cdd6b-125">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="cdd6b-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="cdd6b-126">Note</span><span class="sxs-lookup"><span data-stu-id="cdd6b-126">NOTES</span></span>

## <span data-ttu-id="cdd6b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdd6b-127">RELATED LINKS</span></span>

[<span data-ttu-id="cdd6b-128">New-AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="cdd6b-128">New-AzureRmFrontDoorManagedRuleObject</span></span>](./New-AzureRmFrontDoorManagedRuleObject.md)
